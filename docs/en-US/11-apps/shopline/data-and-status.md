---
title: SHOPLINE store data, permissions, and connection status
description: Understand SHOPLINE read-only access, separate store data and storefront chat statuses, and check orders in customer conversations.
category: Apps and integrations
order: 3
updated_at: 2026-10-02
---

# SHOPLINE store data, permissions, and connection status

SHOPLINE shows separate **Store data** and **Storefront chat** statuses. A connected data status confirms the authorized connection. Chat display and message delivery need their own checks.

## What the app can read

| Read-only access | Purpose |
|---|---|
| Store information | Identify the store and its address |
| Customers | Provide customer information that can be associated with support requests |
| Orders | Look up order, payment, line-item, and fulfillment information |
| Products | Provide product and variant context for customer service |

These permissions do not grant refunds, order cancellation, address changes, or inventory changes. Read access also does not mean every resource has a separate store-wide management page or that all historical data has finished syncing.

## View connection status

In YundaDesk, open **Apps → SHOPLINE → View store status**. Check the store address before interpreting either status.

| Display | Meaning and next step |
|---|---|
| Store data: Connected | The authorized data connection is available; still verify the actual order you need |
| Store data: Reauthorization required | Follow the prompt using an account with the required permissions |
| Store data: Connection issue | Test the connection, note the displayed message, and follow troubleshooting |
| Storefront chat: Not checked yet | No completed storefront check; enable chat in the theme, then open and check the storefront |
| Storefront chat: Checking | The current check is in progress; keep the storefront page open |
| Storefront chat: Embedded | Chat loaded during this check; next test message delivery |
| Storefront chat: Last check passed | An earlier check succeeded; this is not a new check of the current visit |
| Storefront chat: Embed not detected | Chat was not detected during this check; check the theme, saved settings, and store access |
| Storefront chat: Restore connection first / Configuration issue | Resolve the connection or configuration prompt before checking again |

## What each button checks

- **Test connection** checks store data access. Success does not mean the chat entry is visible.
- **Open store and check** opens the store and checks chat loading. Test actual messages afterward.
- **Refresh status** reads the latest status. It does not turn on or save the app embed in SHOPLINE.

## View orders in a customer conversation

1. Open the customer's conversation in the **Inbox**.
2. Find the orders area in the customer panel on the right and check the store source.
3. When a customer email and orders can be matched, review the returned order status, amount, items, and fulfillment information.
4. If nothing matches, check that the customer supplied the email used for the order, then review the store connection and any error shown.

Opening chat as an anonymous visitor does not automatically associate that visitor with a store customer's orders. Missing order information does not mean theme chat installation failed. Do not expose another customer's order information in public conversations or screenshots.

Installation also does not configure AI reception or automated payment reminders. Complete those tasks through their own available settings and capabilities. For a specific problem, see [Troubleshooting and connection management](./troubleshooting-and-lifecycle.md).
