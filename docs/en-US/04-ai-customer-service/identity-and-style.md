---
title: Set an Agent name and response style
description: Configure the customer-visible name, tone, and emoji preference for one Agent.
category: AI customer service
order: 4
updated_at: 2026-08-28
---

# Set an Agent name and response style

Each Agent has its own customer-visible name and response preferences. Editing one Agent does not overwrite another Agent.

## Configure the identity

1. Open **AI Agents** and select the target Agent.
2. Under **Role**, edit the name and confirm the Role.
3. Add workspace-wide brand preferences under **Your instructions**.
4. Select a tone and turn emoji use on or off.
5. Turn on **Deep reasoning** if the AI should analyze more thoroughly before replying. Customers never see the reasoning process, and replies may take longer.
6. Turn on **Progressive replies** if the AI should send a confirmed stage result before continuing with another required stage of the same request.
7. To edit the online-queue and no-agents-online messages, switch to **Handoff**, then save.

You can also tell Yuna which setting to change for a named Agent. Yuna confirms the target and prepares a delta draft first. The change is applied only after confirmation, and settings you did not mention remain unchanged.

## Verify the result

Ask a typical customer question with **Test conversation** on the **AI Agents** page and inspect the greeting, tone, and formatting. To verify **Progressive replies**, use a request that genuinely requires more than one available business step. Test conversation shows each confirmed stage in order without sending those test messages to a customer; ordinary replies still appear as one bubble. Then spot-check a real channel reply because channel context can affect wording.

After enabling **Deep reasoning**, open the Trace for that reply. It should show a **Deep reasoning** step with a **Trace only** label. Even when there is no reasoning text to display, Trace still shows that deep reasoning was enabled for the reply. Customers always see only the final answer.

With **Progressive replies** enabled, AI customer service sends an early message only after it has a confirmed stage result and the same request still needs further work. An ordinary answer, a single clarification, or a turn without a confirmed stage result still sends one final reply. It does not add empty updates such as “please wait” or “checking now” just to create more bubbles. When the setting is off, each turn sends one final reply. If the customer continues typing, the AI still restarts from the latest message; that reliability behavior does not depend on this setting.

## Reply language

AI customer service replies in the language of the customer's current message. Browser UI language, channel locale, role instructions, previous assistant replies, and source-material language do not override the current message. If the customer sends only an emoji, URL, or code, the most recent customer natural language is reused. With no usable history, the reply stays brief and language-neutral.

## Boundaries

Your instructions are supplemental preferences, not the system prompt. They do not override knowledge, safety rules, the customer's message language, or confirmation requirements. Disabling emoji changes expression, not the source of factual answers. Manage the Widget welcome message in channel settings.
