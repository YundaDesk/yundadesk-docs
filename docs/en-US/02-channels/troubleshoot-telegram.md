---
title: Troubleshoot Telegram
description: Diagnose missing Telegram inbound messages and undelivered replies.
category: Channels
order: 10
updated_at: 2026-09-17
---

# Troubleshoot Telegram

Separate the inbound, answer-generation, and delivery stages so an AI issue is not confused with a Telegram issue.

## The customer message is missing

Check that the Telegram channel is enabled, the bot credential remains valid, and the customer is messaging the correct bot.

Do not connect the same bot to multiple support channels or other services that receive its messages. If the bot is already connected elsewhere, decide which connection to keep before disabling the unused one. Do not delete conversation history or regenerate the bot secret as a first step. Contact support if you are unsure.

If the bot is already connected, use the existing support channel. Disabling it keeps the connection reserved; it does not let you connect the same bot to another support channel.

After changing the Bot Token, click **Save** to apply it. If credential validation fails, the previous credential stays unchanged. If the save result is unclear, refresh the page to check it. Save a replacement credential for the same bot in its existing channel; create a new channel for a different bot.

A successful **Test connection** only confirms that the credential is valid. Check that a customer message reaches the Inbox and a reply appears in Telegram to confirm that receiving and replying both work.

## Health shows a bot receiving conflict

“Bot receiving conflict” means another service is receiving messages for the same bot, so this channel may miss messages. “Bot webhook is active” means the bot uses another receiving method and this channel cannot currently receive messages.

The system slows down retries and updates the status automatically when receiving resumes. Other channels are unaffected by this conflict. Check channel health: valid credentials alone do not confirm message reception. Check the delivery result of replies already in the Inbox separately.

You do not need to repeatedly save credentials or run connection tests to understand the impact. Those actions do not prove that the receiving conflict has ended.

## The Inbox has the message but AI does not reply

Check whether Telegram is enabled for AI reception, the conversation allows AI reception, relevant knowledge or skills are available, and AI usage is available.

## The Inbox has a reply but Telegram does not

Inspect the delivery state and failure log. Delivery succeeds only when the real Telegram client receives the message; a temporary Inbox bubble is not proof.

## Information to provide support

When contacting support, provide the workspace, channel name, customer name, time, and failure state. Never send the bot secret.
