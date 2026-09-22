---
title: Enable the read-only WooCommerce enhancement
description: Authorize WooCommerce in read-only mode and confirm store data, cart context, and event status.
category: Apps and integrations
order: 3
updated_at: 2026-09-24
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

When a visitor asks about an order in website chat and the AI agent finds it, a compact order card appears separately below the text bubble, with the order number, items and quantities, amount, and statuses supplied by the store. The card remains visible after refreshing or reopening the same conversation. It shows information from that lookup; ask again for the latest progress. Missing payment or shipping statuses are not inferred, and a custom order status does not establish that an order has been paid or shipped.

1. Choose a WooCommerce test order and note its order number, billing email, amount, and current status.
2. Open that customer's conversation in YundaDesk and confirm that the customer email matches the order's billing email.
3. In the Inbox's **Store orders** sidebar, verify the store and order details. For an order with multiple products, select **View all N items** to expand every product name, quantity, and available SKU in place. Select **Collapse items** to return to the summary.
4. Also test an email with no orders and confirm that another customer's orders are not displayed.

If orders remain unavailable, check the store and email first, then look for a reauthorization prompt. Previously displayed orders do not verify the current connection. A temporary inability to read orders does not mean the customer has no orders.

## View the current cart

1. Have the visitor start an active YundaDesk conversation on the connected storefront.
2. Add products, change quantities, or remove products in the store.
3. Open that visitor's conversation in YundaDesk and find **Current cart** below **Store orders** in the sidebar. An email address is not required, and the cart can appear without the orders section. Your staff account needs permission to view the conversation and app data.
4. Check product names, quantities, available SKUs, the item count, **Subtotal**, and currency. The subtotal is not the final amount including shipping and tax.
5. Keep the sidebar open to receive updates, or select **Refresh cart**. Use **Data updated** to check how recent the information is.

| Displayed state | What to check |
|---|---|
| The cart is empty | An empty cart was received. Add a product in the store and check again. |
| No cart data is currently available | There is no available information to display; the store cart is not necessarily empty. Confirm that the conversation is active, then change the cart in the store. |
| The cart data has expired | The previous information is no longer available for display. Have the visitor return to the store and change the cart, then check again. |
| The conversation or store connection is unavailable | Check whether the conversation has ended or the correct site needs reconnection or reauthorization. |
| The cart could not refresh | Try again later. If previous information remains visible, check its update time. |

The sidebar shows the latest cart information received from the store. **Refresh cart** rereads that information; it does not change or reload the visitor's store cart. If rapid changes leave the display behind, wait before changing the cart again or reloading the storefront, then check the update time. Repeatedly refreshing the staff page cannot guarantee recovery of changes that have not been received.

Cart information belongs to the current active visitor conversation. YundaDesk does not label the visitor as an abandoned checkout based on it. Cart availability may differ for other ecommerce platforms.

## If WooCommerce is deactivated

The WordPress Widget remains available. Store synchronization and WooCommerce event delivery pause until WooCommerce is active again. After reactivation, return to **Settings → YundaDesk** to refresh the authorization state, then verify the site enhancement and live-data capabilities in YundaDesk.

Read [WordPress and WooCommerce data and permissions](./data-and-permissions.md) for the complete data boundary.
