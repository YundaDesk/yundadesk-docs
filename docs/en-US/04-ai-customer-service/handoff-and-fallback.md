---
title: Define AI handoff boundaries
description: Hand uncertain, sensitive, or unsupported requests to a person.
category: AI customer service
order: 6
updated_at: 2026-08-01
---

# Define AI handoff boundaries

AI should not guess facts just to preserve automation. High-risk, low-confidence, or unsupported requests should be handed off or answered with a clear limitation.

## Appropriate handoff cases

- Refunds, compensation, permissions, or sensitive commitments;
- Requests that require an unconnected order, inventory, or shipping app;
- Conflicting or unverifiable knowledge;
- An explicit request for a person;
- Repeated answers that do not resolve the issue.

## Verify behavior

Test one answerable and one unsupported question in the Playground. The first should answer normally; the second must not invent data and should provide a clear next step.

## After handoff

After a person takes over, AI should not compete for the conversation. Return it to AI only after the human task is complete.

## A technical failure is not a handoff

A temporary AI or integration failure does not automatically transfer the conversation to a person. The customer may see a retryable notice while the current assignment remains unchanged. Handoff occurs only when the customer requests a person or a configured business or safety rule applies.
