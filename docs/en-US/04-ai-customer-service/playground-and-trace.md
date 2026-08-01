---
title: Test answers and inspect traces
description: Test knowledge, skills, tools, and answer evidence without contacting real customers.
category: AI customer service
order: 2
updated_at: 2026-07-17
---

# Test answers and inspect traces

The Playground tests the current AI configuration without sending messages to customer channels.

## Run a test

1. Open **AI → Playground**.
2. Ask the way a real customer would; do not only copy knowledge article titles.
3. Observe the answer, handoff behavior, and tool calls.
4. Open **View details** or the trace link under the answer.

The Playground may show test questions generated from the current knowledge base. Clicking one sends a normal test message. Use **Try another set** to browse more.

## Read an answer trace

The details may show:

- matched knowledge or summaries;
- matched AI skills;
- customer memories that were used;
- business tools and their results;
- safety decisions, fallback, or handoff reasons.

The trace explains why the answer was produced. It is not a merchant-facing workflow editor.

## Build a useful test set

For every important policy, test a standard question, a very short question, and a contextual or misspelled question. Tool-dependent capabilities should also be tested without an order number, with an unavailable tool, and without permission.

If the answer exists in the knowledge base but is not used, verify document status and the latest successful sync before following the [AI answering troubleshooting guide](../10-troubleshooting/ai-answering.md).
