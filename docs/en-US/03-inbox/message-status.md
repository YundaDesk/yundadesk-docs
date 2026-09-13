---
title: Understand message status
description: Distinguish between saved, accepted, delivered, and failed messages.
search_terms: sending sent failed status, message status meaning, delivery state
category: Inbox
order: 5
updated_at: 2026-09-13
---

# Understand message status

An Inbox message may be saved before it is delivered asynchronously through a channel.

## Common states

- **Processing:** Generation or delivery is still running. Do not send a duplicate.
- **Accepted:** The request entered the delivery path but may not have reached the customer.
- **Delivered or sent:** The channel processed the message. Spot-check important messages in the real client.
- **Failed:** Delivery did not complete and requires investigation.

## After refresh

A message must still appear after refresh to count as saved. Its order should remain stable when the reply finishes loading.

## Has the customer read your reply?

In Website Widget conversations, “Read” appears where “Sent” was shown after the customer views your reply in the open chat window. Visiting the website, staying on the Widget home screen, or leaving chat in a background tab does not count as reading it.

If the customer skips messages in the middle, later replies keep their previous status until the customer has viewed the messages up to that point. Confirmed read states remain after you refresh the Inbox. “Read” does not mean the customer has replied or the conversation is resolved. Read status on other channels depends on channel support.

## Who has read a customer message

An incoming customer message may show a “Read” avatar group. These are the agents whose reading position has reached that message. Hover over the group to view the full list. This means they have seen it; it does not mean the conversation has been replied to or resolved.

## Handle failures

Before retrying, open the delivery details to determine whether permissions, the channel, content safety, or an external platform caused the failure.
