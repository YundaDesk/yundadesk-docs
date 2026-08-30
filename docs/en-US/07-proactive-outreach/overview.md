---
title: Create and govern proactive outreach
description: Contact customers at the right time while respecting confirmation, cooldown, and channel safeguards.
category: Proactive outreach
order: 1
updated_at: 2026-08-30
---

# Create and govern proactive outreach

Proactive outreach prepares a message for a selected audience, time, or business condition when the customer has not just sent a new message. It differs from an automatic reply: review the audience, content, and sending result separately.

## Before you begin

- Connect the customer channel that will send the message.
- If outreach depends on orders, payments, carts, or other store changes, connect an app that provides that data.
- Confirm that the sending Agent is enabled and bound to the correct channel.
- Broadcast, segmentation, and approval also depend on member permissions. Ask a workspace administrator when the page does not show the required option.

## Prepare outreach

Tell Yuna the outcome, audience, channel, message, and constraints. For example: “Prepare a follow-up for customers who stop replying for 30 minutes after asking about a product. Limit it to once per customer every 24 hours and let me review it first.”

Yuna asks for missing information and shows a draft or message preview that you can review. Nothing is enabled or sent before confirmation. If required data, channel access, or permission is missing, the page shows why it was not executed or is unavailable. Correct that issue before continuing.

For a one-off birthday greeting or product reminder to one identified customer, ask Yuna to prepare the message, check the customer and channel, and confirm before sending. A one-off message does not need an Automation.

## Repeat customer outreach

Use [Yuna Automations](../06-yuna/automations.md) when prepared outreach should run on demand, every day, on weekdays, or every week:

1. Open **Yuna → Automations**, open the menu beside **Create**, and select **Set up manually**.
2. If **Customer outreach** is available, select it and the executing Agent. Select existing outreach when it is ready. Otherwise, select **Prepare customer outreach with Yuna**, confirm the audience, channel, message, and sending limits, then return to the Automation setup.
3. Select the frequency and save the draft.
4. Review the details and activate the Automation.

**Create with Yuna** creates workspace-task Automations; it does not create customer outreach.

Reaching the scheduled time does not send directly to customers. Every run first freezes the audience, channel, recipient count, and message, then waits for an authorized member to approve or reject it.

## Check before sending

Before approval, verify:

- the audience and actual recipient count;
- the channel and sending Agent;
- the accuracy of campaign details, prices, and commitments;
- whether an opt-out, do-not-disturb setting, quiet hours, or frequency limit applies;
- that the Automation and channel are still available.

Approval cannot expand a frozen audience. A recipient may still be removed before real delivery if they opt out, enter do-not-disturb, exceed a frequency limit, or lose channel availability.

## View the result

Open **Run history** for the Automation and first check whether the run is waiting for approval, succeeded, failed, or was cancelled. After approving outreach, select **View send details** in the result to open the customer-outreach sending history under Automations, then review target, sent, suppressed, failed, delivered, read, and reply results.

**Sent** means the message entered the sending flow. Only a **Delivered** or **Read** result from the channel confirms that stage. When a channel does not provide those receipts, the page shows them as unavailable; do not infer that the customer received the message.
