---
title: Channel overview
description: Connect, enable, and maintain customer messaging channels.
category: Channels
order: 1
updated_at: 2026-08-31
---

# Channel overview

Channels are the places where customers contact your business. Once connected, messages from different sources enter the same Inbox and attach to customer profiles.

## See available channels

Open Channels to see what your workspace can connect. Availability may differ by deployment, plan, or integration status. The current page is authoritative.

Channel cards show connection state and required actions. A channel must be fully configured and healthy before it can reliably send and receive messages.

## Connect an email channel

Choose one of three entry points when adding an email channel:

- **Gmail:** Connect a Gmail or Google Workspace mailbox with official Google authorization.
- **Microsoft Outlook:** Connect an Outlook or Microsoft 365 mailbox with official Microsoft authorization.
- **Other mailbox:** Enter the mailbox address first. YundaDesk uses the address suffix to prefill settings for known providers. If no provider is recognized, enter the incoming and outgoing server settings supplied by your mailbox provider in the next step.

For an “Other mailbox” account protected by two-step verification, use the provider-generated app password or authorization code instead of the normal sign-in password. After connecting, verify both inbound and outbound mail.

## Three checks after connecting

1. **Inbound:** Send a message from the customer side and confirm that it appears in the Inbox.
2. **Human reply:** Reply from the Inbox and confirm that the customer actually receives it.
3. **AI reception:** Open the channel's **Reception settings**, choose the **Reception Agent**, and then start a new customer-side test. Select **Human reception** when the channel should not be bound to an Agent.

## Channels and apps are different

Website, Telegram, and email are messaging channels. Store, CRM, and other business systems are usually connected as apps or plugins. They can provide order, customer, or inventory capabilities without being messaging channels themselves.

## When a channel is unhealthy

Open the channel details and inspect authorization, credentials, and connection state. After reconnecting, repeat both inbound and outbound tests. An “accepted” backend status is not proof of final delivery; verify on the customer side.
