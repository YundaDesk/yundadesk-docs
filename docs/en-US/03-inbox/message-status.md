---
title: Understand message status
description: Distinguish between saved, accepted, delivered, and failed messages.
category: Inbox
order: 5
updated_at: 2026-08-01
---

# Understand message status

An Inbox message may be saved before it is delivered asynchronously through a channel.

## Common states

- **Processing:** Generation or delivery is still running. Do not send a duplicate.
- **Accepted:** The request entered the delivery path but may not have reached the customer.
- **Delivered or sent:** The channel processed the message. Spot-check important messages in the real client.
- **Failed:** Delivery did not complete and requires investigation.

## After refresh

A message must still appear after refresh to count as saved. Its order should remain stable when the reply finishes loading.

## Handle failures

Before retrying, open the delivery details to determine whether permissions, the channel, content safety, or an external platform caused the failure.
