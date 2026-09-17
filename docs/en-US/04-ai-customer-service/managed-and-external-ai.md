---
title: Choose a managed or external Agent
description: Understand the capabilities and reception boundaries of each Agent source.
search_terms: own AI, external AI, service provider, whitelabel, Pro, credit
category: AI customer service
order: 5
updated_at: 2026-09-13
---

# Choose a managed or external Agent

A workspace can have both managed and external Agents, but each Agent uses only one reply source. Different Agents can be bound to different channels.

## Managed AI

YundaDesk managed AI uses the knowledge base, learning review, AI skills, customer memory, and answer details. Billable managed AI capabilities continue to use AI Credits.

## Your own AI: Pro and Enterprise

Pro and Enterprise support connecting your own AI within an Agent. External reception has no additional charge and does not consume YundaDesk AI Credits. You pay your third-party AI provider directly. Seats and channels keep their existing free policy; managed AI continues to use AI Credits.

External AI generates replies through your third-party endpoint. It does not participate in managed YundaDesk learning or automatically use managed skills. Maintain its persona, knowledge, and reply language in the third-party service. YundaDesk passes customer messages and conversation history without adding platform instructions or reply rules.

## Create an external Agent

1. Open **Agents** and select **New Agent**.
2. Enter an Agent name and select **External AI**.
3. Enter an OpenAI-compatible endpoint, API key, and optional model, then select **Create draft**.
4. In the new Agent's **External setup**, verify the connection and test typical questions before enabling the Agent and binding reception channels.

Free and Starter users can select external AI and are prompted to upgrade to Pro. The endpoint must support OpenAI Chat Completions. A platform name such as Dify does not mean its native API is directly compatible; provide a compatible endpoint.

To update an endpoint or key later, open the Agent's **External setup** and select **Edit external AI**. Leave the API key blank to retain the saved key. Reopen the configuration to verify the endpoint and key status; the plaintext key is never displayed. Subsequent replies use the updated configuration, so disable an active Agent before testing changes.

## Reception after a downgrade

If your plan no longer includes your own AI, external reception pauses and your configuration is retained. The system does not automatically switch to managed AI or start charging Credits. Upgrade to restore access, or create a managed Agent and reassign the reception Agent in channel settings. Managed reception uses AI Credits.

## Service providers using only their own AI

Service providers can use the omnichannel inbox and workspace with their own AI on Pro or Enterprise, without using managed AI for customer replies. External reception does not add a per-call fee. Branding and customer workspace entitlements follow each workspace's subscription; one subscription does not imply coverage for every customer workspace. Contact sales for bulk arrangements.

## Before binding channels

Verify the endpoint, test typical questions, and complete a real inbound and outbound test on a low-risk channel. Selecting an Agent source and binding channels are separate actions. Only enabled channels explicitly bound to the Agent enter automatic reception.
