---
title: Understand suggested questions
description: Choose the questions visitors see and regenerate suggestions after updating knowledge.
category: Knowledge and learning
order: 2
updated_at: 2026-10-10
---

# Understand suggested questions

Suggested questions help visitors start a conversation. A Website Widget can use its reception Agent's automatic suggestions or a custom list you save.

## Manage Widget suggested questions

Open **Agents**, select the built-in Agent receiving website conversations, then choose **Suggested questions**:

1. Once the first suggestions are ready, the list is kept automatically. You do not need to edit and save it first, and reopening the page shows the same list. Fewer questions, or none, may appear when there are not enough suitable suggestions.
2. Select a chip under **Knowledge recommendations**, or select **Add question** to write your own.
3. Use the pencil to edit, the trash icon to remove, and the left handle to reorder. Select **Apply question** after editing a row.
4. Try the questions in **Debug preview** on the right, then select **Save** at the top. **Discard changes** restores the last saved list.

In custom mode, **Restore automatic** appears to the left of **Add question**. Select it and save to use automatic suggestions again. Websites received by the same Agent share the list, while each website keeps its own display switches.

Custom questions define only the opening text. Clicking one asks the AI to answer normally, so check the answers in Debug preview before saving. Questions follow the Widget interface language; when translation is unavailable, text from another language is not shown.

## Where suggestions come from

Automatic suggestions use the Agent's available knowledge. A business overview, core products or services, intended audience, and getting-started guidance help produce useful opening questions.

Review the results. Check that each question relates to your core business, has a clear answer in the knowledge, and does not first require an order number or other personal information.

## Where they appear

Open **Channels**, select the Website Widget, and expand **Display settings**:

- **Home:** Shows the list between **Chat with support** and **Contact us**.
- **Empty chats:** Shows the same questions below the first conversation greeting. They disappear after the visitor sends a message.

In the Agent’s **Suggested questions** header, select **Configure display** to the left of **Add question**. If one website is bound, its settings open directly. If several websites are bound, choose a channel from the menu first.

The switches are independent. Select **Manage** beside **Suggested questions** to open the corresponding Agent.

Visitors see questions only from the enabled built-in Agent bound to the channel. Automatic suggestions also require knowledge retrieval. Questions are hidden during human reception, when no Agent is bound, or when the Agent is unavailable.

Use the Agent's **Debug preview** to try your edits. Questions under **Knowledges → Test knowledge** help check answers and do not change the visitor-facing list.

## When they update

After updated knowledge finishes processing, reopen or refresh the suggested questions page to see new candidates. New candidates do not automatically replace the questions already displayed.

Knowledge updates do not overwrite your saved display list. It applies on the next Widget load, while the candidates below continue to follow knowledge changes.

## Regenerate suggested questions

Select **Regenerate suggested questions** beside **Knowledge recommendations** in the Agent's **Suggested questions** section. You need permission to manage knowledge, and knowledge retrieval must be enabled for the Agent.

While the button shows **Generating…**, refreshing or leaving the page does not interrupt generation. Return to see its status and results. If the material has not changed, previous candidates remain visible during generation and after a failed attempt. You can try again after a failure.

Regeneration updates only the candidates below and keeps the current display list. Select or edit suitable questions, then select **Save** at the top to apply them.

If your website has changed, sync it in **Knowledges** first. Regeneration uses the currently saved material; it does not fetch webpages again or guarantee different questions each time.

## If the suggestions are not suitable

- **Adjust the display list:** Add candidates, then edit, remove, or reorder them. You can also write your own questions and save.
- **Improve automatic suggestions:** Update the Agent's business overview, core products, intended audience, or getting-started guidance. Wait for processing to finish, then regenerate.
- **Still unsuitable:** Edit and save your display list directly instead of repeatedly regenerating.

**Restore automatic** replaces your custom display list. **Regenerate suggested questions** refreshes the candidates; the two actions serve different purposes.
