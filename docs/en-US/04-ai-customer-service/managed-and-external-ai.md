---
title: Choose a managed or external Agent
description: Understand the capabilities and reception boundaries of each Agent source.
search_terms: own AI, external AI, service provider, whitelabel
category: AI customer service
order: 5
updated_at: 2026-10-09
---

# Choose a managed or external Agent

A workspace can have both managed and external Agents, but each Agent uses only one reply source. Different Agents can be bound to different channels.

## Managed AI

YundaDesk managed AI uses the knowledge base, learning review, AI skills, customer memory, and answer details. It suits teams that want to improve and review answers in one place.

## Your own AI

Before connecting, check **Settings → Subscription** to confirm whether the workspace supports your own AI. Refer to the product and third-party service for current charges and allowances.

External AI generates replies through your third-party endpoint. It does not participate in managed YundaDesk learning or automatically use managed skills. Maintain its persona, knowledge, and reply language in the third-party service.

## Create an external Agent

1. Open **Agents** and select **New Agent**.
2. Enter an Agent name and select **External AI**.
3. Enter an OpenAI-compatible endpoint, API key, and optional model, then select **Create draft**.
4. In the new Agent's **External setup**, verify the connection and test typical questions before enabling the Agent and binding reception channels.

If the page says your current plan does not support this option, follow the prompt to review available plans. The endpoint must support OpenAI Chat Completions. A platform name such as Dify does not mean its native API is directly compatible; provide a compatible endpoint.

To update an endpoint or key later, open the Agent's **External setup** and select **Edit external AI**. Leave the API key blank to retain the saved key. Reopen the configuration to verify the endpoint and key status; the plaintext key is never displayed. Subsequent replies use the updated configuration, so disable an active Agent before testing changes.

## Reception after a downgrade

If your plan no longer includes your own AI, external reception pauses and your configuration is retained. The system does not automatically switch to managed AI. Upgrade to restore access, or create a managed Agent and reassign the reception Agent in channel settings.

## Service providers using only their own AI

Service providers can also choose external Agents. Check each workspace's subscription page for external AI and branding entitlements. Contact sales for bulk arrangements.

## Before binding channels

Verify the endpoint, test typical questions, and complete a real inbound and outbound test on a low-risk channel. Selecting an Agent source and binding channels are separate actions. Only enabled channels explicitly bound to the Agent enter automatic reception.
