---
title: Connect WhatsApp
description: Connect a WhatsApp business number through Meta authorization and verify customer message delivery.
search_terms: set up WhatsApp channel, WhatsApp Business API setup, Connect with Meta
category: Channels
order: 5
updated_at: 2026-10-06
---

# Connect WhatsApp

YundaDesk connects WhatsApp through Meta's official authorization window. You do not enter a third-party provider's API Key manually.

## Before you begin

Prepare a Meta account that can manage business assets and a business phone number eligible for WhatsApp Cloud API. Allow the browser to open Meta's authorization window.

## Connect a number

1. Open "Channels", find WhatsApp in the channel market, and click "Add".
2. Wait for connection preparation to finish, then select **Connect with Meta**.
3. Sign in inside the Meta authorization window and follow the prompts to select or create the business account and number.
4. After authorization, the remaining setup completes automatically. The channel stays disabled after creation.
5. Run **Test connection** on the channel settings page, then enable the channel after the check passes.
6. Send a customer-side test message and confirm that it reaches the Inbox. Reply from the Inbox and confirm that the customer actually receives it.

## Reply window

WhatsApp replies are subject to its conversation window. If the Inbox says you cannot reply, follow the notice, wait for the customer to contact you again, or contact YundaDesk support. A connected channel does not mean you can send unsolicited messages to any number at any time.

## Troubleshooting

- **Authorization window does not open:** Allow pop-ups for this site, then retry.
- **Preparation failed, authorization cancelled, or timed out:** Follow the page's retry instructions and check that Meta is reachable. Incomplete authorization is not a connection.
- **Number already connected:** Check the existing channel before attempting a duplicate connection.
- **Reauthorization fails:** Authorize the number already attached to the channel. Reauthorization cannot replace it with a different number.
- **Connection check fails or a message is missing:** Check channel status and Meta account permissions, keep the displayed error, and contact support. A successful connection check still needs a real send-and-receive test.
