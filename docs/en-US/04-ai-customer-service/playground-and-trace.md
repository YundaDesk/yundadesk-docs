---
title: Test answers and review details
description: Test knowledge, skills, connected business information, and answer sources without contacting real customers.
category: AI customer service
order: 2
updated_at: 2026-08-01
---

# Test answers and review details

The Playground tests the current AI configuration without sending messages to customer channels.

## Run a test

1. Open **AI → Playground**.
2. Ask the way a real customer would; do not only copy knowledge article titles.
3. Observe the answer, handoff behavior, and whether the required business information was available.
4. Open **View details** below the answer.

The Playground may show test questions generated from the current knowledge base. Clicking one sends a normal test message. Use **Try another set** to browse more.

## Review answer details

The details may show:

- matched knowledge or summaries;
- matched AI skills;
- customer memories that were used;
- information from connected business apps;
- safety decisions, fallback, or handoff reasons.

The details explain why the answer was produced without requiring knowledge of the product's internal implementation.

## Build a useful test set

For every important policy, test a standard question, a very short question, and a contextual or misspelled question. Capabilities that need live business information should also be tested without an order number, with an unavailable app, and without permission.

If the answer exists in the knowledge base but is not used, verify document status and the latest successful sync before following the [AI answering troubleshooting guide](../10-troubleshooting/ai-answering.md).
