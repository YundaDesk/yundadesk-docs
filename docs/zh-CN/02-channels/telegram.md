---
title: 连接 Telegram
description: 把 Telegram 客户消息接入 YundaDesk 工作台。
search_terms: 接入 Telegram 机器人渠道, 配置 Telegram Bot, Telegram 渠道接入
category: 渠道
order: 3
updated_at: 2026-08-01
---

# 连接 Telegram

连接 Telegram 后，客户给 Bot 发送的消息会进入 YundaDesk 工作台，团队和 AI 客服可以从同一会话回复。

## 连接前准备

你需要一个通过 Telegram 官方方式创建并管理的 Bot，以及页面要求的有效凭证。不要在聊天、文档或截图中公开凭证。

## 连接步骤

1. 打开“渠道”，选择 Telegram。
2. 按页面提示填写 Bot 信息和凭证。
3. 保存并等待渠道状态变为可用。
4. 用另一个 Telegram 账号给 Bot 发一条测试消息。
5. 在工作台回复，确认 Telegram 端真实收到。

需要 AI 自动回复时，再进入“AI → 接待设置”启用这个 Telegram 渠道。

## 验收建议

不要只看后台消息气泡。至少完成一次“Telegram 发入站消息 → 工作台显示 → 人工回复 → Telegram 收到”和一次 AI 回复测试。

## 故障排查

如果后台显示已发送但 Telegram 没有收到，查看消息投递详情和渠道授权状态。重复生成 AI 内容、消息刷新后消失或只在后台可见都不算成功，应保留会话和投递信息后联系支持。
