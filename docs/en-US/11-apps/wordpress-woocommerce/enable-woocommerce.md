---
title: Enable the read-only WooCommerce enhancement
description: Authorize WooCommerce in read-only mode and confirm store data, cart context, and event status.
category: Apps and integrations
order: 3
updated_at: 2026-08-05
---

# Enable the read-only WooCommerce enhancement

WooCommerce is an optional mode inside the same YundaDesk plugin. The WordPress Widget works without it. Store access begins only after an administrator separately approves WooCommerce **Read** permission.

## Before you begin

- Connect the WordPress site to YundaDesk.
- Install and activate WooCommerce 8.2 or newer.
- Use an account that can manage both WordPress settings and WooCommerce.

## Authorize WooCommerce

1. Open **Settings → YundaDesk**.
2. Find **WooCommerce enhancement**.
3. Select **Connect WooCommerce (read-only)**.
4. On the WooCommerce authorization page, confirm that the requested access is **Read**.
5. Approve the connection and return to **Settings → YundaDesk**.

![WooCommerce asks for Read access only](/help/assets/docs/wordpress/en/woocommerce-read-authorization.jpg "Approve read-only WooCommerce access")

YundaDesk does not ask for **Write** or **Read/Write** access. You never need to paste a Consumer Key or Consumer Secret into a YundaDesk form, and WooCommerce credentials are not saved in WordPress options.

## Wait for the initial sync

The first sync reads the store in this order:

1. store information;
2. customers;
3. products and variations;
4. orders.

After authorization, **Settings → YundaDesk** confirms that read-only WooCommerce access is connected. In YundaDesk, open **Apps → WordPress**, choose the site, and confirm that its WooCommerce enhancement is **Connected**. Later syncs read changes instead of rebuilding the entire store. Event notifications contain a minimal resource reference; YundaDesk then reads the current resource from WooCommerce.

The WordPress settings page confirms the authorization state; it does not display per-resource sync progress. Use synthetic test data to verify that each supported resource reaches YundaDesk, and do not treat authorization alone as proof that every resource has synchronized.

## Verify store context

1. Create or update a test product, customer, and order.
2. Confirm that the changed resources appear in YundaDesk after synchronization.
3. Open the storefront as a visitor with an active YundaDesk conversation.
4. Add, change, and remove a product in both the classic cart and Cart block when your site uses them.
5. Confirm that the current cart context updates without sending an address, email address, or phone number.

Cart context is short-lived and belongs to the current visitor conversation. YundaDesk does not label a cart as an abandoned checkout.

## If WooCommerce is deactivated

The WordPress Widget remains available. Store synchronization and WooCommerce event delivery pause until WooCommerce is active again. After reactivation, return to **Settings → YundaDesk** to refresh the authorization state, then verify the site enhancement and live-data capabilities in YundaDesk.

Read [WordPress and WooCommerce data and permissions](./data-and-permissions.md) for the complete data boundary.
