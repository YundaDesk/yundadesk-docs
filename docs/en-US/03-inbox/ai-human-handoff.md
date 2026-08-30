---
title: Switch between AI and human service
description: Understand the difference between global AI reception and taking over one conversation.
category: Inbox
order: 2
updated_at: 2026-08-30
---

# Switch between AI and human service

YundaDesk supports AI-first service with human takeover at any time. Global reception settings and the service state of one conversation are separate controls.

## Global reception settings

**AI Agents** determines which Agent serves customers and which channels are bound to each Agent. A channel without a bound, available Agent does not trigger automatic AI replies for new customer messages.

## Take over one conversation

Open the conversation and select **Take over** or the equivalent action. After takeover:

- the AI stops replying automatically in that conversation;
- if the agent-joined notice is enabled, the customer receives it as a normal message from the agent who takes over;
- the assigned agent can reply directly;
- the service state and assignee are updated.

While AI is handling the conversation, the current Agent name is shown. Select the name to open that Agent's settings. If another Agent is available, a member with channel management permission can select **Switch Agent** and choose the new reception Agent.

When the issue is resolved, you can return the conversation to AI where supported, or close it. If only one Agent is available and the channel already has a valid binding, the handoff can use it directly. If multiple Agents are available or the channel has no valid binding, choose an Agent in the picker first. Confirming both assigns the current conversation and makes that Agent the channel's reception Agent for future conversations; it does not create a conversation-only override.

Before returning the conversation, confirm that the AI has the knowledge and context needed to continue safely.

## Automatic handoff

Handoff may occur when the AI lacks a reliable answer, the customer asks for a person, a required app or channel is unavailable, or a safety rule applies. A handoff does not mean the issue has been resolved; the team must continue in the Inbox.

## Recommended practices

Keep refunds, price changes, and other high-risk commitments behind human confirmation. When an AI answer is wrong, use **Correct AI** so the problem can enter the governed learning flow.
