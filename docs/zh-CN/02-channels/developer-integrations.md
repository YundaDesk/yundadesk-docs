---
title: 配置 Custom API 与事件推送
description: 配置 Custom API 的 Callback 或本地 Pull，以及签名和事件推送。
category: 渠道
order: 6
updated_at: 2026-08-29
---

# 配置 Custom API 与事件推送

Custom API 渠道和事件推送用于把自有系统与 YundaDesk 连接起来。当前可用能力以产品中的套餐页为准。

## 套餐变化时会发生什么

如果工作区切换到不再包含某项开发者集成能力的套餐：

- 已有配置、签名密钥和历史投递记录不会被删除。
- 对应的 Custom API 渠道或事件推送会被停用，不再接收或发送新的集成流量。
- 你仍可以查看、禁用或删除已有配置，但不能创建、启用、测试、重放或轮换密钥。
- 再次获得权益后不会自动恢复，请检查配置后手动启用。

## 选择回复方式

创建 Custom API 渠道时，选择一种客服回复方式：

- **Callback**：YundaDesk 主动把客服回复推送到你的公网回调地址。适合已有公网 HTTPS 服务的系统。
- **Pull（本地 Connector）**：本地 Connector 主动长轮询 YundaDesk，再把回复转发到本机服务。适合开发机、门店电脑或没有公网入口的系统。

两种方式会长期并存，不是迁移关系。一个渠道只能选择一种回复方式；不同渠道可以分别使用 Callback 和 Pull。客户消息的入站地址不受此选择影响，仍使用页面显示的 Custom API 入站地址。

创建页不会显示 Channel Key 和签名密钥；这两个值会在保存渠道后由系统自动生成，并在已保存渠道的详情中提供。

## 配置 Callback 地址

仅 Callback 模式需要填写回调地址。回调地址或事件推送地址必须满足：

- 使用公网 `https://` 地址，端口为 443。
- 地址中不能包含用户名、密码或 `#` 片段。
- 域名必须与保存的允许域名一致；如需允许多个子域，请显式配置受控的通配子域。
- 目标服务器需要能够从 YundaDesk 公布的固定出口 IP 接收请求。

保存后使用页面上的“测试”操作验证连接。测试成功只代表当前请求可达；正式使用前还应在目标系统核对签名、事件内容和来源 IP。

## 配置 Pull API

1. 创建或编辑 Custom API 渠道，把回复方式设为 **Pull（本地 Connector）**，然后保存。
2. 选择 Pull 后，右侧会显示“发送给你的开发 Agent”。提示词会明确两个公开地址：向 Custom API 入站地址发送客户消息，向 Pull 地址拉取客服回复，并包含鉴权头、请求体和 offset 处理要求。创建前 Channel Key 使用占位符；保存后会自动带入当前渠道的真实值。
3. 提示词不会包含签名密钥。保存渠道后，从渠道详情把签名密钥放入项目的安全配置；不要把它粘贴到 Agent 对话、源码、日志或 offset 状态文件。
4. 你的系统直接请求 Pull 地址。成功响应为 `{ "success": true, "data": { "updates": [...], "next_offset": 1 }, "error": null }`：首次提交 `offset=0`，处理完 `data.updates` 后持久化 `data.next_offset`，并在下一次请求中提交。任一条更新处理失败时不要推进 offset；`data.updates` 为空是正常的长轮询超时。
5. 如果不想自行实现轮询，也可以安全设置 `YD_CUSTOM_API_SIGNING_SECRET`，使用本地 Connector 把回复转发到本机 HTTP 地址，例如 `http://127.0.0.1:8080/yundadesk/callback`：

```bash
customapi-pull \
  --pull-url "<页面显示的 Pull URL>" \
  --channel-key "<页面显示的 Channel Key>" \
  --forward-url "http://127.0.0.1:8080/yundadesk/callback" \
  --consumer-id "my-local-connector"
```

Connector 会在用户配置目录保存非敏感 offset。只有本机接收地址返回 2xx 后，它才确认该条回复；进程中断后可能重复转发最后一条，但不会因提前确认而丢失。接收端应使用 `Idempotency-Key` 或 `X-YD-Update-ID` 请求头去重。

同一渠道不要同时运行多个 Connector。需要迁移本机时，先停止旧 Connector，再把 offset 状态文件安全迁移到新机器；如果无法迁移，应准备接收端按幂等键处理可能的重复。

## 固定出口 IP

YundaDesk 通过固定出口 IP 发送 Custom API Callback 和事件 Webhook。Pull 是本地 Connector 主动出站访问 YundaDesk，不需要为 Pull 配置 YundaDesk 出口 IP。页面默认不直接展开 Callback/Event Webhook 的出口 IP；需要配置接收端时，点击蓝色的“查看白名单 IP”，再将显示的地址加入目标服务器白名单。

如果页面显示尚未公布出口 IP，请联系 YundaDesk 支持，不要自行放开所有来源。页面可能同时显示多个 IP，应全部加入白名单。

## 验证请求

请在目标系统验证 YundaDesk 提供的签名和时间戳，并使用事件 ID 或投递 ID 做幂等处理。不要仅依赖来源 IP 作为身份验证。

Custom API 的公网入站地址以产品页面显示为准。重复提交同一条已签名的回执不会重复更新投递状态。

## 排查投递失败

先在对应的 Custom API 或事件推送页面查看投递状态和错误类型：

- 套餐或额度限制：检查当前套餐和用量。
- 地址或域名被拒绝：检查 HTTPS、端口、域名和 URL 内容。
- 连接超时或目标不可用：确认目标服务在线，并允许所有已公布出口 IP。
- 签名失败：重新核对当前密钥；轮换后确保目标系统已使用新密钥。
- Pull 返回 401：检查 Channel Key、签名密钥、本机时间，以及每次请求是否使用了新的 Nonce。
- Pull 返回 409：仅 `CUSTOM_API_PULL_BUSY` 可在等待后重试；其他 409 先确认渠道仍为 Pull 模式，且没有把本地 offset 改到尚未收到的位置，不要盲目重试。
- Pull 返回 429：按 `Retry-After` 等待后重试，不要提高并发轮询数量。
- 本地接收地址持续失败：Connector 不会推进 offset；恢复本机服务并返回 2xx 后会继续处理。

临时网络或 DNS 故障会进入自动重试。达到最大重试次数后，再按页面提供的重放操作处理。
