---
title: Manage apps and workspace capabilities
description: Understand how apps, plugins, channels, and platform features determine what a workspace can do.
category: Customers and team
order: 3
updated_at: 2026-08-01
---

# Manage apps and workspace capabilities

Apps and plugins connect stores, CRMs, and other business systems to YundaDesk. Once ready, they can provide order, customer, inventory, or other tool capabilities to the current workspace.

## Apps and channels

Channels send and receive customer messages. Apps provide business data and actions. A store app may help install the website widget, but the store itself does not become a messaging channel.

## How capabilities become available

Workspace capabilities are calculated from platform features, connected channels, installed apps, and plugin declarations. Installation alone may not be enough; authorization, configuration, and dependent tools must also be ready.

Use the capability center to review:

- capabilities available now;
- data sources or configuration that must be connected;
- capabilities not yet available and any supported alternative.

## YundaDesk Translation Assistant

New workspaces include **YundaDesk Translation Assistant** as an enabled app. When you turn on chat translation under Settings → Chat tools, it is used as the default translation route.

If the workspace already uses an enabled DeepL route, YundaDesk keeps that selection. When no translation app is available, YundaDesk does not save an enabled translation setting without a route. Restore or install a translation app first.

Turning off Translate visitor messages also turns off real-time translation. Viewing apps requires the View apps permission. Installing, configuring, enabling, disabling, or uninstalling apps requires Manage apps. Changing chat translation also requires Manage chat tools.

## Tool-backed requests

When Yuna or AI customer service needs an order, tracking, or customer lookup, it calls a ready workspace tool. Permission is checked again at execution time. The AI does not hold store secrets, and live business data should not be copied into the knowledge base as a substitute for a tool.
