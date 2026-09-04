---
title: Channel overview
description: Connect, enable, and maintain customer messaging channels.
category: Channels
order: 1
updated_at: 2026-09-04
---

# Channel overview

Channels are the places where customers contact your business. Once connected, messages from different sources enter the same Inbox and attach to customer profiles.

## See available channels

Open Channels to see what your workspace can connect. Availability may differ by deployment, plan, or integration status. The current page is authoritative.

Channel cards show connection state and required actions. A channel must be fully configured and healthy before it can reliably send and receive messages.

## Complete third-party authorization in a new tab

Keep the original Channels page open when connecting or reconnecting Messenger, Instagram DM, or YouTube. The authorization button opens the provider sign-in and consent flow in a new tab. After you finish or cancel, that tab closes automatically and the original page shows the account or channel confirmation result without a manual refresh.

If no new tab appears, allow pop-ups for the current site and select the authorization button again. When reconnecting, choose the Facebook Page, Instagram professional account, or YouTube channel already attached to that channel. Choosing a different asset fails and leaves the existing channel unchanged.

## When YouTube reports mismatched authorization permissions

If you see “YouTube authorization permissions do not match,” this YouTube authorization was not saved and the current channel configuration is unchanged. Do not keep submitting the same authorization. Recover in this order:

1. Make sure Gmail and any other connected Google channels can be reauthorized, and have the required accounts ready.
2. Open your Google Account's third-party connections, find YundaDesk, and remove its previous access.
3. Return to Channels in YundaDesk, reconnect YouTube, and review the permissions shown on the consent page.
4. Check Gmail and your other Google channels. If authorization is no longer valid, reconnect each one with its original account and repeat the send-and-receive test.

Removing YundaDesk's Google access may require existing Google channels to be reauthorized as well. Contact your workspace administrator before proceeding if you are unsure about the impact.

## Choose a provider when connecting email

After you enter the full email address, the page may suggest a provider from the address domain and its public mail settings. A suggestion is never submitted automatically; confirm the provider before continuing.

If no provider is detected, or the suggestion does not match the service you use, choose one manually. Select **Other mailbox** when unsure, then enter the incoming and outgoing server settings supplied by your provider. Always run the connection test after setup. A successful test is what confirms that the account, authorization method, and server settings work.

## Three checks after connecting

1. **Inbound:** Send a message from the customer side and confirm that it appears in the Inbox.
2. **Human reply:** Reply from the Inbox and confirm that the customer actually receives it.
3. **AI reception:** Open the channel's **Reception settings**, choose the **Reception Agent**, and then start a new customer-side test. Select **Human reception** when the channel should not be bound to an Agent.

## Channels and apps are different

Website, Telegram, and email are messaging channels. Store, CRM, and other business systems are usually connected as apps or plugins. They can provide order, customer, or inventory capabilities without being messaging channels themselves.

## When a channel is unhealthy

Open the channel details and inspect authorization, credentials, and connection state. After reconnecting, repeat both inbound and outbound tests. An “accepted” backend status is not proof of final delivery; verify on the customer side.
