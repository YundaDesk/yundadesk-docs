---
title: View Yundastore carts and create a recovery discount
description: Check store and conversation carts, understand their status, and create a recovery discount through preview and approval.
category: Apps and integrations
order: 1
updated_at: 2026-10-01
---

# View Yundastore carts and create a recovery discount

Before you begin, make sure the Yundastore app is installed, store data access is authorized for the correct store, and storefront chat is enabled. Staff need permission to view app data and the conversation. Creating and approving a discount require their respective permissions.

## View store carts

1. In YundaDesk, open **Store data → Carts** and select the store you want to check.
2. Add a product on the storefront. The open cart list updates automatically; you can also select **Refresh** and check when the page was last checked.
3. Open the matching cart and check the product names, quantities, SKUs (when available), subtotal, and currency. Shipping and taxes may be added later at checkout.

You can add to the cart before starting a Widget conversation, or start the conversation first and add to the cart afterward. Normal use does not require opening the storefront cart page or refreshing the storefront. The conversation sidebar shows a current cart only after a conversation with that same visitor has been established. The store-wide list can show a cart before the visitor starts chatting.

## View the current conversation cart

1. Have the visitor open the Widget on the same store and send a message.
2. Open that conversation in YundaDesk and find **Current cart** in the **Store orders** sidebar.
3. Change a quantity, remove an item, or empty the cart on the storefront, then check the sidebar. It updates while the page is in the foreground; you can also select **Refresh cart**.

After a customer signs out and another signs in, check the new customer's own conversation. Do not treat items from the previous conversation as the new customer's cart.

| Displayed state | Meaning and next step |
|---|---|
| Not linked | The conversation exists, but a current cart has not been confirmed. Change the cart on this store and check again. |
| Syncing | A cart is linked and store data is still arriving. Check the update time shortly. |
| Empty | The current cart has been confirmed to contain no items. |
| Expired | Older cart information is no longer displayed as current. Have the visitor continue using the store and check again. |
| Unsupported | This store connection cannot currently supply a conversation cart. Check the app connection status. |
| Unavailable or access denied | Check the selected store, conversation permissions, and app authorization. Retry a temporary failure later. |
| Removed or cleared | The cart is no longer available. Do not use its previously displayed items. |

If a refresh fails, the page may say it is showing the last successfully received data. Do not treat that as the current store state. Check the connection and authorization, then retry.

## Create a recovery discount

1. Open the cart in **Store data → Carts** and select **Create recovery discount**.
2. Review the allowed discount types, amount or percentage limits, currency, expiry, and use limit. Enter a code and the requested values.
3. Select **Preview in store and request approval** and check the store's target, discount details, and risk notice. If the cart or conditions change, prepare and preview again.
4. A person with approval permission reviews the pending action independently and approves or rejects it.
5. After approval, keep checking the action status. Treat the discount as created only when the store readback confirms success. If the result is still being checked, wait instead of submitting it again.

Creating a discount does not send a message to the visitor or mean that checkout is complete. Completed or cleared carts show that a recovery discount cannot be created; the action is also unavailable without creation permission. Follow the page guidance if the cart is missing, authorization has expired, or the store is temporarily unavailable. A temporary read failure does not prove that the cart was deleted.
