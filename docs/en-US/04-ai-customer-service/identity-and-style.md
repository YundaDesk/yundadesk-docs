---
title: Set the AI name and response style
description: Configure the customer-visible AI identity, tone, and emoji preference.
category: AI customer service
order: 4
updated_at: 2026-08-11
---

# Set the AI name and response style

The AI name is the single reception identity customers and agents see. Switching between managed and external AI does not create another employee.

## Configure the identity

1. Open AI reception settings.
2. Edit the customer-service name and choose a reception focus.
3. Add workspace-wide brand preferences under **Your instructions**.
4. Select a tone and turn emoji use on or off.
5. Edit the fallback / human-handoff message and save.

You can also tell Yuna which item to change. Yuna reads the current configuration and prepares a delta draft first. The change is applied only after confirmation, and settings you did not mention remain unchanged.

## Verify the result

Ask a typical customer question in the Playground and inspect the greeting, tone, and formatting. Then spot-check a real channel reply because channel context can affect wording.

## Reply language

AI customer service replies in the language of the customer's current message. Browser UI language, channel locale, role instructions, previous assistant replies, and source-material language do not override the current message. If the customer sends only an emoji, URL, or code, the most recent customer natural language is reused. With no usable history, the reply stays brief and language-neutral.

## Boundaries

Your instructions are supplemental preferences, not the system prompt. They do not override knowledge, safety rules, the customer's message language, or confirmation requirements. Disabling emoji changes expression, not the source of factual answers. Manage the Widget welcome message in channel settings.
