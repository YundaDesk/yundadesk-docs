---
title: Create and govern proactive outreach
description: Contact customers at the right time while respecting confirmation, cooldown, and channel safeguards.
category: Proactive outreach
order: 1
updated_at: 2026-08-01
---

# Create and govern proactive outreach

Proactive outreach prepares or sends a message based on an event, time, or audience condition when the customer has not just sent a new message. It is not a normal auto-reply or a renamed FAQ.

## Create a rule

Tell Yuna the business outcome, for example: “If a customer stops replying for 30 minutes after asking about a product, prepare a follow-up draft, at most once per customer every 24 hours.” Yuna organizes the trigger, action, channel, and cooldown, then creates a learning suggestion.

Triggers based on cart, payment, order, or other store events require an app or tool that produces those real events. Without a real event source, the system must not fabricate a trigger from keywords.

## Operating modes

Outreach may run in observation, per-message confirmation, or automatic mode. Available modes depend on current configuration and risk. Start with observation or confirmation, then consider automatic sending only after reviewing real behavior.

## Safeguards

Before sending, YundaDesk checks workspace enablement, channel readiness, consent, quiet hours, cooldown, duplicate outreach, and customer memory. A missing required condition should block the send and record the reason.

## View the result

Skill details, Yuna tasks, traces, and delivery logs explain what triggered, which action was selected, why it was blocked, and whether the channel delivered it. Broadcast and segmented outreach are higher-risk and normally require a draft and confirmation; current availability is shown in the capability center.
