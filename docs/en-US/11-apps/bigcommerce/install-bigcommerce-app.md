---
title: Install and authorize the YundaDesk BigCommerce app
description: Install YundaDesk from BigCommerce, review its permissions, and securely connect the store to one YundaDesk workspace.
category: Apps and integrations
order: 1
updated_at: 2026-08-06
---

# Install and authorize the YundaDesk BigCommerce app

Installation uses the BigCommerce single-click authorization flow. You do not create an API account, copy credentials, or paste Widget code.

## Before you begin

Prepare the following:

- a BigCommerce store owner or authorized user who can install apps for the store;
- an existing YundaDesk account, or a business email for creating one;
- a YundaDesk workspace where you can manage apps;
- a browser that allows `app.yundadesk.com` to open a new secure tab.

If you plan to display storefront chat, use a Stencil storefront or Catalyst 1.1 or later. Blueprint and unverified headless storefronts cannot enable the YundaDesk Widget.

## Choose an installation entry

You can search for YundaDesk in the BigCommerce Marketplace or start from the YundaDesk app center. Both entries open the same official BigCommerce app details and authorization flow; they do not create separate installations.

### Start from the YundaDesk app center

1. Sign in to YundaDesk and open **Apps**.
2. Find the **BigCommerce** card.
3. If the button says **Install on BigCommerce**, select it and continue the official BigCommerce installation in the new tab.

If the card says **Pending marketplace listing**, the public Marketplace URL is not yet available and the button remains disabled. Do not enter a store identifier, create an API account, or download a package from a third party. Wait for the public listing or contact YundaDesk Support to confirm availability.

The YundaDesk card never asks for a BigCommerce store identifier or API key. It only opens the official installation page after the app is public. After installation and workspace connection, the same card changes to **Installed** and **View store status**.

### Install from BigCommerce

1. Sign in to the BigCommerce control panel.
2. Open **Apps → Marketplace** and search for **YundaDesk**.
3. Open the YundaDesk app details and select the install action.
4. Review the authorization summary, then confirm the installation.

![Review the YundaDesk installation permissions in BigCommerce](/help/assets/docs/bigcommerce/shared/01-install-permissions.jpg "Review permissions before installation")

5. If BigCommerce then shows an access-update confirmation page, review the permissions again and select **Confirm**. This is BigCommerce's second confirmation for the single-click OAuth flow; you do not need to copy API keys.

![Confirm YundaDesk access to the BigCommerce store](/help/assets/docs/bigcommerce/shared/02-confirm-access.jpg "Confirm OAuth access")

YundaDesk reads only the store, customer, order, product, cart, and storefront information needed for customer-support context. BigCommerce automatically includes its basic store access for every app, so the authorization page may show **View and modify basic store information**; YundaDesk does not use that default access to change store settings. The separate content-modification permission is used only to manage YundaDesk's own storefront Script through the BigCommerce Scripts API. YundaDesk does not modify orders, refunds, inventory, customers, checkout, or payments.

If YundaDesk does not yet appear in the Marketplace, the app is not currently public for your store. Do not download an unofficial package from a third party; contact YundaDesk Support to confirm availability.

## Connect a YundaDesk workspace

After authorization, BigCommerce opens the YundaDesk app in the control panel.

1. Select **Connect YundaDesk account**.
2. Sign in to YundaDesk in the new secure tab, or create an account.
3. Review the BigCommerce-verified store name and store URL. These values are read-only on the connection page.
4. Choose the YundaDesk workspace that should manage this store.
5. Explicitly confirm the connection.
6. Return to the BigCommerce control panel and select **I completed account linking**. If the page was closed, reopen **Apps → My Apps → YundaDesk** instead.

The account connection opens in a new tab and cannot run inside a third-party iframe. A BigCommerce login never grants YundaDesk workspace access by itself.

## Complete initial setup

After the connection succeeds, the YundaDesk app shows:

- **Connected** for both BigCommerce authorization and the YundaDesk workspace;
- read-only synchronization controls for Store, Customers, Orders, and Products;
- webhook subscription health;
- detected BigCommerce storefronts and their compatibility;
- Installation Guide, User Guide, and support links.

Next, [sync store data and enable storefront chat](./use-yundadesk-with-bigcommerce.md). Installing the app does not automatically load the Widget on the primary storefront; a workspace administrator must enable it explicitly.

## Installation problems

### You cannot install apps

Ask the store owner to grant the current BigCommerce user permission to install apps, or have the store owner complete the installation.

### The account connection does not open

Allow the browser to open a new tab for `app.yundadesk.com`, then select **Connect YundaDesk account** again. Do not share the connection URL with anyone else.

### The store is already connected to another workspace

A BigCommerce store can be connected to only one YundaDesk workspace at a time. Ask an administrator of the original workspace to disconnect it before you install or connect again.

### The app asks for reauthorization

The store owner must reinstall or reauthorize YundaDesk from BigCommerce. Data synchronization and storefront status checks pause until reauthorization is complete.
