---
title: Install the YundaDesk plugin on WordPress
description: Install one YundaDesk plugin for WordPress live chat and the optional WooCommerce enhancement.
category: Apps and integrations
order: 1
updated_at: 2026-08-05
---

# Install the YundaDesk plugin on WordPress

YundaDesk uses one WordPress plugin. It adds live chat and AI customer service to a WordPress site, then unlocks optional read-only store features when WooCommerce is present. You do not install a second WooCommerce plugin.

## Before you begin

You need:

- WordPress 6.2 or newer;
- PHP 7.4 or newer;
- a WordPress administrator who can install plugins and manage site settings;
- WooCommerce 8.2 or newer only if you want the store enhancement.

The WordPress base connection continues to work when WooCommerce is absent or inactive.

## Install from WordPress.org after directory publication

This option becomes available after WordPress.org publishes the plugin. During a private review or controlled test, use the ZIP supplied by YundaDesk instead.

1. In WordPress Admin, open **Plugins → Add New Plugin**.
2. Search for **YundaDesk**.
3. Confirm the plugin name is **YundaDesk** and its directory slug is `yundadesk`.
4. Select **Install Now**, then **Activate**.
5. Open **Settings → YundaDesk**.

![Search for and install YundaDesk from the WordPress plugin screen](/help/assets/docs/wordpress/en/install-plugin.jpg "Install the YundaDesk plugin")

## Install a ZIP supplied by YundaDesk

If YundaDesk Support gives you an installation ZIP:

1. Open **Plugins → Add New Plugin**.
2. Select **Upload Plugin**.
3. Choose the YundaDesk ZIP, select **Install Now**, and then activate it.
4. Open **Settings → YundaDesk**.

Do not rename files inside the ZIP or install a separate package for WooCommerce.

## What activation does

Activation prepares the plugin locally. It does not connect the site, load the storefront Widget, read WooCommerce data, or contact YundaDesk. An administrator must explicitly select **Connect YundaDesk** before any external request begins.

![The native YundaDesk settings page before a site is connected](/help/assets/docs/wordpress/en/settings-unconnected.jpg "YundaDesk is installed but not connected")

On WordPress multisite, activate and connect each child site that should use YundaDesk. Network activation does not automatically bind every child site to one workspace.

## Next step

Continue with [Connect a WordPress site to YundaDesk](./connect-yundadesk.md).
