---
title: Correct an AI answer
description: Submit a correction from a real conversation and verify that the AI uses the new capability.
search_terms: correct outdated knowledge, outdated support phone number, fix wrong knowledge, correct the AI
category: Knowledge and learning
order: 5
updated_at: 2026-08-11
---

# Correct an AI answer

**Correct AI** sends a wrong customer answer into governed relearning. It is not a like/dislike button and does not send a replacement message to the customer.

## Submit a correction

1. Find the wrong AI answer in the Inbox.
2. Select **Correct AI**.
3. In **Correction**, state the correct fact and how similar cases should be answered or handled. Add conditions and exceptions when needed, then submit.

The original AI answer now keeps one compact **AI correction** status button beneath it. The button stays attached after a refresh or after you reopen the conversation. You can correct the same answer again; the button shows the correction count and uses the newest receipt as its current status. Open it to review the current correction and outcome in place. YundaDesk uses the question, original answer, and correction to decide whether to update knowledge, an AI skill, customer memory, the current conversation, or configuration.

Clear, conflict-free knowledge, skill, and customer-memory corrections continue through preparation and verification. When YundaDesk needs a choice, detects a conflict with existing knowledge or skills, or needs a skill change, Yuna opens a new conversation. A configuration correction also opens the Yuna conversation dedicated to that correction, where Yuna clarifies and performs the change instead of treating it as successful learning. Yuna first explains the customer question, original AI answer, correction, and proposed direction, then asks for your decision. Reopening Yuna resumes that same conversation; you do not need to search a learning list.

When a correction explicitly applies only to the current conversation and does not conflict with platform rules, YundaDesk applies it to later AI reception in that conversation and shows **Applied to current conversation**. It is not saved as knowledge, a skill, or a long-term rule, and it does not open Yuna. A configuration correction shows **Continue in Yuna** and always reopens the conversation for that correction, not another historical Yuna conversation.

After confirmation, the button updates through preparation, activation, and verification without requiring a hard refresh. Skill corrections are tested before they are enabled. Knowledge corrections are checked against the target knowledge. YundaDesk automatically re-asks the original question and one similar question. It shows **Correction successful** only when the final asset is active and both answers pass verification. Creating a suggestion, confirming it, or writing an asset is not a successful terminal state.

If you ignore a learning suggestion, the card explicitly shows **Ignored** rather than reporting a system failure, and you can still submit another correction. If the system rejects a correction before learning content is created, the card shows a user-readable processing reason rather than only an internal code. If saving the learning fails, the record remains visible and is not treated as completed.

## Write a useful correction

A useful **Correction** combines the trusted fact and handling guidance, such as “We currently support PayPal and credit cards. List them when customers ask about payment methods, and escalate only if they ask about another method.” YundaDesk prepares the customer-facing candidate answer and scope, so you do not need to repeat the same information in a second field or choose a scope.

Do not write only “wrong answer” or “bad tone.” Identify the incorrect fact, applicable conditions, and exceptions. State “only for this customer” when the information is a personal preference. YundaDesk determines whether shared guidance belongs in knowledge or an AI skill.

The deciding factor is what should change. Verifiable facts such as payment methods or return policies belong in knowledge. Reusable reception behavior—greetings, agent identity, tone, follow-up questions, or escalation style—belongs in an AI skill, even when the behavior has only one step.

## Verify the result

If automatic verification fails, the card shows the reason, failed test question, and actual AI reply instead of only a generic failure. Follow the guidance to correct it again, or open the related knowledge or skill to roll back, disable, or delete it.

Platform rules cannot be overridden by a correction. For example, the AI must follow the language of the customer's latest message, so a correction such as “always answer in English regardless of the customer language” does not become a usable learning asset. A candidate reply follows the customer's question language rather than the language used to write the correction. A skill reply that still violates this rule is not sent to the customer. Later correct hits in real reception provide additional evidence that the correction is being used.
