---
title: 连接 LINE
description: 用 Channel ID 和 Channel Secret 把 LINE 官方账号的客户消息接入 YundaDesk 工作台。
search_terms: 接入 LINE 官方账号, LINE Messaging API 接入, LINE Channel ID, LINE Webhook 设置
category: 渠道
order: 11
updated_at: 2026-09-26
---

# 连接 LINE

连接后，客户在 LINE 上发给官方账号的一对一消息会进入 YundaDesk 工作台，团队和 AI 客服可以在同一会话中回复。

## 连接前准备

- 一个 LINE 官方账号，以及可以管理它的 LINE Official Account Manager 登录权限。
- 在 LINE Official Account Manager 中打开“设定 → Messaging API”，启用 Messaging API。启用后，同一页面会显示 Channel ID 和 Channel Secret。

Channel ID 是一串数字。不要填写以 U 开头的 ID：LINE 后台显示的“Your user ID”是你本人的账号 ID，不是官方账号的标识。不要在聊天、文档或截图中公开 Channel Secret。

## 连接步骤

1. 打开“渠道”，选择 LINE。
2. 填写 Channel ID 和 Channel Secret，点击保存。系统会先向 LINE 验证，验证失败时不会保存。验证通过后，“LINE 官方账号”会显示账号名称和 LINE ID，请确认这是你要接入的账号。
3. 点击“启用”。
4. 复制页面上“入站 Webhook URL”中的地址，粘贴到 LINE Official Account Manager“设定 → Messaging API”的 Webhook 网址并保存。
5. 在“设定 → 回应设定”中开启 Webhook。建议同时关闭自动回应讯息和加入好友的欢迎讯息，避免客户收到重复回复。
6. 回到 YundaDesk，点击“测试连接”。通过后，渠道状态会变为“已连接”。
7. 用 LINE 给官方账号发一条消息，确认它出现在工作台；再从工作台回复，确认 LINE 上收到。

需要 AI 自动回复时，在渠道的“接待设置”中选择负责接待的 Agent。

LINE 渠道的设置不会自动保存，修改后请点击“保存”。有未保存的更改时，需要先保存，再测试连接。

## 状态说明

- **待配置**：渠道还没有通过 LINE 验证，或还没有确认 LINE 能把消息推送到 YundaDesk。页面会提示下一步，完成后点击“测试连接”。
- **连接失败**：LINE 拒绝了已保存的 Channel ID 或 Channel Secret，或该官方账号已接入其他渠道。按页面提示重新填写，或处理重复的渠道。
- **已连接**：测试连接已通过，或已经收到过客户消息。

一个 LINE 官方账号只能接入一个渠道。LINE 的 Webhook 网址同一时间只能指向一个地址；如果该官方账号之前接入过其他客服系统，改为 YundaDesk 的地址后，原系统将不再收到消息。

## 之前已接入的 LINE 渠道

系统会使用已保存的信息，自动为之前接入的渠道完成验证，大多数情况下无需操作。如果渠道显示“待配置”或“连接失败”，并提示重新填写 Channel ID 和 Channel Secret，请按连接步骤重新填写并保存，然后点击“测试连接”。LINE 后台已经填好的 Webhook 网址如果与页面显示的地址一致，不需要修改。

## 验收建议

不要只看后台消息气泡。至少完成一次“LINE 发来消息 → 工作台显示 → 人工回复 → LINE 收到”，需要 AI 接待时再完成一次 AI 回复测试。

## 故障排查

- **提示 Channel ID 应为纯数字**：回到 LINE Official Account Manager“设定 → Messaging API”复制 Channel ID。
- **提示 Channel ID 或 Channel Secret 不正确**：重新复制两项后保存。如果在 LINE 后台重新发行过 Channel Secret，需要填写新的 Channel Secret。
- **提示该 LINE 官方账号已接入其他渠道**：继续使用已有渠道，或先删除原渠道再重新接入。
- **测试连接提示 Webhook 网址不一致**：LINE 后台填写的是其他地址。复制页面上的地址重新填写并保存。
- **测试连接提示 Webhook 未开启**：到“设定 → 回应设定”开启 Webhook。
- **测试连接提示 LINE 无法送达测试消息**：稍后重试；持续失败时联系支持。
- **工作台没有出现客户消息**：确认渠道已启用、测试连接已通过，并且客户是在与官方账号的一对一聊天中发送消息。群组和聊天室中的消息不会进入工作台。
