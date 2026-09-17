---
title: Channel overview
description: Connect, enable, and maintain customer messaging channels.
category: Channels
order: 1
updated_at: 2026-09-15
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

## Connect an email channel

Choose one of three entry points when adding an email channel:

- **Gmail:** Connect a Gmail or Google Workspace mailbox with official Google authorization.
- **Microsoft Outlook:** Connect an Outlook or Microsoft 365 mailbox with official Microsoft authorization.
- **Other mailbox:** Enter the mailbox address first, then use the suggested provider or enter the incoming and outgoing server settings supplied by your mailbox provider.

After you enter the full email address, the page may suggest a provider from the address domain and its public mail settings. A suggestion is never submitted automatically; confirm the provider before continuing.

If no provider is detected, or the suggestion does not match the service you use, choose one manually. For an **Other mailbox** account protected by two-step verification, use the provider-generated app password or authorization code instead of the normal sign-in password. Always run the connection test and verify both inbound and outbound mail after setup.

## Three checks after connecting

1. **Inbound:** Send a message from the customer side and confirm that it appears in the Inbox.
2. **Human reply:** Reply from the Inbox and confirm that the customer actually receives it.
3. **AI reception:** Open the channel's **Reception settings**, choose the **Reception Agent**, and then start a new customer-side test. Select **Human reception** when the channel should not be bound to an Agent.

## Configure reception

Expand **Reception settings** in the channel configuration and choose the **Reception Agent**. A disabled Agent can remain bound, but only receives new conversations after it is enabled.

Under **Human assignment**, use **Auto-assign conversations** to control automatic assignment and **Receiving members** to choose workspace agents or selected members. When auto-assignment is off, human conversations queue for an agent to pick up.

Leaving **Receiving members** empty or clearing all selections uses agents across the entire workspace. Selecting specific members limits the receiving pool to those members. Automatic assignment still requires agents to be online, accepting conversations, and below their capacity limit. The same receiving pool applies when AI hands a conversation over to a human.

Changes save automatically; you can also click **Save**. Wait for the saved status before leaving. If saving fails, keep your selection and click **Save** to retry. Collapsed sections retain a summary of their current settings.

## Set the Widget appearance

Open **Widget appearance** on a website channel. The current workspace brand name appears here; select **Change workspace brand name** to open Branding settings.

On Free, launcher icon choices and the **Hide Powered by YundaDesk** switch remain visible but disabled, with an **Unlock with Starter** hint. Starter and higher plans can select an icon and turn on the switch to hide attribution on both the Widget home and conversation screens. Turn it off to restore attribution.

Changes save automatically. Refresh after saving to confirm the setting, and check the preview. Existing channels keep attribution by default; downgrading to Free restores it.

## Channels and apps are different

Website, Telegram, and email are messaging channels. Store, CRM, and other business systems are usually connected as apps or plugins. They can provide order, customer, or inventory capabilities without being messaging channels themselves.

## When a channel is unhealthy

Open the channel details and inspect authorization, credentials, and connection state. After reconnecting, repeat both inbound and outbound tests. An “accepted” backend status is not proof of final delivery; verify on the customer side.
