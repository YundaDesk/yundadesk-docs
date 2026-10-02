---
title: Install and connect a SHOPLINE store
description: Install YundaDesk from the public SHOPLINE App Store, approve read-only access, and connect the store to the correct workspace.
category: Apps and integrations
order: 1
updated_at: 2026-10-02
---

# Install and connect a SHOPLINE store

Install YundaDesk from the public SHOPLINE App Store. After authorizing the store, sign in to YundaDesk and confirm the workspace. You do not need to copy API keys or create a custom app.

Pause the walkthrough or move between steps to learn where to act. It uses demo data and does not authorize an app, connect a store, or send messages for you. Complete the actual steps in your own store and workspace.

## Before you begin

- Use a SHOPLINE account with permission to install apps on the store.
- Have an account in the intended YundaDesk workspace with permission to manage apps.
- Identify the correct store. If you manage several stores, check the name and address at each installation.

## Install and authorize in SHOPLINE

1. Open [YundaDesk in the SHOPLINE App Store](https://apps.shopline.com/detail/yundadesk_connector). You can also find SHOPLINE under **Apps** in YundaDesk and select **Install on SHOPLINE**.
2. Select **Install**, sign in to SHOPLINE if prompted, and choose the intended store.
3. On the authorization page, check the app name, store, and permissions. YundaDesk requests read access to store information, customers, orders, and products. See [Data and permissions](./data-and-status.md).
4. Read the privacy terms shown on the page. If you agree, confirm authorization and installation.

## Confirm the YundaDesk workspace

1. Follow the redirect to sign in to or register with YundaDesk.
2. Check the store address and current workspace on the connection confirmation page. Complete the connection only when both are correct.
3. If the page says the store is already connected, follow the offered access or account-linking options. Do not create duplicate workspaces to bypass the message.
4. In YundaDesk, open **Apps → SHOPLINE → View store status**.
5. Check the store address and confirm **Store data** shows **Connected**.

If the authorization has expired, start again from the YundaDesk app entry in SHOPLINE instead of reusing an old return link. If the store belongs to another workspace, contact its administrator; see [Store or workspace mismatch](./troubleshooting-and-lifecycle.md#store-or-workspace-mismatch).

## Next: enable storefront chat

Store data can start syncing after connection. Storefront chat still needs to be enabled in the SHOPLINE theme. If chat shows **Not checked yet** or **Embed not detected**, continue with [Enable and verify storefront chat](./enable-storefront-chat.md); the theme setting does not by itself indicate installation failed.

The blue book icon and **Installation guide** link are at the bottom left of the SHOPLINE connection dialog. The link opens this guide in a new tab.
