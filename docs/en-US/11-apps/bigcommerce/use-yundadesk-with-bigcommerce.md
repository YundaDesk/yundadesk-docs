---
title: Use YundaDesk with BigCommerce
description: Sync read-only store data, enable the Widget on compatible storefronts, and view support context in the YundaDesk Inbox.
category: Apps and integrations
order: 2
updated_at: 2026-09-08
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
4. Review the **Store data** connection. Under **Storefront chat**, each storefront has a card with its URL, chat status, and an **Open store and check** button.
5. For an enabled, compatible storefront, select **Open store and check** on its card to open that storefront in a new tab and check the chat launcher. **Last check passed** refers to an earlier check; run another check to confirm the current state. If a new tab does not open automatically, select **Continue to storefront** in the same position to continue the current check.
6. Select **Set up storefront chat** at the bottom to open the store’s YundaDesk app configuration page in a new tab and manage each storefront there. Enable a storefront there before checking it.

When there are more than three storefronts, expand the remaining storefronts to see the full list. With more than five, the expanded list scrolls internally. **Help center** at the bottom left opens BigCommerce help; the refresh button on the right updates connection status.

The YundaDesk card provides a quick view of connection and storefront-chat status for the linked store. Continue to use **Apps → My Apps → YundaDesk** in the BigCommerce control panel for BigCommerce-specific resource synchronization, webhook repair, storefront enablement, and Script repair.

## Manage several stores

A workspace can connect several BigCommerce stores, and each store can have multiple storefronts. The list shows the current store count, with each store’s connection status, storefront URLs, and actions grouped separately.

- **Connect another store:** select this button below the list, sign in to BigCommerce, and choose the store to install on. Confirm the actual store and target workspace to finish linking. YundaDesk highlights the newly connected store when you return.
- **Uninstall in BigCommerce:** select this action at the bottom of the store card, to the left of **Configure storefront chat**. It opens that store’s **Apps → My Apps**. Confirm the current store name, then uninstall YundaDesk from its app menu. This affects every storefront belonging to that store, but not other connected stores.
- **Check the result:** return to YundaDesk to view or refresh the status. Opening the admin page does not mean the app has been uninstalled. Once the uninstall result is confirmed, the store leaves the current list. You can connect a store again after removing the last one.

Complete any sign-in, store switching, or permission requests in BigCommerce. YundaDesk members without permission to manage apps can view connection status and help, but cannot use installation, uninstall-navigation, or chat-settings actions.

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
5. Wait for **Enabled**. Then open the storefront to verify that chat actually loads.

YundaDesk creates its own functional, footer, deferred Script through the BigCommerce Scripts API. You do not copy JavaScript. BigCommerce may take a short time to refresh a new script, so wait up to a minute before testing the public storefront.

Stencil and version-confirmed Catalyst storefronts are supported. Blueprint and unverified headless storefronts remain unsupported and cannot be forced on.

## Verify the Widget and a real message

Select **Open storefront and check** for the storefront, or **Open store and check** on its row in YundaDesk. The browser opens that storefront and checks whether chat loads.

- **Verification pending**: chat is enabled but has not passed this check.
- **Verified in this check**: chat loaded during this check.
- **Previously verified**: an earlier check passed; this is not a live assertion.
- **Widget not detected**: check the storefront, browser blocking, and chat status, then try again.

Verify each storefront separately. Disabling one storefront’s chat leaves store data and other storefronts connected.

Continue with a real-message check:


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

## Chat after reconnecting

Ordinary reauthorization keeps healthy, previously enabled storefronts enabled in the same workspace. Disabled storefronts stay disabled. A missing Script requires confirmed repair, and a changed storefront address requires confirmation before enabling again.

After uninstalling and reinstalling, confirm the workspace again and enable the desired storefronts individually. Previous activation choices are not restored automatically.
