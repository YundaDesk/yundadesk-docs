---
title: Ask, act, and teach with Yuna
description: Use natural language to query data, complete actions, and teach AI customer service.
category: Yuna
order: 2
updated_at: 2026-08-01
---

# Ask, act, and teach with Yuna

You do not need to know internal tool names or customer IDs. Describe the goal, target, and constraints. Yuna will inspect current capabilities and decide the next step.

## Ask questions

Examples include “How many conversations did each channel receive yesterday?” and “Which issues are handed to people most often?” Yuna calls available read-only tools and returns the result. When data is unavailable, it should say so rather than fill the gap with a guess.

## Perform an action

For example: “Send a Telegram message to a selected customer about the new product.” Yuna can help you choose the customer and then show a confirmation containing the recipient, channel, and exact message. The message is sent only after confirmation, followed by a real delivery result or failure reason.

When a request has an important choice, Yuna can ask with a selection card, such as **Create a draft only** or **Send after confirmation**. After selection, progress should remain visible until the next draft or confirmation card appears.

For setup changes such as connecting a channel, creating knowledge, configuring AI reception, updating branding, or inviting members, Yuna first shows a draft or validation result. It performs the change only after you confirm. Read-only questions still follow your workspace permissions.

## Teach the AI

Examples include a standard cash-on-delivery answer or a temporary holiday shipping policy. Yuna classifies the request as knowledge, a temporary skill, a multi-step skill, customer memory, or proactive outreach, then creates a learning card for review.

## Capability boundaries

Order, inventory, logistics, CRM, broadcast, and similar actions require a connected tool. A knowledge article cannot replace a live business-data capability.
