---
title: Use YundaDesk with BigCommerce
description: Sync read-only store data, enable the Widget on compatible storefronts, and view support context in the YundaDesk Inbox.
category: Apps and integrations
order: 2
updated_at: 2026-08-06
---

# Use YundaDesk with BigCommerce

After installation and workspace connection, manage synchronization, webhooks, and storefront chat from BigCommerce. You can also review connection status from the YundaDesk app center before serving customers in the YundaDesk Inbox.

## Open the app status page

1. Sign in to the BigCommerce control panel.
2. Open **Apps → My Apps → YundaDesk**.
3. Confirm that both **BigCommerce authorization** and **YundaDesk workspace** show **Connected**.

Only a YundaDesk member linked to the workspace can view workspace status. Synchronization, webhook repair, and storefront changes also require permission to manage apps.

## Manage from the YundaDesk app center

1. Sign in to YundaDesk and open **Apps**.
2. Find the **BigCommerce** card marked **Installed**.
3. Select **View store status**.
4. Review the **Store data** connection and **Storefront chat** status. Refresh the status or open the storefront for verification when needed.

The YundaDesk card provides a quick view of connection and storefront-chat status for the linked store. Continue to use **Apps → My Apps → YundaDesk** in the BigCommerce control panel for BigCommerce-specific resource synchronization, webhook repair, storefront enablement, and Script repair.

## Sync read-only store data

In **Commerce data**, select **Sync now** for each of these resources:

- **Store:** basic store information;
- **Customers:** the minimum profile needed to identify and support customers;
- **Orders:** order status, totals, and item summaries;
- **Products:** product and variant context for support.

The initial synchronization is queued. Select **Refresh status** later to check the latest state. A repeated synchronization updates existing records instead of duplicating store objects.

**Carts** and **Abandoned checkouts** use post-install events. They have no historical backfill and no manual whole-store sync button. Recording starts with new events after webhook subscriptions are healthy.

## Check webhook status

**Webhook subscriptions** shows whether all required YundaDesk subscriptions are healthy. Webhooks keep customer, order, product, inventory, cart, and uninstall state current.

The status check is read-only and never recreates missing subscriptions automatically. If the page shows **Repair required**:

1. Open the app as a YundaDesk member with permission to manage apps.
2. Select **Repair webhooks**.
3. Read the confirmation and confirm the repair.
4. Refresh the status when it finishes.

## Enable storefront chat

YundaDesk lists detected storefronts under **Storefront chat**. Enable each storefront separately.

1. Find the primary storefront or another storefront you want to enable.
2. Review its URL and storefront type.
3. Select **Enable storefront chat**.
4. For Catalyst, confirm that the storefront runs Catalyst 1.1 or later.
5. Wait for the status to become **Active**.

YundaDesk creates its own functional, footer, deferred Script through the BigCommerce Scripts API. You do not copy JavaScript. BigCommerce may take a short time to refresh a new script, so wait up to a minute before testing the public storefront.

Stencil and version-confirmed Catalyst storefronts are supported. Blueprint and unverified headless storefronts remain unsupported and cannot be forced on.

## Verify the Widget and a real message

1. Open the enabled storefront URL in a private browser window.
2. Accept or configure the storefront's cookie choices. The YundaDesk Script follows BigCommerce's functional consent configuration.
3. Confirm that the page shows one YundaDesk chat launcher.
4. Send a test message that contains no private information.
5. Sign in to YundaDesk, open the **Inbox**, and confirm that the new conversation reached the correct workspace.
6. Reply from the Inbox and confirm that the storefront Widget receives the reply.

If a workspace connects several stores, verify the store source in the Inbox. Only customer or order information verified and synchronized from the commerce platform should appear as store context.

## View order context in the Inbox

Open a BigCommerce customer conversation in the YundaDesk Inbox. When a match is available, the customer sidebar shows read-only store context such as order status, totals, item summaries, and update time.

This information helps support teams answer questions such as “What is my order status?” and “What did I buy?” YundaDesk does not offer actions to refund, cancel, change an address, modify inventory, edit a customer, change discounts, or handle payments.

## Manage multiple storefronts

- Enable each compatible storefront that needs live chat.
- Every storefront has its own URL and Script status; enabling one never enables the others automatically.
- Selecting **Disable** stops the YundaDesk Widget on that storefront without affecting other enabled storefronts.
- If an administrator deletes the YundaDesk Script in BigCommerce Script Manager, the app reports **Script missing** and does not write it back automatically. Select **Repair Script** only after reviewing the confirmation.

Continue with [data permissions, multi-user access, and uninstall](./data-permissions-and-lifecycle.md).
