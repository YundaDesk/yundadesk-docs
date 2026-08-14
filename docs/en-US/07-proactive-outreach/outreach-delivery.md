---
title: Inspect outreach delivery
description: Verify each stage from the trigger and decision to final channel delivery.
category: Proactive outreach
order: 3
updated_at: 2026-08-13
---

# Inspect outreach delivery

An outreach message passes through a trigger, decision, safety checks, and channel delivery before a customer receives it.

## Inspect the path

1. Open the outreach record in Marketing history. A one-off single-customer send does not create a marketing plan.
2. Verify the real trigger event and target customer.
3. Check cooldown, quiet hours, consent, and permission gates.
4. Confirm that the outreach item was created.
5. Open the delivery record and inspect the final channel status.

## Common reasons a message was not sent

Common reasons for no send include missing event data, an active cooldown, quiet hours, an unavailable channel identity, a missing channel or app capability, pending human confirmation, or channel delivery failure. When the required capability is missing, Yuna shows a system-controlled **Not executed** result and cannot claim the message was sent. If a batch recipient is already in a conversation handled by another teammate or AI, that recipient is counted as **Suppressed**; no transfer is required, and it is not reported as a channel failure.

No generated message is not always an error. A safety gate may have correctly blocked outreach.

The Target → Sent → Delivered → Read → Replied → Confirmed payment funnel is based on durable messages, channel receipts, customer replies, and explicit paid events. Missing receipts or reliable paid events remain zero or unknown rather than being inferred.
