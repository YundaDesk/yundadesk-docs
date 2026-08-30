---
title: Inspect outreach delivery
description: Verify each stage from the trigger and decision to final channel delivery.
category: Proactive outreach
order: 3
updated_at: 2026-08-30
---

# Inspect outreach delivery

Do not treat “Automation ran” as proof that a customer received a message. Check the run, approval, and channel result separately.

## Inspect the path

1. Open **Yuna → Automations**, find the task, and open **Run history**.
2. Check the time, version, status, and result summary for this run.
3. If the status is Waiting for approval, open the approval preview, verify the audience, channel, recipient count, and exact message, then approve or reject it.
4. After approval, open the outreach result or history entry offered by the page and review target, sent, suppressed, and failed counts.
5. Continue to the **Delivered** or **Read** result returned by the channel. Spot-check important outreach in the real customer channel.

## Common reasons a message was not sent

Common reasons for no send include missing event data, an active cooldown, quiet hours, an unavailable channel, missing app access or permission, pending human confirmation, or channel delivery failure. If a batch recipient is already in a conversation handled by another teammate or AI, that recipient may be shown as **Suppressed** rather than as a channel failure.

No generated message is not always an error. A safety gate may have correctly blocked outreach.

The Target → Sent → Delivered → Read → Replied results come from actual sending outcomes, channel receipts, and customer replies. Missing receipts remain unknown or unavailable rather than being inferred.
