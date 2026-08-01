---
title: Read Yuna action receipts
description: Confirm that an action really completed and inspect its execution path.
category: Yuna
order: 6
updated_at: 2026-08-01
---

# Read Yuna action receipts

Natural-language acknowledgements such as "done" are not proof of execution. A real action produces a structured receipt.

## A receipt should show

- The outcome;
- Target or scope;
- A summary of important content;
- Processing or delivery state;
- A link to the execution path.

## Understand receipt states

Accepted means the request entered the execution path and may not have reached an external channel. Even Completed should be interpreted together with the delivery status. Verify important outbound messages in the real customer client.

## If no receipt appears

If no receipt appears, check whether Yuna only created a draft, still waits for confirmation, lacks the required workspace capability, or was blocked by permission and safety checks.
