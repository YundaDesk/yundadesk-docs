---
title: Set the AI name and response style
description: Configure the customer-visible AI identity, tone, and emoji preference.
category: AI customer service
order: 4
updated_at: 2026-08-23
---

# Set the AI name and response style

The AI name is the single reception identity customers and agents see. Switching between managed and external AI does not create another employee.

## Configure the identity

1. Open AI reception settings and select **General**.
2. Edit the customer-service name and choose a reception focus.
3. Add workspace-wide brand preferences under **Your instructions**.
4. Select a tone and turn emoji use on or off.
5. Turn on **Deep reasoning** if the AI should analyze more thoroughly before replying. Customers never see the reasoning process, and replies may take longer.
6. Turn on **Progressive replies** if one answer should arrive as several natural messages organized by meaning.
7. To edit the online-queue and no-agents-online messages, switch to **Handoff**, then save.

You can also tell Yuna which item to change. Yuna reads the current configuration and prepares a delta draft first. The change is applied only after confirmation, and settings you did not mention remain unchanged.

## Verify the result

Ask a typical customer question in the Playground and inspect the greeting, tone, and formatting. With **Progressive replies** enabled, the Playground also shows the ordered reply as separate bubbles without sending those test messages to a customer. Then spot-check a real channel reply because channel context can affect wording.

After enabling **Deep reasoning**, open the Trace for that reply. It should show a **Deep reasoning** step with a **Trace only** label. Even when there is no reasoning text to display, Trace still shows that deep reasoning was enabled for the reply. Customers always see only the final answer.

With **Progressive replies** enabled, AI customer service can send two or three messages with distinct meaning when the answer naturally supports it—for example, a direct conclusion followed by conditions or the next step. It does not add empty updates such as “please wait” or “checking now” just to create more messages. When the setting is off, each turn sends one final reply. If the customer continues typing, the AI still restarts from the latest message; that reliability behavior does not depend on this setting.

## Reply language

AI customer service replies in the language of the customer's current message. Browser UI language, channel locale, role instructions, previous assistant replies, and source-material language do not override the current message. If the customer sends only an emoji, URL, or code, the most recent customer natural language is reused. With no usable history, the reply stays brief and language-neutral.

## Boundaries

Your instructions are supplemental preferences, not the system prompt. They do not override knowledge, safety rules, the customer's message language, or confirmation requirements. Disabling emoji changes expression, not the source of factual answers. Manage the Widget welcome message in channel settings.
