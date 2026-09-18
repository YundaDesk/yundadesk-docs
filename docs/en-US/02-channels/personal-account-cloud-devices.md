---
title: Connect a personal-account cloud device
description: Connect your own social account and understand login, status, and risk.
category: Channels
order: 6
updated_at: 2026-09-19
---

# Connect a personal-account cloud device

If **Personal account hosting** is available in your workspace, you can connect one of the social account types shown on the page to the YundaDesk Inbox. This is different from the platform's official business channel. Understand the account risk before connecting.

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

1. Open **Channels** and find **Personal account hosting** at the bottom of the marketplace, below **Social & Messaging**. If the section is absent, it is not available to this workspace.
2. Select the button at the bottom left of the appropriate card, such as **Host WhatsApp personal account**. Telegram App and Zalo App identify personal-account hosting, not official business channels. These type labels do not rename existing devices.
3. Enter a device name that helps you identify the account.
4. Select an available network egress option. For a custom static proxy, enter its protocol, host, port, and username and password if required. You do not need to enter an expected IP region or provide residential-type evidence. You are responsible for choosing the proxy source and region and assessing account-use risks.
5. Decide whether to sync message history. History is optional; use the support and limits shown on the page.
6. Read and accept the agreement and risk notice, confirm that you are using your own account, then create the device. Complete the displayed QR, pairing, verification-code, PIN, two-step verification, or confirmation step.
7. Wait for the status to become **Online**, then use another account to complete one real inbound message and one human reply.

After creation, wait while the device prepares its connection. If multiple login methods are offered, choose a QR code or phone number. Enter the full phone number with its country code, followed by the verification code and two-step verification password if requested. Enter a LINE PIN on your phone, not back into the web page. Use only the currently valid QR code on the page, not a previously saved code.

After you submit a verification code, PIN, password, or proxy password, the page does not reveal it again. If submission fails, obtain or enter a new value instead of trying to recover it from browser history or screenshots.

## Understand device status

### Login time limit, cancellation, and retry

The Account login section shows the time remaining for the current attempt. Refreshing, switching tabs, reopening the page, or receiving a replacement QR code does not restart the countdown. Verification codes and two-step verification must also be completed within this attempt. Briefly closing the page does not immediately cancel login.

To stop, select **Cancel this login**. After cancellation or expiry, the page hides login codes and shows that the connection is ending. Wait until cleanup finishes and the page allows another login, then select **Start / restart login**. A new attempt does not start automatically.

Ending an incomplete login does not delete the cloud device or proxy configuration, and saved sessions are retained. Once login is confirmed successful, the original login countdown will not stop the signed-in device. If status cannot be confirmed, wait for the page to recover rather than repeatedly submitting or creating duplicate devices.

### Connection and runtime status

“Waiting for runtime resources” means no running instance is available yet; it does not mean your proxy password or account is wrong. After selecting login, “Login request received” or “Login request pending” means you can wait without clicking again. Login starts automatically when ready. While the device proxy connection is being prepared, wait for the result and follow any proxy error shown.

If the login request could not be completed, check device status and start a new request. Being queued or having a request accepted does not mean you are signed in. Complete the challenge and wait for Online status before testing messages.

| Status | Meaning and action |
|---|---|
| Preparing | The device is getting ready. Follow the next step in the login section. |
| Awaiting login | Account authentication is incomplete. Follow the current login step. |
| Online | You can test supported human messaging. |
| Connection issue | A signed-in account has lost its channel connection. Wait for recovery, then follow the instructions. |
| Status unconfirmed | Device status cannot currently be confirmed. Refresh to check; this does not mean the account signed out. |
| Faulted | Review the safe error shown on the page. Contact YundaDesk Support if recovery fails. |
| Stopped | The device is no longer running. If deletion is pending, follow its separate progress notice. |

A running device is not necessarily signed in. QR codes, phone PINs, verification codes and two-step passwords appear in the login section. Complete the current step and wait for the next instruction or confirmed login. Refreshing restores the current valid step without extending its expiry. Telegram may require its two-step password on the web page after scanning; you do not need to disable two-step verification.

After LINE confirms on your phone, wait for the channel page to confirm sign-in. If it reports a rejected login context, sign in again. If it fails again, open **Error details** and share the error code and time with support, never the QR code, PIN or password. If an updated login client is required, contact support instead of repeatedly scanning.

## Check the device network exit

A failed exit check does not mean the account signed out. Follow the reason shown on the page. A **Last successful measurement** is a historical result with its original time, not a successful result for the current check. Checks continue, and a new successful measurement updates the current result.

Open the device in **Channels** and check **Device network exit** for its check status, exit IP, country/region and measurement time. **Check successful** means a valid exit result was obtained, not that the account is signed in. Wait for the first check after creation and a fresh result after changing the proxy. The previous IP is not presented as the current exit after a proxy change. **Check again** does not sign out or restart the device; avoid repeated clicks.

**Region unknown** means the IP's country/region could not be determined. **Check failed** or **Result expired** means no sufficiently fresh measurement is available, not that account login failed. Country/region is an IP-based estimate, not a physical-location guarantee. Rotating proxies can use different IPs for different connections; read the result together with its measurement time.

Account suspension, throttling, or protocol changes by the third-party platform are not counted as normal YundaDesk availability, but the page should expose a device status or safe error that you can act on.

## History and AI behavior

Use **Basic settings** in the device details to edit its name or history-sync option. Select **Save** after changing the name. **Reception settings** is a separate section below it; expand it to view the AI reception switch. Opening it does not hide Basic settings or clear a name you are editing.

Imported history does not create new-message notifications or trigger AI replies, learning, or automated outreach. Not every account type supports history; rely on the capability shown in the connection flow.

AI auto reception is controlled separately for each device. For the first validation, leave it off, complete stable human round trips and a reconnect test, and then decide whether to enable it for your use case.

## Change a proxy or retry a connection

If a signed-in Telegram account temporarily disconnects, wait for recovery rather than deleting the device or repeatedly scanning. When **Device recovery in progress** appears, follow its stage and next-attempt time; recovery attempts to reuse an existing valid session. Sign in again only when account authorization is explicitly reported as expired. If network safety protection has paused the device, follow the error details and contact support; a successful exit check alone does not mean that protection has been lifted.

If a previous login failed and the device needs connection recovery, choose **Restore device and sign in** in Account login. This restores the existing device connection before continuing login; you do not need to delete or recreate the device. Do not click repeatedly while recovery is in progress. If the request cannot complete, check the proxy and try again.

**Network safety protection has paused the device** means protection has paused the connection, not that a new proxy check has just failed. Follow the page guidance and contact support before checking the new exit result. **Check again** only refreshes the measurement; it does not lift safety protection.

In device details, open **Change device proxy**, enter the full new protocol, host, port and
required credentials, then select **Update proxy and reconnect**. The device disconnects and
reconnects; its previous password is never shown. A submitted change does not mean the device
has connected or signed in successfully. Check its status. If the result is uncertain, refresh
the status first; re-enter the complete configuration only if another attempt is needed.

## Delete a device

Open the device details, select **Delete cloud device**, and confirm. Do not continue sending after submission. The occupied slot is released when deletion finishes; do not create another device for the same account to bypass the pending state.

## Troubleshooting

- After confirming a LINE PIN on your phone, wait for the web page to show a successful login and Online status. Phone confirmation alone does not mean the connection is ready. If the page reports a failed login, review the latest error and use a new QR code when restarting login.
- If the page explicitly says login requests are being limited, wait before retrying and avoid repeated clicks. Other connection or login failures do not necessarily mean throttling. Refresh the status, check the proxy configuration, and contact support if the problem persists.

- The page cannot submit the request: refresh, re-enter the proxy password, and try again. If the device already appears in the list, check its status instead of creating another one.

- Expired QR or verification code: use only the new challenge shown on the page. If the attempt has ended, wait for cleanup before selecting **Start / restart login**.
- Stuck in Connecting: check that the proxy host, port and authentication details are correct and the proxy is reachable, then reconnect.
- Expired status: sign in again and do not repeatedly submit an old code.
- Unknown send result: check the actual social app before sending again to avoid a duplicate message.
- No managed egress or account type on the page: that option is currently unavailable. Use another option shown on the page or contact YundaDesk Support.
- X sign-in cannot continue: ask YundaDesk Support to complete the protected connection. Do not send raw cookies or session files.

If the device still cannot recover, provide the account type, page status, approximate time, and safe error code shown in the UI. Never attach verification codes, passwords, proxy credentials, cookies, or session files.
