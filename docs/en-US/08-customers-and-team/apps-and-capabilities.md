---
title: Manage apps and workspace capabilities
description: Understand how apps, plugins, channels, and platform features determine what a workspace can do.
category: Customers and team
order: 3
updated_at: 2026-10-09
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

Agent reading translation also applies to completed AI customer service replies. When a reply language differs from the agent's configured work language, the workspace offers a Translate action. AI replies are never translated automatically; an agent must request the translation. After translation, the same bubble shows the original text above the translation, separated by a line. Select Hide translation to collapse it and Show translation to restore it; the original always stays visible. Existing translations are shown again after refreshing the page. This translation is for agents only and is never sent to the customer again. If translation fails for either a visitor message or an AI reply, the original stays visible and agents can retry below the message.

## Let an Agent use connectors

Open **AI Agents → Connectors** from the sidebar or **Apps → Self-service → Connectors**. Viewing requires View apps; configuration and testing require Manage apps. Workspaces without access see an upgrade prompt.

Use the Google Public DNS and Microsoft Learn example connections in the list to try the test workflow without entering credentials. Select the DNS lookup and enter `example.com`, or select the MCP documentation search and enter a question about a Microsoft product, then inspect the real response. You can edit, disable, or delete these examples; deleted examples are not automatically restored. To let an Agent use one, select its function in that Agent’s connector settings.

1. Select **Add**, choose API or MCP, and save the connection name, address, and authentication details. Enter credentials only in connection settings.
2. For an API connection, add a function and configure its request, inputs, and outputs. Inputs can come from the conversation, a fixed value, or the current customer's attributes. Enable customer identity requirements when your use case involves customer-specific data.
3. For MCP, select **Discover MCP tools** in connection settings, choose the tools you need, and save. Select a tool to inspect its details, configure usage rules, and test it.
4. Save your configuration, enter inputs in the test panel, and review the result. On narrow screens, use **Test function** to open the panel. Both queries and write operations send real requests. Write tests change external data, so use test data. If the result is uncertain, check the external system before testing again.
5. Open the target Agent's **Connectors** tab, enable connectors, and select the functions it may use. Select an entire connection or expand it to choose individual functions.
6. Ask a related question in the Agent's debug preview, then check **Call history** in Connectors to confirm the call succeeded.

Enabling the switch does not grant access to every tool. If a configuration change invalidates a selection, select the function again. A successful test does not grant Agent access.

**What the Agent receives** shows the returned content; for APIs, it includes only configured output fields. Test again after changing the configuration. After a successful test, select **Configure Agent**, choose the target Agent, check whether this function is authorized, and open its **Connectors** tab. This shortcut does not grant access automatically. Retry if the access status cannot be loaded. If a test fails, follow the guidance to check connection settings or parameters. For an uncertain write, check the result in the external system first.

After a write function is selected, the Agent follows its usage instructions and the business steps in its skills without a separate staff approval setup. Describe the required information and execution conditions for actions that change data.

Select **View details** below a test reply to see the connector call status and whether its result was used in the final answer. New calls also show the connection and function names, duration, and returned field count. A completed call does not necessarily mean its result was used. If the result is incomplete or unconfirmed, check the connector call history and avoid repeating a write operation. Older records may not have a detailed summary.

### Configure requests and parameters

- **POST queries:** Some read APIs require POST. After choosing POST, enable **Read-only** only when the endpoint does not change data. Save it to run a real test and authorize it for your agent. Leave Read-only off for endpoints that change data.
- **Objects and arrays:** Choose the request body as the parameter location and an object or array JSON type to send nested structures. Enter valid JSON for fixed and test values, such as `{"status":["paid"]}`. Describe the expected fields, values, and structure so the agent can collect suitable input.
- **Request headers:** Configure ordinary application headers as input parameters, for example an API version, language, or business scope. Enter API keys and tokens in the connection authentication section. For a custom authentication header, use the name required by the service. Do not put credentials in parameter descriptions or fixed values.
- **Response fields:** Query functions need selected response fields that the agent may read. Choose fields for writes as needed; leave them empty if the endpoint returns no content. Check the returned values before authorizing the function for an agent.

### Verify write results (optional)

You can normally use the business status in the response to understand the result without adding a separate query. If you need an additional check, expand **Result verification (optional)**, select a read-only function in the same connection, and configure its inputs and expected result.

A successful request does not necessarily mean an order has been fulfilled or a refund has arrived. Use the business status returned by the external system. With verification configured, the agent can check the original operation when its result is uncertain; it confirms success only when the query matches the expected result. Without verification, or when the query remains inconclusive, check the external system. “Not yet confirmed” does not mean “not executed.”

If the external service supports `Idempotency-Key` or `X-Idempotency-Key`, select its **Idempotency header** to prevent the same operation from taking effect twice. The system generates an operation key by default. To identify the same business operation across conversations, set **Business identifier input (optional)** to a required text parameter, such as a refund reference. The same identifier must always represent the same operation: an order number may be unsuitable when an order can have multiple refunds. Check the external service’s idempotency rules and retention period first.

If the query accepts the operation key, choose **Operation idempotency key** as the verification parameter’s source. You can also use an original request parameter or a returned field. If the query requires an identifier available only in the response, verification may be impossible when that response is lost.

### When a function cannot be selected

Expand a connection in the agent's **Connectors** tab to see each function's status. Disabled connections, functions with missing credentials, and query functions with no selected response fields show an explanation and cannot be selected. Complete the configuration in Connectors first. If a previously authorized function changes, select it again when prompted, then verify it in the agent preview.

## Use live business information

When Yuna or AI customer service needs an order, tracking, or customer lookup, it uses business information from apps that are connected to the current workspace and available to the current member. After store customers sync, Yuna can query their store, platform order count, and total spend. Selecting a customer before asking Yuna narrows the question to that customer. A customer without a linked messaging channel is query-only and cannot receive a private message.

Yuna serves the merchant team; AI customer service serves visitors. A customer selected on the Contacts page is used only as Yuna's current customer. AI customer service can use information for the customer in the current conversation, but it cannot search other workspace customers.

Keep store credentials only in the product's secure configuration fields, and do not copy live business data into the knowledge base as a substitute for an app connection.
