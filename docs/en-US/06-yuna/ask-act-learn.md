---
title: Ask, act, and teach with Yuna
description: Use natural language to query data, complete actions, and teach AI customer service.
category: Yuna
order: 2
updated_at: 2026-08-07
---

# Ask, act, and teach with Yuna

You do not need to remember feature locations or customer numbers. Describe the goal, target, and constraints. Yuna will decide the next step from the features available in the current workspace.

## Ask questions

Examples include “How many conversations did each channel receive yesterday?” and “Which issues are handed to people most often?” Yuna answers from data you are allowed to view. When data is unavailable, it should say so rather than fill the gap with a guess.

## Perform an action

For example: “Send a Telegram message to a selected customer about the new product.” Yuna can help you choose the customer and then show a confirmation containing the recipient, channel, and exact message. The message is sent only after confirmation, followed by a real delivery result or failure reason.

When a request has an important choice, Yuna can ask with a selection card, such as **Create a draft only** or **Send after confirmation**. After selection, progress should remain visible until the next draft or confirmation card appears.

For setup changes such as connecting a channel, creating knowledge, configuring AI reception, updating branding, or inviting members, Yuna first shows a draft or validation result. It performs the change only after you confirm. Read-only questions still follow your workspace permissions.

## Teach the AI

Examples include a standard cash-on-delivery answer or a temporary holiday shipping policy. When Yuna detects that you may be teaching it, it first asks whether to enter the learning flow. Only an explicit confirmation allows Yuna to prepare a structured draft and create a learning card. Declining continues the normal conversation and creates no learning content.

For a multi-step skill, the draft includes when it applies, information to collect, handling steps, and test scenarios. After confirmation, open the skill detail to review the flow and branches and run customer scenarios.

The system creates multiple customer scenarios for normal handling, missing information, conditional branches, external capability failures, declined confirmation, and human handoff where applicable. You can run one scenario or all scenarios. Simulation does not perform real external actions. Editing a field or asking Yuna to revise the skill makes earlier results stale, so the new revision must be tested again. The skill can be enabled only when every required scenario for the current revision passes, required capabilities are available, and risk checks succeed.

Yuna does not claim that it has learned something before the learning card actually exists. After enablement, AI customer service follows the reviewed flow. If a required capability or permission becomes unavailable at runtime, the system does not bypass the check and continue.

## Capability boundaries

Order, inventory, logistics, customer records, broadcast, and similar actions require a connected app or channel. A knowledge article cannot replace live business information.
