---
title: Define AI handoff boundaries
description: Hand uncertain, sensitive, or unsupported requests to a person.
category: AI customer service
order: 6
updated_at: 2026-08-16
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

## Configure customer-facing messages

1. Open the AI customer service reception settings.
2. The online queue, no-agents-online, and agent-joined notices can be enabled or disabled independently. The agent-joined notice appears as a normal message from the agent who takes over. Disabling a notice only hides that message; it does not change queueing or assignment.
3. Online queue, no-agents-online, and agent-joined notices are sent in the language the visitor is currently using, so you do not maintain separate language versions.
4. Enter the default-language messages for the online queue and for no agents online. When a conversation enters the human queue, YundaDesk checks the channel's effective reception scope and sends only one of them: online queue when an eligible agent is available but has not joined yet, or no agents online when nobody is online. An online workspace agent outside the channel's reception list does not make that channel available; those agents are considered only when workspace-pool fallback is enabled.
5. The workspace shows “Reception settings” below each of these notices so you can return directly to the relevant settings.
6. Verify the handoff in the Playground, then check the visible state changes in a real channel.

The waiting status is sent only once during the same human-waiting episode. Additional customer messages do not repeat it, restart the queue, or let AI take the conversation back. The agent-joined notice is sent once after an agent accepts the conversation.

## Email alerts when no agents are online

You can enable alerts first, then search and select active workspace members through “Select recipients.” The setting is saved with no recipients, but no email is sent until at least one member is selected. Smart digest groups conversations that are still waiting while no agent is online; first-alert mode sends one alert for each waiting episode. Neither mode sends a separate email for every unread message. Turning off automatic assignment changes the queue to manual pickup but does not change the no-agents-online check, and handled waits are not alerted again. The email contains only necessary waiting counts and duration; open the workspace to review the conversation.

## A technical failure is not a handoff

A temporary AI or integration failure does not automatically transfer the conversation to a person. The customer may see a retryable notice while the current assignment remains unchanged. Handoff occurs only when the customer requests a person or a configured business or safety rule applies.
