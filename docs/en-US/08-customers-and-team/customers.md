---
title: Manage customer profiles
description: Review customer identity, channels, labels, history, and AI memory in one profile.
category: Customers and team
order: 1
updated_at: 2026-10-04
---

# Manage customer profiles

Customer profiles bring together identity, source channels, conversation history, labels, notes, and customer memory so the team understands context before replying.

## Find a customer

Open Contacts to search by name, social ID, or email, and switch between Customers and Archived. The default list shows customer, channel/source, location/language, tags, last interaction, added date, and an Actions column with View details. Email or phone appears below the name. Location and the preferred language stored in the profile appear on separate lines, localized when available. Up to two tags are shown; additional tags appear as `+N`, with their names available on hover. Added is the date the customer profile was created. Last interaction and Added use the same date format, with the full time available on hover. Use Toggle Columns to hide location/language, tags, or added date. Missing details remain empty instead of being inferred. A store-only customer with no conversation does not present a profile-sync timestamp as an interaction. A customer may use different identities across channels. YundaDesk automatically merges them only when a channel provides an exact, verified identity relationship; an email or phone number entered by a visitor in website chat is not treated as verified identity. When identity cannot be established reliably, profiles stay separate.

The Customer column provides contact filters. Channel/source and Location/language also provide structured filters. Choose has email, has phone, or no contact details; filter by messaging channel or store source; and narrow by country/region or unknown location. You can select multiple values within each group, while conditions from different groups apply together. Continue using search for names; Last interaction has no time filter. Hiding Location keeps its selected filters; use Clear all filters to return to the full list.

Select any customer row or View details in the last column to open the profile. Profiles remain available for archived customers and customers without a messaging identity. The profile is organized into Overview, Conversation history, AI memory, Store, and Linked identities tabs; cross-channel merge and unlink actions live in the final tab. Use the close button, press `Esc`, or select outside the profile to return to the list.

For an unarchived customer with a reachable messaging identity, select View conversation from the profile. On wide screens, the profile remains on the right and a narrower quick-reply panel opens beside it on the left. When space is limited, quick reply opens over the profile. Quick reply shows the customer's real conversation messages and follows the same assignment rules as Inbox: take an unassigned or AI-handled conversation first, and handle a conversation owned by another agent in Inbox. Closing quick reply or pressing `Esc` the first time closes only the quick-reply panel and keeps the customer profile open.

After the first business message on the website, Telegram, or another messaging channel, the corresponding person is added to Customers automatically. A visitor with only initialization or system events and no message interaction is not added. It may take a short time for the customer to appear; if the customer is still missing after a refresh, first confirm that the message was accepted.

## What a profile can contain

- connected channel identities and source;
- past conversations and recent interactions;
- team labels and notes;
- AI memory and follow-up items that apply only to this customer;
- order or behavior summaries from connected systems.

Profile information in both the chat sidebar and customer details shows the original name, username, user ID, email, and phone supplied by each linked channel. Only available values are shown, with their channel identified. Renaming a customer changes the main heading while keeping the original channel name visible when it differs from the heading. Contact details already shown in the main profile are not repeated; identical usernames and user IDs appear once. In the chat sidebar, device type and screen size share one row. The source row shows the channel icon and name; you do not need to open Linked identities to read these details.

Website page-view activity shows the page the customer visited. To protect privacy, parameters in the page address are not displayed.

Visible fields depend on connected channels, apps, and workspace capabilities. Order or behavior data cannot appear when no source is connected.

## Customers synchronized from stores

After you connect a store app such as Shopify, Shoplazza, or SHOPLINE, synchronized customers appear in Customers. The list initially shows the customer source; platform customer ID, order count, total spend, source status, and last source update remain available in the customer profile.

Store customers and messaging customers use the same customer profile. Even when a store customer is not linked to a website chat, social account, or another messaging identity, you can maintain basic profile fields such as name, email, phone, country/region, language, and time zone. Starting a conversation remains unavailable until a reachable messaging identity exists. Store details update after synchronization instead of refreshing every time you open the profile.

## Maintain useful context

Use labels for team organization, notes for verified facts, and customer memory for durable preferences the AI should apply. Do not record an unverified inference as fact, and avoid sensitive data that is not needed for service.

When you use customer identity management to merge a channel identity into a target customer, related store sources remain on the target profile. Later store syncs do not automatically split a confirmed manual merge. Verify the identity first because an incorrect merge affects both conversation and store context.

## Merge, archive, and restore

Members with customer data management permission can merge or archive a customer from More actions in the customer profile:

- Search for another customer and review the merge preview first. It shows channel identities, conversations, store sources, and field conflicts that will move. A confirmed merge cannot be undone.
- Archiving does not delete customer data. Choose Archived from the Customer status menu at the top of the Customers page to find and restore archived profiles; a new message from that customer may also restore the profile automatically.
- These actions are hidden without the required permission.

## Correct or delete data

Correct inaccurate labels, notes, and memory promptly. To permanently delete customer data, submit a deletion reason from the customer profile. This creates a request for approval and does not delete data immediately. Irreversible erasure starts only after admin approval. Archiving and deletion are different: an archive can be restored, while completed erasure cannot.
