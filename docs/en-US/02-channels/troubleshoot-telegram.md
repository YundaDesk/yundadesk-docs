---
title: Troubleshoot Telegram
description: Diagnose missing Telegram inbound messages and undelivered replies.
category: Channels
order: 8
updated_at: 2026-08-01
---

# Troubleshoot Telegram

Separate the inbound, answer-generation, and delivery stages so an AI issue is not confused with a Telegram issue.

## The customer message is missing

Check that the Telegram channel is enabled, the bot credential remains valid, and the customer is messaging the correct bot.

## The Inbox has the message but AI does not reply

Check whether Telegram is enabled for AI reception, the conversation allows AI reception, relevant knowledge or skills are available, and AI usage is available.

## The Inbox has a reply but Telegram does not

Inspect the delivery state and failure log. Delivery succeeds only when the real Telegram client receives the message; a temporary Inbox bubble is not proof.

## Information to provide support

When contacting support, provide the workspace, channel name, customer name, time, and failure state. Never send the bot secret.
