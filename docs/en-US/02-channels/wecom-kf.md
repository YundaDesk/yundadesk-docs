---
title: Connect WeChat Customer Service
description: Authorize an enterprise, assign customer service accounts, and bring customer messages into the YundaDesk Inbox.
category: Channels
order: 4
updated_at: 2026-08-18
---

# Connect WeChat Customer Service

After the connection is enabled, messages sent to an official enterprise WeChat Customer Service account enter the YundaDesk Inbox. Agents and AI customer service can reply while the conversation remains eligible under WeCom rules.

WeChat Customer Service is not a regular WeCom employee account. Private chats between employees and external contacts, customer group messages, and internal chats are not included in this channel.

## One enterprise can connect to only one workspace

For the same YundaDesk third-party application, an enterprise can be connected to only one YundaDesk workspace at a time. This is an enterprise-level connection, not a connection for one customer service account.

- The same workspace can reauthorize the same enterprise.
- If another workspace scans the authorization code for that enterprise, it sees only **This enterprise is already connected to another workspace**. The connection is not transferred, and the original workspace is not disclosed.
- An administrator of the original workspace must complete the enterprise disconnect and data cleanup before another workspace can connect the enterprise.
- If the current workspace is connected to enterprise A, disconnect enterprise A before connecting enterprise B.

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
| Enable accounts | YundaDesk → WeChat Customer Service | Each selected account becomes an independent channel showing **Enabled / AI replies off** |
| Verify messaging | YundaDesk Inbox + personal WeChat | Customer messages and agent replies are delivered both ways |

The interactive demo above previews the YundaDesk authorization, synchronization, and enablement steps. The screenshots below show the corresponding WeCom admin pages. WeCom may display these pages in Chinese depending on the administrator's locale.

## 1. Create WeChat Customer Service accounts in WeCom

Sign in to the WeCom admin console as an administrator, open **Application Management**, and select **WeChat Customer Service**. Confirm that the application is enabled and review its visibility scope.

![WeChat Customer Service overview in the WeCom admin console](/help/assets/docs/wecom-kf/shared/02-wechat-customer-service-overview.png)

Select **Create account**, then set the avatar and customer-facing name. An enterprise can create multiple accounts. Each account imported into YundaDesk later becomes an independent channel.

![Create a WeChat Customer Service account and configure reception](/help/assets/docs/wecom-kf/shared/03-create-service-account.png)

WeCom manages its native bot, native human receptionists, welcome message, and automatic conversation end time. These are not YundaDesk agent settings. If a native WeCom agent takes over a conversation, YundaDesk continues to show synchronized messages but makes that conversation read-only.

## 2. Authorize the enterprise in YundaDesk

1. Open **Channels** in YundaDesk.
2. Select **WeChat Customer Service**, then select **Authorize in WeCom**. YundaDesk opens authorization in a new tab while the original workspace stays open.
3. Complete the installation as a WeCom administrator and approve the enterprise, member, and WeChat Customer Service permissions shown on the page. The authorization tab returns to YundaDesk when finished, and the original workspace refreshes account status automatically.

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

## 4. Synchronize, select, and enable accounts

Return to WeChat Customer Service in YundaDesk and select **Sync accounts**. Immediately after enterprise authorization—but before API management permission is assigned—an account appears as **No management permission**.

![YundaDesk discovers accounts that do not yet have management permission](/help/assets/docs/wecom-kf/shared/05-discover-service-accounts.png)

After granting permission in WeCom, synchronize again. The account changes to **Manageable**. Select the accounts to connect, then select **Enable selected accounts**.

Enabling selected accounts:

- creates one independent YundaDesk channel for that WeChat Customer Service account;
- keeps conversation sources separated by account;
- allows messages for the account to enter the shared Inbox; and
- enables each channel immediately so agents can reply while the conversation remains eligible under official rules.

AI replies are off by default, so the page shows both **Enabled** and **AI replies off**. To use automatic AI reception, select the channel in the AI customer service reception settings. Channel enablement and AI replies are independent states.

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

## Synchronize, reauthorize, or disconnect

First decide whether you need to act on one customer service account or on the enterprise connection:

| Action | Scope | Releases the enterprise from the workspace |
|---|---|---|
| Sync accounts | Refreshes accounts and management permission without changing channel or AI-reply state | No |
| Reauthorize | Restores an enterprise authorization that cannot be verified in the current workspace | No |
| Unlink one account | Stops that account in YundaDesk while keeping the account in WeCom | No |
| Delete the official account | Deletes that account and its entry points without affecting other accounts in the enterprise | No |
| Disconnect the enterprise | Disables every WeChat Customer Service channel for the enterprise and cleans up connection data | Yes, after cleanup finishes |

**Unlink** and **Delete account** on an individual account page are not an enterprise disconnect. Even if every customer service account is deleted, the enterprise remains connected to the current workspace until the enterprise disconnect below is completed.

### Disconnect the entire enterprise

Only a workspace administrator who also has channel-management permission can perform this action.

1. Open **Channels → WeChat Customer Service** and select **Disconnect enterprise**.
2. Enter the enterprise name as prompted and confirm. YundaDesk immediately disables every WeChat Customer Service channel for the enterprise. Messaging, account synchronization, and new account enablement stop.
3. Ask an enterprise administrator to open **Application Management → Third-party apps → YundaDesk** in the WeCom admin console and select **Delete app**.
4. Return to YundaDesk, select **I deleted it — check status**, and confirm again that the app was deleted.
5. If WeCom still reports the app as authorized, the page continues waiting and cleanup does not begin. After removal is confirmed, YundaDesk shows **Disconnecting and cleaning up data**.
6. Wait until the page shows **Enterprise connection removed**. Only then can this enterprise connect to the current workspace or another workspace.

Before the app is deleted in WeCom, you can select **Cancel disconnect**. YundaDesk verifies the authorization and restores only channels that were enabled when the disconnect started. Channels that were already disabled stay disabled. A disconnect cannot be cancelled after the WeCom authorization is no longer valid.

### When the enterprise revokes access in WeCom

If an enterprise administrator deletes the YundaDesk app directly in WeCom, YundaDesk disables every WeChat Customer Service channel as soon as it receives the revocation notice and begins cleanup. Until cleanup finishes, the enterprise remains assigned to the current workspace and cannot connect to another workspace.

### What each connection state means

| Page state | Meaning and next step |
|---|---|
| Not connected | This workspace has no enterprise connection and can start authorization |
| Connected | Authorization is valid; you can sync or enable accounts, reauthorize, or start an enterprise disconnect |
| Delete the app in the WeCom admin console | The disconnect has started and all channels are disabled; delete the app as instructed, then check its status |
| Reauthorization required | Authorization cannot be verified and all channels are disabled, but the enterprise remains assigned to this workspace; reauthorize with the same enterprise or start a disconnect |
| Disconnecting and cleaning up data | Revocation is confirmed and cleanup is running; authorization and account enablement are unavailable |
| Enterprise connection removed | Cleanup is complete and the enterprise assignment has been released; authorization can start again |

If cleanup temporarily fails, the page continues to show that cleanup is incomplete and YundaDesk retries safely. It does not report a completed disconnect or release the enterprise to another workspace before cleanup succeeds.

### What happens to data after cleanup

An enterprise disconnect removes or anonymizes identifiable data created through that WeChat Customer Service connection, including customer service account details, WeChat customer identities, channel message content, and WeChat Customer Service attachments. Conversation and aggregate reporting structure may remain without identities or message content so reports stay consistent; message positions show a standard cleaned-data notice.

If the same customer also contacted you through the website, email, or another channel, those other identities and histories are not removed by the WeChat Customer Service enterprise disconnect. **Enterprise connection removed** means both cleanup and release of the enterprise assignment have completed.

## Troubleshooting

### “This enterprise is already connected to another workspace”

Scanning the authorization code again does not transfer the enterprise. Ask an administrator of the original workspace to complete the enterprise disconnect, then wait for cleanup to finish before trying again. For privacy, the message does not identify the original workspace.

### The enterprise disconnect keeps waiting for app deletion

Confirm that an enterprise administrator deleted YundaDesk under **Application Management → Third-party apps**. Removing management permission from one customer service account is not enough. After deleting the app, return to YundaDesk and select **I deleted it — check status**.

### The page remains on cleanup

If cleanup fails, YundaDesk keeps every channel disabled and retries without releasing the enterprise connection early. Refresh the page later. Contact YundaDesk Support if the state does not change for an extended period.

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
