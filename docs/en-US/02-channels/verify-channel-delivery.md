---
title: Verify real channel delivery
description: Test inbound messages, replies, and delivery from a real customer client.
category: Channels
order: 6
updated_at: 2026-08-01
---

# Verify real channel delivery

A Connected status only proves that configuration was saved. Complete a two-way test from a real customer client before going live.

## Test the channel

1. Send a unique message from a real website visitor or channel client.
2. Confirm that the Inbox shows the correct conversation, customer, and channel.
3. Send a human reply and verify receipt in the customer client.
4. Enable AI reception for the conversation and ask a question covered by the knowledge base.
5. Confirm that one AI reply is generated and delivered to the customer client.

## Acceptance criteria

A reply visible in the Inbox is not proof of delivery. The customer client must receive it, the delivery state must be valid, and the message must remain after refresh.

## If the test fails

If the test fails, record the channel, customer, time, and delivery state. Check credentials and channel state before reviewing answer details or the displayed failure reason.
