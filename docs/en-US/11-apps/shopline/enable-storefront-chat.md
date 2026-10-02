---
title: Enable and verify SHOPLINE storefront chat
description: Open App embeds in your current SHOPLINE theme, enable YundaDesk Chat and save, then check the storefront and test messages in both directions.
category: Apps and integrations
order: 2
updated_at: 2026-10-02
---

# Enable and verify SHOPLINE storefront chat

Enable **YundaDesk Chat** under **App embeds** in the current SHOPLINE theme and save to show chat to visitors. Return to YundaDesk to check the storefront, then test a message in both directions.

Pause the walkthrough or move between steps to learn where to act. It uses demo data and does not authorize an app, connect a store, or send messages for you. Complete the actual steps in your own store and workspace.

## Before you begin

- [Install the public app and confirm the workspace connection](./install-and-connect.md).
- Use a SHOPLINE account that can edit and save store themes.
- Make sure you are editing the connected store's current theme.

## 1. Open the store admin

In YundaDesk, open **Apps → SHOPLINE → View store status**, check the store address, and select **Set up storefront chat**. Expand the instructions and select the **store admin** link in the first step.

**Online Store** is in the SHOPLINE store admin sidebar. It is not a YundaDesk menu or a page on the buyer-facing storefront. If SHOPLINE asks you to sign in, use an account with theme editing permission and check that you enter the same store.

## 2. Find the current theme

1. In the SHOPLINE admin sidebar, select **Online Store → Design**.
2. Find the current published theme and select **Design** beside it.

![Online Store → Design in the SHOPLINE admin sidebar](/help/assets/docs/shopline/en/store-design-menu.png "Open Online Store → Design in the store admin")

![Design beside the published SHOPLINE theme](/help/assets/docs/shopline/en/current-theme.png "Edit the current published theme")

Do not edit only an alternative theme. Visitors see the published theme.

## 3. Enable YundaDesk Chat and save

1. Select **App embeds** in the theme editor's left sidebar.
2. Find **YundaDesk Chat** and check that the developer shown beneath it is **YundaDesk**.
3. Turn on its switch.
4. Select **Save** in the top-right corner and wait for saving to complete.

![App embeds with YundaDesk Chat enabled](/help/assets/docs/shopline/en/app-embeds.png "Enable YundaDesk Chat under App embeds")

SHOPLINE’s built-in Chat widget from Messages is a different app. Enabling it does not enable YundaDesk Chat.

The English SHOPLINE admin calls this panel **App embeds**; the Chinese admin calls it **应用嵌入**. The menu follows the SHOPLINE admin language, which may differ from your YundaDesk language.

## 4. Return to YundaDesk and check

1. Return to the correct store's **SHOPLINE integration status**.
2. Select **Open store and check** and use the storefront page opened by this action.
3. If the browser does not open it, select **Continue to storefront** when offered. If the store requires a visitor password, complete that access step first.
4. Confirm the YundaDesk chat entry appears. Return to the status page to check the result and refresh the status if needed.

**Embedded** means chat loaded during this check. **Last check passed** is a past result; check again to verify the current theme. For **Embed not detected**, follow [Chat remains undetected](./troubleshooting-and-lifecycle.md#chat-remains-undetected-after-enabling).

## 5. Verify messages in both directions

1. Open YundaDesk chat on the storefront and send a test message without personal information.
2. Open the **Inbox** in the connected YundaDesk workspace, find the new conversation, and check its store source.
3. Join or take over the conversation as its current state requires, then send a human reply.
4. Return to storefront chat and confirm the visitor actually receives the reply.

Only after these steps have you verified message delivery. **Test connection** checks store data access and does not replace this test.

For automated replies, [configure an Agent](../../04-ai-customer-service/configure.md). For chat appearance, see [Customize the website Widget](../../02-channels/customize-widget.md).

## After changing themes

After changing or publishing a theme, check the **YundaDesk Chat** switch in the new current theme, save, and run the check again. Turning it off disables chat in that theme without disconnecting store data.
