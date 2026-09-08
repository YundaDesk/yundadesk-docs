---
title: Connect a personal-account cloud device
description: Connect your own social account in preview and understand login, status, and risk.
category: Channels
order: 5
updated_at: 2026-09-09
---

# Connect a personal-account cloud device

If **Personal account hosting (Engineering Preview)** is available in your workspace, you can connect one of the social account types shown on the page to the YundaDesk Inbox. This is different from the platform's official business channel and is intended for controlled testing after you understand the account risk.

## Before you begin

- Make sure you can manage channels and that you own or are authorized to manage the account.
- Have the phone or authenticator needed for QR scanning, verification codes, a PIN, or two-step verification.
- Review the account types, network egress choices, and capabilities currently shown on the Channels page. They can differ by account type.
- An X personal account requires assistance from YundaDesk Support to complete the protected sign-in step.

Never put account cookies, session files, verification codes, or proxy passwords in chat, support-ticket text, or screenshots. Enter requested information only in the designated secure product field.

## Understand the risk

Personal account hosting is not the corresponding platform's official business API. The platform may restrict personal accounts, require a new login, change available behavior, or interrupt the connection. YundaDesk cannot guarantee that an account will not be throttled or restricted.

Before connecting, you must read and accept the current risk notice shown in the product. YundaDesk connects only an account you provide; it does not buy, rent, or resell accounts.

Personal account hosting does not support broadcasts, segment sends, or automated proactive outreach. AI auto reception runs only after the device signs in and you explicitly enable it for that device.

## Connect the account

1. Open **Channels** and find **Personal account hosting (Engineering Preview)**. If the section is absent, the preview is not available to this workspace.
2. Select an account type currently shown on the page.
3. Read the risk notice and confirm that you are using your own account.
4. Select an available network egress option. For a custom static proxy, enter its protocol, host, port, and username and password if required. You do not need to enter an expected IP region or provide residential-type evidence. You are responsible for choosing the proxy source and region and assessing account-use risks.
5. Decide whether to sync message history. History is optional; use the support and limits shown on the page.
6. Create the device and complete the displayed QR, pairing, verification-code, PIN, two-step verification, or confirmation challenge.
7. Wait for the status to become **Online**, then use another account to complete one real inbound message and one human reply.

After creation, wait while the device prepares its connection. If multiple login methods are offered, choose a QR code or phone number. Enter the full phone number with its country code, followed by the verification code and two-step verification password if requested. Enter a LINE PIN on your phone, not back into the web page. If a QR code expires, restart login and use the new code.

After you submit a verification code, PIN, password, or proxy password, the page does not reveal it again. If submission fails, obtain or enter a new value instead of trying to recover it from browser history or screenshots.

## Understand device status

| Status | Meaning and action |
|---|---|
| Connecting | The device is starting and establishing a connection. Wait for the page to update. |
| Online | You can test supported human messaging. |
| Offline / Reconnecting | The connection is interrupted. Wait for automatic recovery, then use the reconnect action if prompted. |
| Expired | The login is no longer valid and must be completed again. |
| Faulted | Review the safe error shown on the page. Contact YundaDesk Support if recovery fails. |
| Deleting | New outbound messages have stopped. The occupied slot is released after deletion completes. |

Account suspension, throttling, or protocol changes by the third-party platform are not counted as normal YundaDesk availability, but the page should expose a device status or safe error that you can act on.

## History and AI behavior

Imported history does not create new-message notifications or trigger AI replies, learning, or automated outreach. Not every account type supports history; rely on the capability shown in the connection flow.

AI auto reception is controlled separately for each device. For the first validation, leave it off, complete stable human round trips and a reconnect test, and then decide whether to enable it for your use case.

## Change a proxy or retry a connection

In device details, open **Change device proxy**, enter the full new protocol, host, port and
required credentials, then select **Update proxy and reconnect**. The device disconnects and
reconnects; its previous password is never shown. A submitted change does not mean the device
has connected or signed in successfully. Check its status. If the result is uncertain, refresh
the status first; re-enter the complete configuration only if another attempt is needed.

## Delete a device

Open the device details, select **Delete cloud device**, and confirm. Do not continue sending after submission. The occupied slot is released when deletion finishes; do not create another device for the same account to bypass the pending state.

## Troubleshooting

- Expired QR or verification code: select **Start / restart login** and complete the new challenge.
- Stuck in Connecting: check that the proxy host, port and authentication details are correct and the proxy is reachable, then reconnect.
- Expired status: sign in again and do not repeatedly submit an old code.
- Unknown send result: check the actual social app before sending again to avoid a duplicate message.
- No managed egress or account type on the page: that option is currently unavailable. Use another option shown on the page or contact YundaDesk Support.
- X sign-in cannot continue: ask YundaDesk Support to complete the protected connection. Do not send raw cookies or session files.

If the device still cannot recover, provide the account type, page status, approximate time, and safe error code shown in the UI. Never attach verification codes, passwords, proxy credentials, cookies, or session files.
