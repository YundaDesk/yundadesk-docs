---
title: Connect Telegram
description: Bring Telegram customer messages into the YundaDesk Inbox.
category: Channels
order: 3
updated_at: 2026-08-01
---

# Connect Telegram

After Telegram is connected, messages sent to your Bot enter the YundaDesk Inbox. Your team and AI customer service can reply from the same conversation.

## Before you begin

You need a Telegram Bot created and managed through Telegram's official process, plus the valid credentials requested by the setup page. Never expose credentials in chat, documentation, or screenshots.

## Connect the Bot

1. Open Channels and select Telegram.
2. Enter the Bot details and credentials requested by the page.
3. Save and wait for the channel to become available.
4. Use a different Telegram account to send a test message to the Bot.
5. Reply from the Inbox and confirm that Telegram actually receives it.

To enable automatic AI replies, also enable this Telegram channel under **AI → Reception settings**.

## Acceptance test

Do not rely only on a message bubble in the admin UI. Complete both a human round trip and an AI round trip from the real Telegram client.

## Troubleshooting

If the UI says sent but Telegram receives nothing, inspect delivery details and channel authorization. Repeated AI messages, messages that disappear after refresh, or replies visible only in the admin UI are failures and should be reported with conversation and delivery information.
