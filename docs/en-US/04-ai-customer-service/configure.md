---
title: Configure AI reception
description: Select the AI source, reception channels, and response style.
category: AI customer service
order: 1
updated_at: 2026-07-17
---

# Configure AI reception

Each workspace has one customer-facing AI identity. You can select YundaDesk managed AI or a configured external AI. The selected source handles automatic replies on enabled channels.

## Choose an AI source

- **YundaDesk managed AI:** Supports the knowledge base, Yuna learning, AI skills, customer memory, and answer traces.
- **External AI:** Calls your configured external API for replies and does not participate in YundaDesk managed learning.

Switching the source does not create a second customer-facing identity. The display name that customers and agents see is managed separately from the runtime source.

## Choose reception channels

Select the connected channels that may receive automatic AI replies. Unselected channels can still receive customer messages, but the AI will not reply automatically.

## Configure response behavior

Managed AI supports role, instructions, tone, and other service preferences. When **Use emoji** is off, the AI should avoid emoji in customer replies. If the page uses autosave, wait for the saved state before leaving.

## Before going live

Verify that knowledge processing is complete, core questions pass in the Playground, answer traces use the correct sources, real channels pass inbound and outbound tests, handoff boundaries are correct, and AI usage is available.

A successful configuration is not proof of successful channel delivery. Final acceptance requires the real customer client to receive the reply.
