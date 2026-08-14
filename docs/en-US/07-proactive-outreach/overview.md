---
title: Create and govern proactive outreach
description: Contact customers at the right time while respecting confirmation, cooldown, and channel safeguards.
category: Proactive outreach
order: 1
updated_at: 2026-08-13
---

# Create and govern proactive outreach

Proactive outreach prepares or sends a message based on an event, time, or audience condition when the customer has not just sent a new message. It is not a normal auto-reply or a renamed FAQ.

## Create a rule

Tell Yuna the business outcome, for example: “If a customer stops replying for 30 minutes after asking about a product, prepare a follow-up draft, at most once per customer every 24 hours.” Yuna organizes the trigger, action, channel, and cooldown, then creates a learning suggestion.

Rules based on cart, payment, order, or other store changes require a connected app that provides that information. Without a real information source, keywords alone must not trigger the rule.

When Marketing is available in the workspace, you can also open **YundaDesk AI → Marketing** and select “Create with Yuna.” Yuna reuses details already supplied in the current conversation, asks for any missing goal, audience, trigger, channel, content, and frequency limit, then shows a complete preview before asking whether to create a reviewable learning proposal. Before explicit confirmation, no proposal is created and nothing is enabled or sent. Confirmation starts learning review; it does not mean the plan is active.

A one-off birthday greeting or product reminder to one customer is a marketing execution, but it does not create a plan. After confirmation, YundaDesk checks marketing consent, opt-out, quiet hours, frequency limits, and channel readiness. The AI customer-service identity bound to that channel sends the message, and the execution appears once in Marketing history. If the required channel or app capability is unavailable, Yuna returns a system-controlled **Not executed** result with a configuration prompt; it does not generate a sent claim.

Daily, weekly, and other recurring plans can first be organized as reviewable drafts. Whether a draft can be enabled still depends on timezone, audience segmentation, channel, frequency control, and scheduling readiness. If any capability is not ready, YundaDesk shows that gap instead of claiming the plan is scheduled.

## Operating modes

Outreach may run in observation, per-message confirmation, or automatic mode. Available modes depend on current configuration and risk. Start with observation or confirmation, then consider automatic sending only after reviewing real behavior.

## Safeguards

Before sending, YundaDesk checks workspace enablement, channel readiness, consent, quiet hours, cooldown, duplicate outreach, and customer memory. A missing required condition should block the send and record the reason.

## View the result

Skill details, Yuna tasks, and delivery details explain what triggered, which action was selected, why it was blocked, and whether the channel delivered it. Broadcast and segmented outreach are higher-risk and normally require a draft and confirmation; current availability is shown in the capability center.

For a running marketing plan, **Review and send** opens a new Yuna conversation. Yuna resolves only customers with marketing consent and shows the number matched, currently eligible, and filtered out before freezing the exact audience, channel, recipient count, and final message. The audience is not expanded or recalculated after confirmation. Before real delivery, YundaDesk checks consent, opt-out, quiet hours, frequency limits, plan state, and channel readiness again, so the final recipient count may only decrease. Missing structured filters, no eligible recipients, or an unavailable channel stops the send with a visible reason. Confirmed batches appear in Marketing history.

In **YundaDesk AI → Marketing**:

- **Marketing plans** shows plan status, version, recent use, and a visual path from trigger to audience, AI customer-service send, and frequency control.
- **Marketing history** lists one-off outreach, suppressed, preview-only, triggered, sent, partially completed, delivered, read, and failed results in time order. One confirmed batch appears as one history record with target, sent, suppressed, and failed recipient counts. Sent records visualize the seven-day funnel from target to sent, delivered, read, replied, and confirmed payment.

Marketing plans use the existing AI skill lifecycle for testing, enabling, disabling, and archiving, so you do not maintain the same rule in two places.

The AI customer-service identity bound to the plan or customer channel sends the message, so the approving teammate's conversation capacity is not consumed. For a single-customer send, an existing active conversation keeps its current assignee and the message is appended directly, with no transfer required. Broadcast and segmented delivery still skip conversations being handled by another assignee so a campaign cannot interrupt active support. **Sent** means the message has entered the sending flow; **Delivered** and **Read** appear only after the channel returns those results.

Use Marketing history to review delivered, read, replied, and payment results. When a result is unavailable, it appears as zero or unknown.
