---
title: Connect a WordPress site to YundaDesk
description: Securely link a WordPress site to a workspace, display the Widget, and verify a real conversation.
category: Apps and integrations
order: 2
updated_at: 2026-09-07
---

# Connect a WordPress site to YundaDesk

Connecting creates a site-specific link between WordPress and one YundaDesk workspace. The site receives only the limited configuration needed to display its public Widget. WooCommerce store data remains unavailable until you approve the separate read-only authorization.

## Before you begin

- Install and activate the YundaDesk plugin.
- Sign in as a WordPress administrator with permission to manage site settings.
- Use a YundaDesk workspace account with permission to manage apps.
- Make sure the server can reach YundaDesk over HTTPS.
- Decide which YundaDesk workspace should own the site. A site can belong to only one workspace at a time.

## Connect the site

1. In WordPress Admin, open **Settings → YundaDesk**.
2. Select **Connect YundaDesk**.
3. Sign in to YundaDesk, or create an account if needed.
4. Review the site address, WordPress and plugin versions, detected WooCommerce version, and current workspace.
5. For a first connection, select **Confirm site connection**. When reconnecting, check the original chat channel shown and confirm. You only need to choose when several previous channels are found. This does not grant WooCommerce access.
6. When YundaDesk says the authorization is ready, select **Return to WordPress**. This explicit return opens the same WordPress Admin page and finishes the secure connection.
7. Confirm that the connection status is **Connected**.

The return link is accepted only for the same WordPress Admin origin that started the connection. If the page says the request expired, return to **Settings → YundaDesk** and start again instead of reusing the old link.

## Reconnect or restore a previous site

Start again from **Settings → YundaDesk** in the current WordPress Admin, and make sure you are in the intended workspace. Use the options offered on the confirmation page:

If the page still shows **Connected** without a connection button, but you need to pair again or update the site address, disconnect the current site on this page first. Wait for confirmation, then select **Connect YundaDesk**. The Widget pauses while disconnected; do not delete another site.

| Page display | What to do |
|---|---|
| Reconnect this WordPress site | Check the chat channel and select “Confirm reconnection”; past conversations are kept without creating another channel |
| Installation information has changed | Confirm this address still belongs to your original website before restoring the channel shown; cancel if unsure |
| Confirm the site address change | Check the previous address, current address and original channel, then select “Update and connect” |
| Choose the chat channel to restore | Compare addresses, last connection times and references, select the correct history and choose “Confirm restoration”; nothing is preselected |

Ordinary reconnection does not offer a separate new connection. A new chat channel is created only for a first connection with no related history.

Do not select a historical connection just because its address matches. If the intended site is unclear, check with your workspace administrator first. Restoring a connection does not merge another site's history or renew WooCommerce access.

After confirming, select **Return to WordPress**. Check for **Connected** in WordPress, verify the site address and channel in YundaDesk, and test a new message as described below.

If the page says the connection changed, select **Refresh pairing details** and review it again. If the original chat channel is unavailable, ask your workspace administrator to check it before starting again. Do not delete another site to bypass the warning.

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

## Manage current sites in YundaDesk

Open **Apps → WordPress → Manage sites** to see the current connection count and each site's full address. **Site chat** and **WooCommerce read-only data** have separate statuses. Not enabling WooCommerce or not yet granting read-only access does not mean site chat has failed. Read-only members can inspect status; connection and disconnect actions require the appropriate management permission.

Select **Open WordPress settings** to visit that site's admin page. **Disconnect in WordPress** also only opens the admin page; it does not disconnect anything until you confirm the action in WordPress. Returning to YundaDesk refreshes the status. Select **Retry** if loading fails.

**Installation guide** opens the official WordPress/WooCommerce guide in a new tab. **Close** only dismisses the details; it does not disconnect the site or change authorization.

If you can manage apps and the official installation entry is available, **Install on another site** appears beside **Close**. It opens the official WordPress.org plugin directory in a new tab, leaving the current site and details unchanged. Install the plugin on the other WordPress site and complete its connection separately.

Sites leave this list after disconnection completes, while conversation history is retained. When all sites have finished disconnecting, the cards no longer show an installed status and return to the same official installation entry used for a first connection. When available, **Install on WordPress** opens the WordPress.org plugin directory in a new tab, without a site-management or connection-instructions dialog first. The WooCommerce card's official installation entry opens the same plugin. If the entry is not available yet, follow the status shown on the card.

An already installed plugin does not need to be downloaded again. You can reconnect directly from **Settings → YundaDesk** in WordPress Admin. Previous connections are offered only when confirming an actual connection request.

## Next step

If WooCommerce is active, continue with [Enable the read-only WooCommerce enhancement](./enable-woocommerce.md).
