---
title: Connect LINE
description: Bring LINE Official Account customer messages into the YundaDesk Inbox with the Channel ID and Channel Secret.
search_terms: set up LINE Official Account, LINE Messaging API setup, LINE Channel ID, LINE webhook settings
category: Channels
order: 11
updated_at: 2026-09-26
---

# Connect LINE

After LINE is connected, one-on-one messages that customers send to your LINE Official Account enter the YundaDesk Inbox. Your team and AI customer service can reply from the same conversation.

## Before you begin

- A LINE Official Account, and permission to manage it in LINE Official Account Manager.
- In LINE Official Account Manager, open **Settings > Messaging API** and enable the Messaging API. The same page then shows the Channel ID and Channel Secret.

The Channel ID contains only digits. Do not enter an ID that starts with U: the "Your user ID" shown in LINE is your personal account ID, not the ID of the official account. Never expose the Channel Secret in chat, documentation, or screenshots.

## Connect the account

1. Open Channels and select LINE.
2. Enter the Channel ID and Channel Secret, then click **Save**. YundaDesk verifies them with LINE first; a failed check saves nothing. After verification, **LINE Official Account** shows the account name and LINE ID. Confirm that it is the account you want to connect.
3. Click **Enable**.
4. Copy the address under **Inbound webhook URL** on the page, paste it into **Webhook URL** under **Settings > Messaging API** in LINE Official Account Manager, and save.
5. Turn on Webhook under **Settings > Response settings**. We also recommend turning off auto-response and greeting messages so customers don't receive duplicate replies.
6. Back in YundaDesk, click **Test connection**. When it passes, the channel status changes to **Connected**.
7. Send a message to the official account from LINE and confirm that it appears in the Inbox. Then reply from the Inbox and confirm that LINE receives it.

To enable automatic AI replies, choose the Agent that serves customers in the channel's **Reception settings**.

LINE channel settings do not save automatically. Click **Save** after making changes. If there are unsaved changes, save them before testing the connection.

## Channel status

- **Needs setup**: LINE has not verified the channel yet, or YundaDesk has not yet confirmed that LINE can deliver messages to it. Follow the prompt on the page, then click **Test connection**.
- **Connection failed**: LINE rejected the saved Channel ID or Channel Secret, or the official account is already connected to another channel. Enter the details again as prompted, or resolve the duplicate channel.
- **Connected**: A connection test has passed, or a customer message has been received.

One LINE Official Account can be connected to only one channel. LINE sends webhooks to a single Webhook URL at a time. If the official account was previously connected to another customer service system, that system stops receiving messages once you switch to the YundaDesk address.

## LINE channels connected earlier

YundaDesk uses the saved details to verify channels that were connected earlier, so most of them need no action. If a channel shows **Needs setup** or **Connection failed** and asks you to enter the Channel ID and Channel Secret again, follow the steps above to enter and save them, then click **Test connection**. If the Webhook URL in LINE already matches the address on the page, you don't need to change it.

## Acceptance test

Do not rely only on a message bubble in the admin UI. Complete at least one round trip from LINE: a customer message appears in the Inbox, and a human reply arrives in LINE. If AI serves this channel, also complete one AI reply test.

## Troubleshooting

- **The Channel ID must contain only digits**: Copy the Channel ID again from **Settings > Messaging API** in LINE Official Account Manager.
- **The Channel ID or Channel Secret is incorrect**: Copy both again and save. If the Channel Secret was reissued in LINE, enter the new one.
- **The LINE Official Account is already connected to another channel**: Keep using the existing channel, or delete it before connecting again.
- **Test connection reports a Webhook URL mismatch**: LINE is set to another address. Copy the address on the page, enter it again, and save.
- **Test connection reports that Webhook is turned off**: Turn it on under **Settings > Response settings**.
- **Test connection reports that LINE could not deliver a test message**: Try again later. Contact support if it keeps failing.
- **Customer messages do not appear in the Inbox**: Confirm that the channel is enabled, the connection test passed, and the customer is messaging the official account in a one-on-one chat. Messages from groups and multi-person chats do not enter the Inbox.
