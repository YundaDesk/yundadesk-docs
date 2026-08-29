---
title: Choose a managed or external Agent
description: Understand the capabilities and reception boundaries of each Agent source.
category: AI customer service
order: 5
updated_at: 2026-08-29
---

# Choose a managed or external Agent

A workspace can have both managed and external Agents, but each Agent uses only one reply source. Different Agents can be bound to different channels.

## Managed AI

YundaDesk managed AI uses the knowledge base, learning review, AI skills, customer memory, and answer details. It is intended for teams that want improvement and review in one system.

## External AI

External AI uses your configured third-party AI service. It only generates replies and does not participate in managed YundaDesk learning or automatically use managed skills.

To connect an OpenAI-compatible endpoint:

1. Go to **Apps → App Store → AI Service**.
2. Select **View** on the **Custom Agent API** card.
3. Enter the endpoint, API key, and model in Reception Settings, then save.
4. Test typical replies before switching reception to external AI.

## Before binding channels

Confirm that the source is configured, test typical questions, understand which managed learning and answer-detail features are unavailable, and complete a real inbound and outbound test on a low-risk channel.

Selecting an Agent source and binding reception channels are separate actions. The Agent answers only on enabled channels that are explicitly bound to it.
