---
title: Connect a WordPress site to YundaDesk
description: Securely link a WordPress site to a workspace, display the Widget, and verify a real conversation.
category: Apps and integrations
order: 2
updated_at: 2026-08-05
---

# Connect a WordPress site to YundaDesk

Connecting creates a site-specific link between WordPress and one YundaDesk workspace. The site receives only the limited configuration needed to display its public Widget. WooCommerce store data remains unavailable until you approve the separate read-only authorization.

## Before you begin

- Install and activate the YundaDesk plugin.
- Sign in as a WordPress administrator with permission to manage site settings.
- Make sure the server can reach YundaDesk over HTTPS.
- Decide which YundaDesk workspace should own the site. A site can belong to only one workspace at a time.

## Connect the site

1. In WordPress Admin, open **Settings → YundaDesk**.
2. Select **Connect YundaDesk**.
3. Sign in to YundaDesk, or create an account if needed.
4. Review the site address, WordPress and plugin versions, detected WooCommerce version, and current workspace.
5. Confirm the site connection. This confirmation does not grant WooCommerce access.
6. When YundaDesk says the authorization is ready, select **Return to WordPress**. This explicit return opens the same WordPress Admin page and finishes the secure connection.
7. Confirm that the connection status is **Connected**.

The return link is accepted only for the same WordPress Admin origin that started the connection. If the page says the request expired, return to **Settings → YundaDesk** and start again instead of reusing the old link.

## Verify the storefront Widget

1. Open a public page in a private browser window.
2. Confirm that the YundaDesk launcher appears.
3. Open it and send a unique test message.
4. In the YundaDesk Inbox, confirm that a new website conversation appears for the correct site.
5. Reply from the Inbox and confirm that the visitor receives the reply in the Widget.

![The YundaDesk Widget receiving a real reply on the WordPress storefront](/help/assets/docs/wordpress/en/storefront-widget.jpg "Verify a real storefront conversation")

The plugin loads the Widget on public rendered pages only. It does not inject it into WordPress Admin, login pages, feeds, or REST requests. Only the public Widget identifier is exposed to the storefront; connection credentials and WooCommerce credentials are never placed in page source.

## Connect more than one site

A workspace can contain several WordPress sites. Install the same plugin on each site and complete the connection separately. Each site keeps its own status, Widget configuration, WooCommerce state, and disconnect lifecycle.

## Next step

If WooCommerce is active, continue with [Enable the read-only WooCommerce enhancement](./enable-woocommerce.md).
