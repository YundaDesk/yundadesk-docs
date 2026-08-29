---
title: Create and govern proactive outreach
description: Contact customers at the right time while respecting confirmation, cooldown, and channel safeguards.
category: Proactive outreach
order: 1
updated_at: 2026-08-28
---

# Create and govern proactive outreach

Proactive outreach prepares or sends a message based on an event, time, or audience condition when the customer has not just sent a new message. It is not a normal auto-reply or a renamed FAQ.

## Create a rule

Tell Yuna the business outcome, for example: “If a customer stops replying for 30 minutes after asking about a product, prepare a follow-up draft, at most once per customer every 24 hours.” Yuna organizes the trigger, action, channel, and cooldown, then creates a learning suggestion.

Rules based on cart, payment, order, or other store changes require a connected app that provides that information. Without a real information source, keywords alone must not trigger the rule.

Yuna first checks whether the current workspace has the required event, customer-query, audience-segmentation, and sending-channel capabilities. If anything is unavailable, Yuna replies with **Not executed**, names the missing capability, and explains where to enable it. No plan proposal, confirmation task, or message is created, and the conversation must not end with a blank response.

When Marketing is available in the workspace, open **Workspace**, select **Marketing**, and then select **New marketing plan**. First choose the responsible Agent. The picker lists only Agents with bound reception channels and shows the channels available to that Agent. YundaDesk then opens the real Yuna conversation. Yuna asks one necessary question at a time to collect the plan name, audience, channel, message, trigger, and frequency limit, then shows the complete preview in the conversation. You do not enter a separate marketing goal. Editing an existing plan still uses the structured form: enter filters for a dynamic audience, or search the customer directory and select the current page or individual customers across pages for a fixed list. You never need to type customer names one by one. Yuna then shows a change preview. Before explicit confirmation, no change is saved, no proposal is created, and nothing is enabled or sent. Confirmation starts the next review step; it does not mean the plan is active.

A one-off birthday greeting or product reminder to one customer is a marketing execution, but it does not create a plan. After confirmation, YundaDesk checks explicit opt-out, quiet hours, frequency limits, and channel readiness. The AI customer-service identity bound to that channel sends the message, and the execution appears once in Marketing history. An unrecorded marketing-consent value does not block sending; an explicit decline or unsubscribe still produces **Not sent**. If a required channel or app capability is unavailable, Yuna shows **Not executed** with a configuration prompt. Neither failure is reported as sent.

Daily, weekly, and other recurring plans can first be organized as reviewable drafts. Whether a draft can be enabled still depends on timezone, audience segmentation, channel, frequency control, and scheduling readiness. If any capability is not ready, YundaDesk shows that gap instead of claiming the plan is scheduled.

## Operating modes

Outreach may run in observation, per-message confirmation, or automatic mode. Available modes depend on current configuration and risk. Start with observation or confirmation, then consider automatic sending only after reviewing real behavior.

## Safeguards

Before sending, YundaDesk checks workspace enablement, channel readiness, explicit opt-outs, quiet hours, cooldown, duplicate outreach, and customer memory. Missing marketing-consent data is not a blocker. Any other failed safeguard blocks the send and records the reason.

## View the result

Marketing plan details, Yuna tasks, and delivery details explain what triggered, which action was selected, why it was blocked, and whether the channel delivered it. Broadcast and segmented outreach are higher-risk and normally require a draft and confirmation; the plan shows its current readiness and any missing requirement.

For a running marketing plan, **Prepare to send** stays on the Marketing page and does not send immediately. The page lists the currently eligible customer names with pagination and shows the number matched, eligible, and filtered out. **Freeze audience and review** then freezes the complete audience, channel, recipient count, and final message for the confirmation step. The audience is not expanded or recalculated after confirmation. Before real delivery, YundaDesk checks explicit opt-outs, quiet hours, frequency limits, plan state, and channel readiness again, so the final recipient count may only decrease. Missing dynamic filters, an empty fixed list, no eligible recipients, or an unavailable channel stops the send with a visible reason. Confirmed batches appear in Marketing history.

In **Workspace → Marketing**:

- **Marketing plans** lists the responsible Agent, plan status, version, and recent use. Plan details organize trigger rules, target audience, message content, send settings, execution readiness, and recent performance.
- **Marketing history** lists one-off outreach, suppressed, preview-only, triggered, sent, partially completed, delivered, read, and failed results in time order. One confirmed batch appears as one history record with target, sent, suppressed, failed, delivered, read, replied, and confirmed-payment counts. Details open in a centered dialog; **Open conversation** navigates to the conversation without automatically opening its AI reply details.

Viewing the recipient list and preparing a send requires permission to manage Marketing and AI skills, view all customers, and resolve AI approvals.

Marketing plans use the existing AI skill lifecycle for testing, enabling, disabling, and archiving, so you do not maintain the same rule in two places.

The AI customer-service identity bound to the plan or customer channel sends the message, so the approving teammate's conversation capacity is not consumed. For a single-customer send, an existing active conversation keeps its current assignee and the message is appended directly, with no transfer required. Broadcast and segmented delivery still skip conversations being handled by another assignee so a campaign cannot interrupt active support. **Sent** means the message has entered the sending flow; **Delivered** and **Read** appear only after the channel returns those results.

Scheduled and event-triggered plans run with the plan creator's current member permissions. If that member is disabled, leaves the workspace, or no longer has permission to manage Marketing, sending stops and a visible failure requires attention; old permissions are not reused.

Use Marketing history to review delivered, read, replied, and payment results; the open page refreshes these facts automatically. If a channel does not provide delivered or read receipts, those two values appear as “—” with an unavailable notice instead of a misleading zero. Real customer replies continue to update separately.
