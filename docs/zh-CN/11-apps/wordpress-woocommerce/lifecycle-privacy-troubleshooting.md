---
title: 停用、解绑、卸载和使用隐私工具
description: 安全管理 YundaDesk 插件生命周期、WordPress 隐私请求、重新授权与常见故障。
category: 应用与集成
order: 5
updated_at: 2026-08-05
---

# 停用、解绑、卸载和使用隐私工具

停用、解绑和删除插件的效果不同。请根据你是要暂时暂停、迁移站点还是彻底移除集成，选择对应操作。

## 区分各项生命周期操作

| 操作 | WordPress Widget | WooCommerce 增强 | 本地连接信息 |
|---|---|---|---|
| 停用 YundaDesk | 停止加载 | 暂停同步与 YundaDesk 创建的事件 | 保留，便于恢复 |
| 解绑站点 | 停止加载 | 暂停并撤销 YundaDesk 连接 | 解绑完成后移除 |
| 删除插件 | 停止加载 | 删除插件拥有的事件配置 | 删除插件 options 与临时数据 |
| 仅停用 WooCommerce | 继续工作 | 暂停 | WordPress 连接保留 |

要解绑站点，请打开**设置 → YundaDesk**，选择解绑操作，并在收到成功确认后再删除插件。如果曾授权 WooCommerce，还需要打开**WooCommerce → 设置 → 高级 → REST API**，在解绑后删除 YundaDesk key。

解绑一个站点不会影响同一 YundaDesk 工作区中的其他 WordPress 站点。

## 导出个人数据

1. 在 WordPress 后台打开**工具 → 导出个人数据**。
2. 输入已经核实身份的请求者 email。
3. 使用 WordPress 标准流程发送或确认请求。
4. WordPress 将请求标记为已确认后，生成导出文件。

YundaDesk exporter 只返回与当前连接站点相关的客服数据，不会包含同一客户在其他连接站点中独立产生的数据。

## 删除个人数据

1. 打开**工具 → 删除个人数据**。
2. 输入已经核实身份的请求者 email。
3. 完成 WordPress 标准确认流程。
4. 执行删除，并查看每个参与插件返回的结果。

YundaDesk eraser 只作用于当前站点连接。远程删除无法完成时会报告为未完成，管理员可以重试。站点管理员仍需核实请求者，并判断是否因法律义务需要保留部分数据。

![WordPress 个人数据导出与删除工具](/help/assets/docs/wordpress/zh/privacy-tools.jpg "为当前连接站点使用 WordPress 隐私工具")

## 将站点迁移到其他域名

迁移前先在旧地址解绑 YundaDesk。WordPress 改用新的 HTTPS origin 后，打开**设置 → YundaDesk**重新连接。不要重复使用旧配对链接，也不要在不同 origin 之间复制连接值。

## 故障排查

### Widget 没有出现

- 在**设置 → YundaDesk**确认站点状态为**已连接**。
- 使用公开页面测试，不要在 WordPress 后台、登录页、Feed 或 REST 响应中测试。
- 连接后清除页面缓存与 CDN 缓存。
- 确认站点内容安全策略允许[数据和权限](./data-and-permissions.md)中列出的 YundaDesk API 与 Widget loader。

### 未检测到 WooCommerce

- 确认 WooCommerce 在同一个 WordPress 站点中处于启用状态。
- 将 WooCommerce 升级到 8.2 或更高版本。
- 重新加载**设置 → YundaDesk**。

### 显示需要重新授权

再次选择 WooCommerce 只读连接并批准 **Read**。不要自行创建 Consumer Key 或 Consumer Secret 后粘贴到 YundaDesk。

### 同步或事件状态异常

打开**设置 → YundaDesk**刷新状态，并使用页面提供的恢复操作。如果问题持续存在，请在联系 [YundaDesk 支持](https://yundadesk.com/contact/)前记录站点地址、大致时间、YundaDesk 插件版本、WordPress 版本、WooCommerce 版本和页面显示的非敏感错误。不要在工单中发送密码、API key、客户地址或完整订单记录。
