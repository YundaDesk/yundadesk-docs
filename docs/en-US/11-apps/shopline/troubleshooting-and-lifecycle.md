---
title: SHOPLINE troubleshooting and connection management
description: Resolve theme chat, store connection, and messaging problems, and understand reauthorization, disabling chat, and uninstalling.
category: Apps and integrations
order: 4
updated_at: 2026-10-02
---

# SHOPLINE troubleshooting and connection management

Identify whether the problem concerns installation, theme display, message delivery, or order lookup. When store data is connected, check the theme settings before uninstalling the app.

## Cannot find Online Store or App embeds

- **Online Store** is in the SHOPLINE store admin sidebar. Open the admin address from the YundaDesk store instructions instead of searching YundaDesk menus or the buyer-facing storefront.
- **App embeds** is in the current theme's **Design** editor, on the left. The Chinese admin calls it **应用嵌入**.
- If theme editing is unavailable, check that your account has theme editing permission.

See the full steps in [Enable storefront chat](./enable-storefront-chat.md).

## YundaDesk Chat is missing from App embeds

1. Confirm the public YundaDesk app is installed on this store and the workspace connection is complete.
2. Compare the store in SHOPLINE with the address in YundaDesk connection status.
3. Close and reopen the current theme editor, then check App embeds again.
4. If it remains missing, record the theme name and version and ask support to check compatibility. Do not add another copy of the chat script.

## Chat remains undetected after enabling

1. Check that you enabled **YundaDesk Chat**, not SHOPLINE's built-in Message Center chat widget.
2. Check that you edited the current published theme and selected **Save** in the top-right corner.
3. Use **Open store and check** in YundaDesk to open the actual storefront, rather than remaining in theme preview.
4. Complete the store's visitor password step if required. If the new page was blocked, select **Continue to storefront**.
5. Check whether your browser's content-blocking settings prevent chat loading. Allow it according to your browser policy and retry.
6. Return to YundaDesk, refresh the status, and confirm you have not switched stores or workspaces.

**Last check passed** is historical. After changing themes, recheck the switch, save, and run a new check.

## Chat appears but a message is missing

Check that you are in the connected YundaDesk workspace. In the **Inbox**, check conversation filters, assignment, and reception status, then follow [Verify channel message delivery](../../02-channels/verify-channel-delivery.md). A visible Widget does not prove each message was delivered; confirm receipt on the other side.

If only AI replies are missing, check the channel's Agent binding and reception settings. See [Configure an Agent](../../04-ai-customer-service/configure.md).

## Store or workspace mismatch

Check the current SHOPLINE store and the YundaDesk account and workspace. An already-connected store's confirmation page may offer continued access or account linking; read the options before choosing. Contact the original workspace administrator to change ownership. Do not uninstall merely to test whether it resolves the mismatch, and do not forward temporary authorization links.

## Reauthorization is required

1. Follow the prompt to **Reauthorize** the affected store.
2. Check the store and permissions in SHOPLINE, complete authorization, and return to YundaDesk.
3. Check store data status, YundaDesk Chat in the theme, and message delivery again.

If the return page says the request expired, start again from the current app entry. A completed redirect alone does not prove all features work after reauthorization.

## Disabling chat versus uninstalling

| Action | Effect |
|---|---|
| Turn off YundaDesk Chat in the theme and save | Removes YundaDesk chat from that theme while keeping the store data connection |
| Uninstall YundaDesk from the SHOPLINE admin app list | Revokes this store's app connection; data sync and associated storefront chat stop |
| Reinstall | Requires authorization, workspace confirmation, theme-switch checks, and message verification again |

Before uninstalling, check the store and the effect. Use the theme switch if you only want to hide chat temporarily. After uninstalling, return to YundaDesk to review the latest status. Uninstalling is not the same as immediately erasing all historical conversations or personal data. For erasure, see [Security and data](../../10-troubleshooting/security-and-data.md) and contact support.

## Before contacting support

Use [Contact support](../../10-troubleshooting/contact-support.md) and provide the failing step, approximate time, theme name and version, displayed message, and redacted screenshots. Do not include passwords, authorization links, keys, or complete customer order records.
