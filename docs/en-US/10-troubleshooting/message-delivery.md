---
title: Message failed or the customer did not receive it
description: Distinguish backend acceptance, channel delivery, and final customer receipt.
category: Troubleshooting
order: 2
updated_at: 2026-08-01
---

# Message failed or the customer did not receive it

A message normally travels through YundaDesk, a channel adapter, and an external platform. A message bubble or an “accepted” status does not always mean the customer received it.

## Troubleshooting order

1. Open message details and review send, delivery, and failure states.
2. Check that the channel is online and authorization has not expired.
3. Confirm that the recipient identity and conversation belong to the correct channel.
4. Retry once from the Inbox; avoid repeated clicks that could create duplicates.
5. Verify the result in Telegram, the website widget, or the actual customer client.

## Common symptoms

- **Visible before refresh, missing afterward:** A temporary UI message may not have been persisted. This is not a successful send.
- **Marked sent, not received:** Check final channel delivery and external platform restrictions.
- **Several AI replies to one message:** Stop AI reception for that conversation and report the message times and answer details.
- **A Yuna action times out:** Check whether a real side effect already occurred before confirming again.

## What to provide when contacting support

When contacting support, provide the workspace, channel, conversation, time, message summary, and delivery details. Never send a Bot Token, API key, or sensitive customer content.
