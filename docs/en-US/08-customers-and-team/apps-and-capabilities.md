---
title: Manage apps and workspace capabilities
description: Understand how apps, plugins, channels, and platform features determine what a workspace can do.
category: Customers and team
order: 3
updated_at: 2026-08-12
---

# Manage apps and workspace capabilities

Apps and plugins connect stores, CRMs, and other business systems to YundaDesk. Once ready, Yuna and AI customer service can use order, customer, inventory, and other business information when permission allows.

## Apps and channels

Channels send and receive customer messages. Apps provide business data and actions. A store app may help install the website widget, but the store itself does not become a messaging channel.

## How capabilities become available

Available workspace features depend on product features, connected channels, installed apps, and their current status. Installation alone may not be enough; authorization and required configuration must also be complete.

Use the capability center to review:

- capabilities available now;
- data sources or configuration that must be connected;
- capabilities not yet available and any supported alternative.

## YundaDesk Translation Assistant

New workspaces include **YundaDesk Translation Assistant** as an enabled app. When you turn on chat translation under Settings → Chat tools, it is used as the default translation route.

If the workspace already uses an enabled DeepL route, YundaDesk keeps that selection. When no translation app is available, YundaDesk does not save an enabled translation setting without a route. Restore or install a translation app first.

Turning off Translate visitor messages also turns off real-time translation. Viewing apps requires the View apps permission. Installing, configuring, enabling, disabling, or uninstalling apps requires Manage apps. Changing workspace chat translation requires Manage chat tools. Each agent can set Continuous translation for themselves under Chat tools.

Agent reading translation also applies to completed AI customer service replies. When a reply language differs from the agent's configured work language, the workspace offers a Translate action. AI replies are never translated automatically; an agent must request the translation. Agents can switch back to the original text that the customer actually received. This translation is for agents only and is never sent to the customer again. If translation fails for either a visitor message or an AI reply, agents can retry below the message.

## Use live business information

When Yuna or AI customer service needs an order, tracking, or customer lookup, it uses business information from apps that are connected to the current workspace and available to the current member. After store customers sync, Yuna can query their store, platform order count, and total spend. Selecting a customer before asking Yuna narrows the question to that customer. A customer without a linked messaging channel is query-only and cannot receive a private message.

Yuna serves the merchant team; AI customer service serves visitors. A customer selected on the Customers page is used only as Yuna's current customer. AI customer service can use information for the customer in the current conversation, but it cannot search other workspace customers.

Keep store credentials only in the product's secure configuration fields, and do not copy live business data into the knowledge base as a substitute for an app connection.
