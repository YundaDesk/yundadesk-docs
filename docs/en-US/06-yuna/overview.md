---
title: Meet Yuna
description: Understand how Yuna differs from AI customer service and what it can do for your team.
category: Yuna
order: 1
updated_at: 2026-09-15
---

# Meet Yuna

Yuna is the AI assistant for your merchant team. It helps you understand data, complete setup, teach AI customer service, and handle tasks. It is not the customer-facing AI agent.

Yuna replies in the language of your current message. Browser UI language, previous Yuna replies, and referenced content do not override it. If you send only an emoji, URL, or code, Yuna reuses the natural language from your most recent message.

## Four ways Yuna helps

- **Ask:** Query conversations, channels, team activity, usage, and connected business data.
- **Act:** Use capabilities available in the workspace to draft or perform setup and customer actions.
- **Teach:** Turn rules, standard answers, customer preferences, or outreach requests into learning suggestions.
- **Receive:** Surface learning tasks, AI failures, delivery issues, and follow-up reminders.

## How Yuna knows what it can do

Yuna checks the current workspace setup. Available actions depend on product features, connected channels, installed apps, and workspace settings. When something required is missing, Yuna should explain what must be connected rather than pretending that an action succeeded.

## Confirmation and safety

Read-only questions can usually return immediately. Sending messages, affecting customers, changing permissions, or making broad configuration changes displays a confirmation card first. Without confirmation, no real side effect should occur. Service style on the current Agent page is a low-risk, reversible edit with an explicit target: Yuna can ask natural follow-up questions and save directly once the request is clear, without adding a confirmation card. Permission, approval, cooldown, and channel policy still apply even when a capability exists.

## Plans and allowance

Yuna availability and allowance depend on the current subscription and workspace settings. Open the subscription page to review current availability, usage, and the remaining allowance. Yuna usage is shown separately from AI Credit.

## Entry

Open Yuna from the AI area. The full page and floating window share the same conversation state and should continue the same in-progress operation across page changes.

When you start a new conversation on the full Yuna page, you can choose from three next-step suggestions. These may come from work information you can access, or offer help preparing a business brief, reply drafts, or support knowledge. Preparation suggestions do not mean something is wrong with your workspace. Selecting one starts a Yuna conversation; it does not directly send customer messages or change settings. For source-backed suggestions, expand **Reference context** in the message to inspect the supporting material. Return to a new conversation to see the available suggestions.

For work that needs to repeat, expand **Yuna** in the main navigation and select **Automations**. You can [create a workspace-task Automation with Yuna](./automations.md) or manually set up work that runs on demand, every day, on weekdays, or every week. If the manual form offers Customer outreach, every send still requires a person to review and approve the audience and message.

Use the mode picker at the bottom of the composer to switch between **Base** and **Thinking**. After you select **Thinking**, it stays active after sending, changing pages, or refreshing until you switch back to **Base**. Thinking lets Yuna analyze more thoroughly internally, but raw reasoning is never shown. While generating, Yuna shows elapsed work time and real tool activity only; after completion, it collapses to “Worked for x s,” and the final answer remains separate.

When you open Yuna again, the browser resumes only a locally remembered conversation that was active recently. If no conversation is remembered, or it has been inactive for a while, Yuna opens a new conversation page.

When a full-page conversation contains at least two real messages, a rail appears on the left on desktop. User messages and Yuna replies with text each receive a tick, and every message intersecting the viewport is emphasized. Moving the pointer near the rail continuously magnifies neighboring ticks, pausing briefly opens a message preview, and selecting a tick jumps to that message. Supporting activity, data cards, and action receipts do not create separate ticks. The rail is not shown in mobile or floating-window layouts.

When you open the floating window on a supported page, a neutral Current page chip may appear above the composer. It can represent a selected customer, conversation, knowledge document, channel, setting, or report.

The chip is only a choice until you select it. After selection, it appears as a compact attachment beside pending files in the composer and applies to the next message. You can remove it before sending. After sending, the context attachment remains below that message so you can see which context was used.

Within the current browser session, unsent text, images, page context, and shortcut mode remain available when you move between the floating Yuna window and the full page, or leave Yuna and return. Starting a new conversation opens a blank composer.

Selected context can narrow Yuna's answer to the current customer, conversation, knowledge document, channel, setting, or report range. Yuna uses only information you are allowed to access. Unsupported pages do not show the chip, and Yuna may ignore it when your request is unrelated.

If one response has several visible steps, **Activity in this response** groups them and can be collapsed after completion. Reading position is remembered for each conversation. Connection notices appear when the browser is offline or unstable, and drafts are cleared after a message is sent successfully.

## Voice input

In browsers that support speech recognition, the Yuna composer shows a microphone button. Click it and allow microphone access to see your speech appear in the draft. Stop recording, review or edit the text, then send it. The Chinese interface uses Mandarin recognition; the English interface uses English recognition.

Switching conversations or leaving the composer ends the recording. If no microphone button appears, continue typing or use your device keyboard’s dictation feature. If recognition fails, check microphone permissions and your connection. Recognition is provided by your browser and may require internet access; results vary by browser and dialect.
