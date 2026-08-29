---
title: Complete common tasks with Yuna
description: Give Yuna a clear goal, target, and constraints for queries, setup, teaching, and follow-up.
category: Yuna
order: 7
updated_at: 2026-08-28
---

# Complete common tasks with Yuna

Tell Yuna the goal, target, time range, and constraints. You do not need to remember feature names. Use these examples according to the channels, apps, and permissions available in the current workspace.

## Ask how to use YundaDesk

Ask questions such as “Where do agents use a saved team quick reply?”, “How do I verify Telegram after connecting it?”, or “Why is confirmation required before changing settings?”. Yuna consults the current published help for navigation, steps, prerequisites, expected effects, and verification.

When no matching guidance exists, Yuna should say so instead of guessing. Product help explains how YundaDesk works; it does not prove what is configured in the current workspace. Ask Yuna to inspect the relevant object when you need the current channel, member, or setting state.

After reading the steps, you can continue with “Set that up for me.” Yuna switches to the corresponding action, collects missing information, and shows a draft or confirmation. Asking for instructions alone does not create a draft or change settings.

## Ask about the business

- “Summarize the most common handoff reasons from the last seven days and group them by cause.”
- “Compare yesterday's conversation volume and AI participation by channel.”
- “List our current quick replies and tell me which ones are disabled.”
- “Which custom fields are configured for customer profiles?”
- “Which knowledge sources exist, and which ones have not finished indexing?”
- “Inspect the knowledge, channels, and capabilities that are actually effective for AI customer service, and explain any blockers.”
- “Is knowledge retrieval enabled for the current AI customer service, and which phone-number FAQs can participate in answers?”
- “Preview how AI customer service answers ‘What is your phone number?’ without sending anything to a customer.”
- On a customer or conversation page, select **Current page**, then ask: “Summarize the main needs from this customer's recent conversations.”

Results use only data the current member may view. Quick-reply, custom-field, and knowledge-source queries read existing configuration without creating or changing it. Yuna should explain the limitation when report, customer, knowledge, channel, or settings access is missing. AI customer-service inspection reports the knowledge scope, bound and ready channels, and capabilities that are actually effective instead of only repeating a saved settings value. Knowledge inspection further distinguishes the overall switch, bound sources, and each FAQ's answer-participation state. A preview uses the current AI customer-service configuration and returns run evidence, but it creates no customer message. A channel marked ready means its configuration conditions are met; it does not prove that a particular customer conversation received a message. Verify real delivery through the Widget or customer channel.

## Get help with setup

- “Help me prepare a Telegram connection and tell me what information I need.”
- “Prepare knowledge settings for the new return policy and let me review them first.”
- “Make the AI customer service tone more concise without changing the refund policy.”
- “Rename customer service to Global Support, set the reception focus to pre-sales, and turn off emoji. Keep every other setting unchanged.”
- “Add this to Your instructions: collect an email for high-value orders. Show me the confirmation before applying it.”
- “Add a refund-status quick reply and show me the content before saving it.”
- “Add a membership-tier customer field and create a high-value customer tag.”
- “Assign the high-value tag to the current customer and add the note ‘Prefer email contact.’ Let me confirm first.”
- “Bind the returns and shipping knowledge sources to the current AI customer service. Keep other knowledge settings unchanged.”
- “Automatically translate incoming English messages and close conversations after 30 minutes of inactivity.”
- “Turn off AI reception for the website channel, enable automatic assignment, and use only the selected agents.”
- “Set support hours to 9:00–18:00 on weekdays in the Singapore time zone, with an offline message.”
- “Change an existing agent's display name and set the concurrent conversation limit to 8. Let me confirm first.”

A request that changes settings should read the current configuration first, then show a draft, choice, or confirmation. No real change occurs before confirmation. Yuna can help configure AI customer service, bind knowledge sources, manage quick replies, customer fields and the tag catalog, assign existing tags or notes to a selected customer, configure agent translation and auto-close tools, channel reception and assignment, welcome copy, business hours, offline messages, and an existing member's display name, role, or concurrent conversation limit. Disable or delete a member from member settings instead. Actions always follow current permissions; they stop when the required permission is revoked or the account is disabled. After confirmation, inspect the action receipt and, when needed, verify the corresponding settings page.

## Teach and correct the AI

- “Use this temporary policy for holiday shipping questions and stop using it on the specified date.”
- “This answer treated a customer preference as a global rule. Make it apply only to the current customer.”
- “Use these repeated questions I am providing to prepare a suggestion for review.”

Teaching requests become improvement suggestions. One conversation does not directly change answers for every customer.

After confirming a correction to an existing FAQ, ask Yuna to preview the same question first. Final acceptance should still ask again through the Widget or a real customer channel and compare the customer-visible answer with the preview.

## Contact customers and plan outreach

- “Prepare a follow-up draft for the current customer, but do not send it.”
- “Design a follow-up rule for customers who stop replying for 30 minutes, starting with confirmation for each message.”
- “List the current marketing plans, then send the VIP launch plan.” Yuna reads the existing plan list first; it does not ask you for an internal ID or guess the plan.
- Open the previous outreach failure in Yuna tasks to review why it was not sent.

Sending requires an available channel, a clear target, and the necessary permission. Broadcast, segmented, or automatic sending normally requires stricter confirmation and safety conditions. A technical failure does not mean a message was sent or a human handoff occurred; without a real receipt, treat it as failed and review the reason.

Enabling proactive outreach or changing quiet hours and frequency limits only updates pre-send safety policy. It does not create a marketing plan or send a message. A real send still shows the audience and content for separate confirmation, and only a delivery receipt proves it was sent.

## Review tasks and results

Open the Yuna task area to review learning suggestions, AI failures, channel delivery failures, and proactive outreach items. Select a task card to open its details, then use the available review, confirmation, or retry action.

Yuna saying “completed” does not replace an action receipt or real channel result. Inspect the receipt for important actions and verify outbound messages in the customer's real channel.

## Write a clearer request

A useful structure is: **goal + target + time range + constraints + expected next step**.

For example: “Summarize Telegram handoff reasons from the last 30 days. Use only data I can access, give the conclusion and three actionable recommendations first, and do not change any settings.”
