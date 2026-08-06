---
title: BigCommerce data permissions and app lifecycle
description: Understand what YundaDesk reads, multi-user access, reauthorization, uninstall, and common troubleshooting.
category: Apps and integrations
order: 3
updated_at: 2026-08-06
---

# BigCommerce data permissions and app lifecycle

YundaDesk keeps BigCommerce store authorization separate from YundaDesk workspace membership and limits store capabilities to read-only support context and its own storefront Widget.

## Data YundaDesk reads

| Object | Purpose | Data boundary |
|---|---|---|
| Store | Identify the conversation source and show basic store information | Store identifier, name, public URL, currency, and similar basics |
| Customer | Match a customer in the Inbox | Platform customer identifier, email, display name, and optional country when available without reading addresses |
| Order | Help agents answer order questions | Order identifier, status, totals, currency, item summary, and timestamps |
| Product and variant | Provide purchased-product context | Product and variant identifiers, name, SKU, price, and availability status |
| Cart and abandoned checkout | Provide cart context created after installation | Cart identifier, status, totals, item summary, and timestamps; no historical backfill |

YundaDesk does not store shipping or billing addresses, phone numbers, payment information, full IP information, or raw BigCommerce responses. Cart context does not store addresses or coupons.

## Actions YundaDesk does not perform

YundaDesk does not:

- edit, cancel, or refund orders;
- modify inventory, products, customers, or discounts;
- change checkout or handle payments;
- invent abandoned-checkout records from historical carts;
- automatically send abandoned-cart marketing messages.

BigCommerce automatically includes its basic store access for every app, so the authorization page may show **View and modify basic store information**; YundaDesk does not use that default access to change store settings. The only storefront write YundaDesk performs is managing its own Script, and an administrator must still confirm each storefront enable, disable, or repair action in the app.

## Events and synchronization

Store, Customers, Orders, and Products have read-only manual synchronization controls on the app status page. BigCommerce webhooks also keep customer, order, product, inventory, and cart changes current.

Carts and abandoned checkouts begin only after the app is installed and webhooks are healthy. A successful authorization does not prove that every resource already has data. Verify each type with synthetic customers, products, orders, and carts that contain no real personal information.

## Multi-user access

A BigCommerce store can let multiple authorized users open YundaDesk, but BigCommerce identity never bypasses YundaDesk permissions:

1. The store owner installs the app and connects the store to one workspace.
2. When another BigCommerce user first opens the app, they must sign in in a new tab as an existing YundaDesk member of that workspace.
3. A member can perform only the actions allowed by their YundaDesk role.
4. Synchronization, webhook repair, storefront changes, and Script repair require permission to manage apps.

Removing a user's YundaDesk app access in BigCommerce ends that user's BigCommerce app session. It does not automatically delete their independent YundaDesk workspace membership. A workspace administrator manages that membership separately when needed.

## Reauthorize the app

If the store token becomes invalid, authorization is revoked, or required permissions change, the app asks for reauthorization and pauses synchronization and storefront status checks.

1. Have the BigCommerce store owner open the app.
2. Follow the page instructions to reinstall or reauthorize YundaDesk.
3. Reopen the app and confirm that both authorization and workspace show **Connected**.
4. Check webhook and storefront Script status. Run a confirmed repair only when the page reports a missing item.

Do not reuse an old account-connection link or forward one to another user.

## Disable chat on one storefront

To stop the Widget on only one storefront:

1. Open **Apps → My Apps → YundaDesk**.
2. Find the storefront under **Storefront chat**.
3. Select **Disable**.
4. Use a private browser window to confirm that the storefront no longer loads the Widget.

Other enabled storefronts and read-only store synchronization continue.

## Uninstall the app

Uninstall only when you no longer need the entire store connection:

1. In the BigCommerce control panel, open **Apps → My Apps**.
2. Find YundaDesk, open its app actions, and select uninstall.
3. Review the BigCommerce confirmation and confirm.

After uninstall, YundaDesk stops synchronization and event processing for the store, ends app sessions, and immediately rejects Widget configuration for its storefronts. BigCommerce cleans up webhooks and auto-uninstall Scripts created by the app. Data created from this store authorization enters cleanup according to the YundaDesk Privacy Policy.

A later reinstall creates a new authorization and requires an explicit YundaDesk workspace selection again. Old connection links and old authorization cannot be reused.

## Common troubleshooting

### The Widget does not appear

- Confirm that the target storefront is **Active**, not merely that the app is installed.
- Wait one minute, then hard-refresh the public storefront.
- Test the exact HTTPS storefront URL shown in the app.
- Check that the cookie-consent configuration permits functional Scripts.
- Blueprint and unverified headless storefronts are unsupported.

### The Script is missing

YundaDesk never recreates it during a status check. After confirming that an administrator removed the Script, use a member with app-management permission to select **Repair Script** and confirm.

### Webhooks require repair

Use a member with app-management permission to select **Repair webhooks**, read the prompt, and confirm. Real-time changes may not reach YundaDesk promptly until repair finishes.

### Synchronization has no data

Confirm that the test store contains visible synthetic customers, orders, and products, then select **Sync now** for each relevant resource. Carts and abandoned checkouts process new post-install events only and cannot be backfilled by manual synchronization.

If the problem continues, follow [Prepare an effective support request](../../10-troubleshooting/contact-support.md) and include the public store URL, approximate time, non-sensitive status shown on the page, and reproduction steps. Never send passwords, API keys, customer addresses, phone numbers, or full order records.
