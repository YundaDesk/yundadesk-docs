---
title: Connect WeChat Customer Service
description: Authorize an enterprise, assign customer service accounts, and bring customer messages into the YundaDesk Inbox.
category: Channels
order: 4
updated_at: 2026-08-06
---

# Connect WeChat Customer Service

After the connection is enabled, messages sent to an official enterprise WeChat Customer Service account enter the YundaDesk Inbox. Agents and AI customer service can reply while the conversation remains eligible under WeCom rules.

WeChat Customer Service is not a regular WeCom employee account. Private chats between employees and external contacts, customer group messages, and internal chats are not included in this channel.

## Before you begin

You need:

- YundaDesk workspace administrator access;
- a WeCom administrator who can install third-party applications and manage customer service accounts;
- at least one WeChat Customer Service account created in the WeCom admin console;
- a personal WeChat account for real delivery testing; and
- WeChat Customer Service visible on the current workspace's Channels page and included in the current plan.

## Understand the complete flow

| Stage | Where to perform it | Completion signal |
|---|---|---|
| Create accounts | WeCom admin console | At least one WeChat Customer Service account exists |
| Install the app | YundaDesk → Channels → WeChat Customer Service | Enterprise authorization shows **Connected** |
| Grant management | WeCom → WeChat Customer Service → Manage conversation messages through the API | The account shows **Manageable** in YundaDesk |
| Import accounts | YundaDesk → WeChat Customer Service | Each account becomes an independent channel |
| Enable and verify | YundaDesk Inbox + personal WeChat | Customer messages and agent replies are delivered both ways |

The interactive demo above previews the YundaDesk authorization, synchronization, and import steps. The screenshots below show the corresponding WeCom admin pages. WeCom may display these pages in Chinese depending on the administrator's locale.

## 1. Create WeChat Customer Service accounts in WeCom

Sign in to the WeCom admin console as an administrator, open **Application Management**, and select **WeChat Customer Service**. Confirm that the application is enabled and review its visibility scope.

![WeChat Customer Service overview in the WeCom admin console](/help/assets/docs/wecom-kf/shared/02-wechat-customer-service-overview.png)

Select **Create account**, then set the avatar and customer-facing name. An enterprise can create multiple accounts. Each account imported into YundaDesk later becomes an independent channel.

![Create a WeChat Customer Service account and configure reception](/help/assets/docs/wecom-kf/shared/03-create-service-account.png)

WeCom manages its native bot, native human receptionists, welcome message, and automatic conversation end time. These are not YundaDesk agent settings. If a native WeCom agent takes over a conversation, YundaDesk continues to show synchronized messages but makes that conversation read-only.

## 2. Authorize the enterprise in YundaDesk

1. Open **Channels** in YundaDesk.
2. Select **WeChat Customer Service**, then select **Authorize in WeCom**.
3. Complete the installation as a WeCom administrator and approve the enterprise, member, and WeChat Customer Service permissions shown on the page.

![Third-party application installation authorization in WeCom](/help/assets/docs/wecom-kf/shared/01-install-authorization.png)

**Dedicated support for you** is an optional WeCom service-provider contact setting. It does not determine whether customer service messages can enter YundaDesk. After approval, return to YundaDesk and wait until the enterprise authorization shows **Connected**.

## 3. Grant account management permission in WeCom

Enterprise authorization lets YundaDesk discover customer service accounts. YundaDesk can manage and exchange messages only for accounts that the enterprise explicitly assigns to it.

In the WeCom admin console, open **Application Management → WeChat Customer Service**, scroll to the section for managing conversation messages through the API, and select the option to authorize a third-party application.

![Entry for managing WeChat Customer Service messages through the API](/help/assets/docs/wecom-kf/shared/04-api-management-entry.png)

Open the action menu for the YundaDesk application and select the option to authorize customer service accounts.

![Authorize customer service accounts for YundaDesk in WeCom](/help/assets/docs/wecom-kf/shared/06-authorize-third-party-app.png)

Select the accounts that YundaDesk should manage and confirm. If WeCom allows only one third-party application to manage an account at a time, remove the previous management relationship first.

![Select WeChat Customer Service accounts for YundaDesk](/help/assets/docs/wecom-kf/shared/07-select-service-accounts.png)

WeCom menu labels can change. Confirm that you are assigning **WeChat Customer Service accounts**, not regular members, customer contacts, or customer group permissions.

## 4. Synchronize, select, and import accounts

Return to WeChat Customer Service in YundaDesk and select **Sync accounts**. Immediately after enterprise authorization—but before API management permission is assigned—an account appears as **No management permission**.

![YundaDesk discovers accounts that do not yet have management permission](/help/assets/docs/wecom-kf/shared/05-discover-service-accounts.png)

After granting permission in WeCom, synchronize again. The account changes to **Manageable**. Select the accounts to connect, then select **Import selected**.

![Select and import manageable customer service accounts in YundaDesk](/help/assets/docs/wecom-kf/shared/08-import-service-accounts.png)

Importing an account:

- creates one independent YundaDesk channel for that WeChat Customer Service account;
- keeps conversation sources separated by account;
- allows messages for the account to enter the shared Inbox; and
- allows agents or AI to reply while the conversation remains eligible under official rules.

Every imported account is disabled by default. Importing alone does not start receiving new messages or automatic replies. Open and enable each channel that should go live. To use automatic AI reception, also select that channel in the AI customer service reception settings.

## 5. Verify a real message round trip

1. In the WeCom admin console, get the entry link or QR code for customer service account A.
2. Open it from a personal WeChat account and send a test message with a unique marker.
3. In the YundaDesk Inbox, confirm that the new conversation shows the correct WeChat Customer Service account as its source.
4. Send a human reply from the Inbox and confirm that it arrives in the personal WeChat account.
5. If AI reception is enabled, send another customer message and verify that the AI reply is delivered.
6. Repeat the test with account B and confirm that the two account sources do not get mixed.

A **Sent** state in the admin UI is not proof of final delivery. Verify the message in the customer's WeChat client and watch for a later asynchronous failure state.

## Connection boundaries and reply limits

| Item | Behavior after connection |
|---|---|
| Message entry | Only messages sent to imported WeChat Customer Service accounts are included |
| Customer-facing identity | Replies always use the selected customer service account identity, not an individual YundaDesk agent |
| Multiple accounts | Each customer service account becomes an independent channel and conversation source |
| Regular WeCom private chats | Not available to YundaDesk |
| WeCom native human reception | Messages can remain visible, but YundaDesk becomes read-only after a native agent takes over |

The customer must initiate a WeChat Customer Service conversation. Regular API replies are also subject to these rules:

- replies are allowed only within 48 hours of the customer's latest message;
- at most five replies can be sent in the current reply window;
- a new customer message recalculates the reply window and available count; and
- YundaDesk cannot continue regular sending after a native WeCom agent takes over, the session ends, or the account becomes unavailable.

| Inbox state | Available action |
|---|---|
| Reply available | An agent or AI can send within the remaining allowance |
| Waiting for WeCom native reception | Review messages and wait for the official state to change |
| WeCom native agent is serving | Review synchronized messages in read-only mode |
| Session ended | Wait for the customer to start a new conversation |
| Reply window expired or limit reached | Wait for a new customer message before replying |

Assigning a YundaDesk agent does not change the native WeCom reception state. Customers always see the selected WeChat Customer Service account as the sender.

## Supported messages

YundaDesk can display inbound text, commonly used media, and selected structured cards. Outbound messages support text, images, voice, video, and files. Whether a reply can be sent still depends on the current conversation state, reply window, and official limits.

When the official profile provides a usable WeChat nickname, the Inbox shows it first. Otherwise, YundaDesk uses **WeChat customer #identifier** as a stable fallback.

## Synchronize, reauthorize, or unlink

- **Sync accounts:** Refresh manageable accounts and account state without enabling channels.
- **Reauthorize:** Restore an enterprise connection after authorization is revoked or expires; channels remain disabled until you enable them.
- **Unlink from YundaDesk only:** Stop local sending and receiving and remove the mapping while keeping the official account in WeCom.
- **Also delete the official account:** Delete the account and its entry points from WeCom. YundaDesk cannot restore it.

Unless you explicitly need to delete the official account in WeCom, prefer unlinking it from YundaDesk only.

## Troubleshooting

### No accounts appear after authorization

Confirm that at least one WeChat Customer Service account exists in WeCom, then select **Sync accounts** in YundaDesk. If the list remains empty, check that the enterprise authorization is still valid.

### An account has no management permission

Ask the WeCom administrator to grant the YundaDesk application access to that account, then synchronize again. If another third-party application already manages it, resolve the previous relationship first.

### Customer messages do not enter the Inbox

Confirm that the customer used the account's entry link or QR code rather than sending a private message to a regular WeCom employee. Also confirm that the imported channel is enabled.

### The reply composer is read-only

Read the reason shown in the Inbox. Common causes include native WeCom human reception, an ended session, an expired 48-hour window, or all five replies being used.

### A message is sent and later fails

WeCom can report an asynchronous failure after accepting a send request. Use the final Inbox state and the customer's WeChat client as the source of truth. Reauthorize, wait for a new customer message, or retry a retryable message as instructed by the UI.
