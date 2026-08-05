---
title: WordPress and WooCommerce data and permissions
description: Understand what the YundaDesk plugin sends, what WooCommerce data it reads, and what it never changes.
category: Apps and integrations
order: 4
updated_at: 2026-08-05
---

# WordPress and WooCommerce data and permissions

YundaDesk separates the WordPress site connection from WooCommerce store access. Connecting WordPress enables the Widget. WooCommerce data remains off until a store administrator approves read-only access.

## WordPress site connection

When an administrator starts the connection, the plugin sends the site address, a random site identifier, and the installed YundaDesk, WordPress, PHP, and optional WooCommerce versions. After connection, a limited status check reports version and availability information so the site can show whether the integration is healthy.

The storefront loads YundaDesk's hosted Widget only after connection. Messages and details that visitors choose to submit through the Widget are processed as customer-support data.

## WooCommerce read-only data

| Resource | What YundaDesk uses | Important boundary |
|---|---|---|
| Store | Currency and non-sensitive store information | No store settings are changed |
| Customer | Email address, display name, and country or region | Phone numbers are not retained for this integration |
| Product and variation | Product name, SKU, price, inventory, and variation information | Products and stock are never edited |
| Order | Order number, amount, currency, status, line items, and permitted identity fields | Shipping address and phone number are not retained |
| Cart | Current items, SKU, quantity, amount, currency, and page context | Sent only for a visitor with an active Widget conversation; no address, email, or phone |

YundaDesk does not edit orders, issue refunds, change customers, or modify products. WooCommerce Core does not provide an authoritative abandoned-checkout record, so YundaDesk does not invent one from cart activity.

## Synchronization and events

The initial read is paginated. Later reads use changed-resource markers so the same object is not duplicated. WooCommerce events notify YundaDesk that a supported customer, product, or order changed; the event contains a minimal identifier rather than the full business record. YundaDesk then reads the current version from the store.

If read permission is revoked or expires, the WooCommerce section displays **Reauthorization required** and store reads stop until an administrator approves read-only access again.

## External services

The plugin uses these YundaDesk services after you connect it:

- `app.yundadesk.com` for administrator sign-in and workspace confirmation;
- `api.yundadesk.com` for the site connection, status, privacy requests, and WooCommerce synchronization;
- `cdn.yundadesk.com` for the public Widget loader.

Review the [YundaDesk Privacy Policy](https://yundadesk.com/privacy/) and [Terms of Service](https://yundadesk.com/terms/). Add an appropriate disclosure to your own site's privacy policy before serving visitors.

## Privacy responsibility

The plugin supplies suggested privacy-policy text and integrates with WordPress personal-data tools. These tools help site administrators respond to requests, but installing the plugin does not automatically make a site compliant with GDPR, CCPA, or any other law. Your organization remains responsible for the legal basis, notices, requester verification, retention choices, and responses required for its site.
