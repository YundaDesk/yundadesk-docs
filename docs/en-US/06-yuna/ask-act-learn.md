---
title: Ask, act, and teach with Yuna
description: Use natural language to query data, complete actions, and teach AI customer service.
category: Yuna
order: 2
updated_at: 2026-08-30
---

# Ask, act, and teach with Yuna

You do not need to remember feature locations or customer numbers. Describe the goal, target, and constraints. Yuna will decide the next step from the features available in the current workspace.

## Use composer shortcuts

The **+** menu at the bottom of Yuna's composer provides shortcuts for translation, polishing, conversation review, teaching AI customer service, customer insight, and business briefs. After you select one, the input prompt changes to match the task, such as **Enter text to translate**. Select the active shortcut again to exit it. Translation also provides a submenu for choosing the target language.

After you send, the user message keeps the original text and shows a blue task label at the beginning, such as **Translate to English**. Yuna's next message contains only the result. A task label describes what Yuna should do this time. A page, conversation, or customer context label identifies which information Yuna may use.

| Shortcut | Example | Requirements and result |
|---|---|---|
| Translate | Enter “Please confirm your delivery address” and select Chinese | Returns the text in the target language without changing the source or adding facts |
| Polish | Enter a draft reply that you plan to send to a customer | Improves tone and clarity while preserving meaning, numbers, and commitments |
| Review conversation | From the target conversation, enter “Find out why this conversation was handed to a person” | Requires the relevant conversation; returns key facts, handling issues, and suggested next steps |
| Teach AI customer service | Enter “When customers ask about cash on delivery, check the country and product first” | Prepares a learning draft; it does not affect customer replies until it is reviewed, tested, and enabled |
| Customer insight | From the target customer page, enter “Summarize this customer's needs and risks” | Requires access to that customer and uses only information the current member can view |
| Business brief | Enter “Summarize conversation volume, AI participation, and human handoffs for the last seven days” | Requires the relevant data and report permission; Yuna explains missing data instead of inventing numbers |

### Translate a passage

1. Select **+** at the bottom of the Yuna composer, then select **Translate**.
2. Choose the target language, such as Chinese.
3. Enter the source text and send it.

**Example:** “Please confirm your delivery address. We will ship within two business days after payment.”

Yuna returns only the translated result. The meaning, numbers, and commitments should remain unchanged. Use **Polish** instead when you want to change the tone.

### Polish a reply draft

1. Select **Polish**.
2. Paste the reply you plan to send and describe the desired tone, such as “Friendlier, but do not add any commitments.”
3. Send it, review the result, and then decide whether to use it.

**Example:** “Make this professional and concise: This color is out of stock. Choose another one.”

Yuna improves the wording without changing inventory facts, prices, timing, or refund commitments.

### Review a customer conversation

1. Open the customer conversation you want to analyze.
2. Under **Current page** above the Yuna composer, select the conversation label so that it moves into the composer.
3. Select **Review conversation**, describe what you want to examine, and send it.

**Example:** “Find out why this conversation was handed to a person. List what the AI knew, what was missing, and the next improvements to make.”

Yuna organizes key facts, handling steps, risks, and suggestions from that conversation. If no conversation is selected, Yuna asks you to choose a target instead of guessing.

### Teach AI customer service a handling method

1. Select **Teach AI customer service**.
2. Describe when the method applies, the handling steps, constraints, and when a person should take over.
3. Send it, review the learning draft prepared by Yuna, and then follow the prompts to test and enable it.

**Example:** “When customers ask about cash on delivery, check the destination country and product first. If it is not supported, explain why and offer another payment method. Do not promise an exception.”

This step creates content for review only. It does not change customer-facing replies until the draft is reviewed, tested, and enabled.

### Get insight about a customer

1. Open the target customer's detail page.
2. Under **Current page** above the Yuna composer, select the customer label so that it moves into the composer.
3. Select **Customer insight**, ask a specific question, and send it.

**Example:** “Summarize the products this customer has recently asked about, recurring issues, churn risks, and a recommended follow-up.”

Yuna uses only customer details, conversations, and connected business data that the current member can access. It identifies missing information when the available record is incomplete.

### Create a business brief

1. Open Reports and select the time range you need.
2. Under **Current page** above the Yuna composer, select the report label so that the current range moves into the composer.
3. Select **Business brief**, specify the metrics and output format, and send it.

**Example:** “In five bullet points, summarize conversation volume, AI participation, human handoffs, and unusual changes for the last seven days.”

Yuna queries data within the current report range and the member's permissions. It identifies unavailable metrics instead of replacing them with estimates.

A shortcut gives Yuna a task-specific starting point. It does not expand the current member's data access or bypass action confirmation. Conversation review, customer insight, and business briefs still require the relevant current page, available data, and permission. Yuna asks for the missing target or context when needed.

## Ask questions

Examples include “How many conversations did each channel receive yesterday?” and “Which issues are handed to people most often?” Yuna answers from data you are allowed to view. When data is unavailable, it should say so rather than fill the gap with a guess.

## Perform an action

For example: “Send a Telegram message to a selected customer about the new product.” Yuna can help you choose the customer and then show a confirmation containing the recipient, channel, and exact message. The message is sent only after confirmation, followed by a real delivery result or failure reason.

When a request has an important choice, Yuna can ask with a selection card, such as **Create a draft only** or **Send after confirmation**. After selection, progress should remain visible until the next draft or confirmation card appears.

For setup changes such as connecting a channel, creating knowledge, configuring AI reception, updating branding, or inviting members, Yuna first shows a draft or validation result. It performs the change only after you confirm. Read-only questions still follow your workspace permissions.

## Teach the AI

Examples include a standard cash-on-delivery answer or a temporary holiday shipping policy. When Yuna detects that you may be teaching it, it first asks whether to enter the learning flow. Only an explicit confirmation allows Yuna to prepare a structured draft and create a learning card. Declining continues the normal conversation and creates no learning content.

For a multi-step skill, the draft includes when it applies, information to collect, handling steps, and test scenarios. After confirmation, open the skill detail to review the flow and branches and run customer scenarios.

The system creates multiple customer scenarios for normal handling, missing information, conditional branches, external capability failures, declined confirmation, and human handoff where applicable. You can run one scenario or all scenarios. Simulation does not perform real external actions. Editing a field or asking Yuna to revise the skill makes earlier results stale, so the new revision must be tested again. The skill can be enabled only when every required scenario for the current revision passes, required capabilities are available, and risk checks succeed.

Yuna does not claim that it has learned something before the learning card actually exists. After enablement, AI customer service follows the reviewed flow. If a required capability or permission later becomes unavailable, the system does not bypass the check and continue.

### Correct an existing knowledge fact

If an existing contact detail, address, policy, or similar fact is wrong, tell Yuna the correct information. Yuna first locates the current knowledge source and asks you to choose when several targets are possible. Review the **current answer → corrected answer** preview, then confirm it. Yuna submits that knowledge change directly instead of creating another learning proposal for review.

After confirmation, the completion receipt lists the updated question and answer. Correcting knowledge created from an uploaded file or website does not rewrite the original file or external site; edit and resync the source when that content must also change. Then ask the customer's original question and one paraphrase in a real Widget or with **Test conversation** on the **AI Agents** page to confirm that the new knowledge is used.

If the source file, website, or connector content changes later, the system does not silently overwrite the confirmed answer. When the new source conflicts with that answer, Yuna shows a **Knowledge correction needs review** task and opens the exact FAQ entry so you can compare the current answer with the new source suggestion. You can keep the current answer, edit it, or adopt the suggestion. The review is complete only after you save, and it is not a new learning proposal.

## Capability boundaries

Order, inventory, logistics, customer records, broadcast, and similar actions require a connected app or channel. A knowledge article cannot replace live business information.
