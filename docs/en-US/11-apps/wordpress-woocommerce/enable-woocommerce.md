---
title: Enable the read-only WooCommerce enhancement
description: Authorize WooCommerce in read-only mode and confirm store data, cart context, and event status.
category: Apps and integrations
order: 3
updated_at: 2026-09-07
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

YundaDesk does not ask for **Write** or **Read/Write** access. You do not need to create or paste a Consumer Key or Consumer Secret; complete the connection through the authorization page above.

## Wait for the initial sync

After authorization, **Settings → YundaDesk** confirms that read-only WooCommerce access is connected. In YundaDesk, open **Apps → WordPress → Manage sites** and check **WooCommerce read-only data** for the correct address. **View store status** on the WooCommerce app card opens the same management view. If synchronization is still in progress, refresh the page later.

**Site chat** and store data authorization are independent. If read-only authorization is required, select **Open WordPress settings** and approve access for that site. Another site's connected status does not grant access to this store.

The WordPress settings page confirms authorization, not that all store data is already available. Check the correct store's products and orders in YundaDesk, then verify an actual order lookup.

## Reauthorize an existing store

WooCommerce may require authorization again after reconnecting a disconnected site, restoring a previous connection, or changing the website address. A **Connected** WordPress status does not mean store access has also been restored.

1. Check the current WordPress address and the site selected in YundaDesk.
2. Under **Settings → YundaDesk**, select the read-only WooCommerce connection again.
3. Approve **Read** on the current store's authorization page, then return to settings.
4. Return to YundaDesk, refresh that site's status, and verify an order from that store.

Handle each site separately. Do not use another store's authorization in place of the current store's connection.

## Verify order lookup

1. Choose a WooCommerce test order and note its order number, billing email, amount, and current status.
2. Open that customer's conversation in YundaDesk and confirm that the customer email matches the order's billing email.
3. In the Inbox's store-orders sidebar, verify the store and order details.
4. Also test an email with no orders and confirm that another customer's orders are not displayed.

If orders remain unavailable, check the store and email first, then look for a reauthorization prompt. Previously displayed orders do not verify the current connection. A temporary inability to read orders does not mean the customer has no orders.

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
