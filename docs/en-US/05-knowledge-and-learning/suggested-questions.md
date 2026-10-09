---
title: Understand suggested questions
description: Learn how the website widget and test conversation receive knowledge-based suggested questions.
category: Knowledge and learning
order: 2
updated_at: 2026-10-09
---

# Understand suggested questions

Suggested questions help visitors begin a conversation and help merchants test the AI. A Website Widget can use automatic knowledge suggestions or custom questions configured on its reception Agent.

## Manage Widget suggested questions

Open **Agents**, select the built-in Agent receiving website conversations, then choose **Suggested questions**:

- Before you edit, the list shows three suggestions from that Agent's knowledge scope by default, or fewer when there are not enough suitable questions.
- Select a chip under **Knowledge recommendations** to add it to the list, or select **Add question** to write your own.
- Use the pencil to edit, the trash icon to remove, and the left handle to drag questions into order. Select **Apply question** after editing a row, then **Save** at the top. **Discard changes** restores the last saved list.
- Mix knowledge suggestions and custom text in one list of up to four unique questions, each up to 120 characters. Your saved order is used as-is. In custom mode, **Restore automatic** appears to the left of **Add question**. Select it and save to return to knowledge-based selection.

Custom questions only define the visitor's opening text, not an answer or a guarantee that AI can answer. Clicking still uses the normal AI answer flow. Text is translated for the Widget interface language; if translation is unavailable, the source text is not shown in another language.

Websites received by the same Agent share this question list. Each website keeps independent display switches. **Debug preview** on the right of the Agent configuration reflects your current edits so you can try them before saving.

## How questions are selected

YundaDesk considers the Agent’s currently available knowledge together and generates opening questions that are:

- focused on your core business: what you offer, its main uses, who it is for, and how to get started;
- supported by clear answers in the source material;
- independent of an order number, live inventory, or an unconnected app;
- free from internal, sensitive, or temporary context.

The system aims for topic diversity instead of repeating similar questions. Policy details, unusual exceptions, and advanced troubleshooting may support an answer without being suitable conversation starters. If there are too few suitable questions, fewer or none appear; peripheral questions are not added to fill the list.

## Where they appear

- **Widget Home:** When **Show suggestions on Home** is enabled, up to four questions appear in one list card between **Chat with support** and **Contact us**, separated by dividers. Selecting one immediately sends it as a real visitor message.
- **First empty conversation:** When **Show suggestions in empty chats** is enabled and the visitor enters chat without selecting a Home question, the same questions appear below the welcome message in the same order. They disappear after the first visitor message.
- **Agent Debug preview:** An empty conversation shows the current welcome message and question list. **Restart** shows them again, and refreshing does not bring back messages from before the restart.
- **Knowledge test conversation:** Load another set of knowledge-validation questions separately from the Agent's display list.

Clicking a question sends it through the normal AI answer flow. It does not reveal a static stored answer.

Open **Channels**, select the Website Widget, and expand **Display settings** to adjust **Show suggestions on Home** and **Show suggestions in empty chats**. The switches are independent. To edit content, select **Manage suggested questions** beside **Show suggestions on Home**, which opens that exact Agent.

Visitors see questions only from the enabled built-in Agent bound to that channel. Automatic mode also requires knowledge retrieval; custom mode does not require knowledge compilation. With human reception, no binding, or an unavailable Agent, no questions appear, but display switches can still be configured in advance.

## When they update

After updated knowledge finishes processing, reopen or refresh the suggested questions page to generate fresh candidates automatically. Automatic mode follows the new list, though similar content may produce the same questions. Removed or unavailable material is no longer used for recommendations.

Custom questions apply on the next Widget load after saving the Agent and are not overwritten by knowledge sync. **Knowledge recommendations** below the list still follows knowledge updates.

## Regenerate suggested questions

In the Agent’s **Suggested questions** section, select **Regenerate suggested questions** beside **Knowledge recommendations**. You need permission to manage knowledge, and knowledge retrieval must be enabled for the Agent.

This generates questions directly from the currently saved material without reprocessing the whole knowledge base. The button shows **Generating…**. Refreshing or leaving the page does not stop the task; returning shows its status and results. Repeated clicks do not start overlapping tasks.

When the material has not changed, the previous candidates remain visible during generation and after a failed attempt. Select **Regenerate suggested questions** to retry. Automatic mode updates the display list. Custom mode keeps your edited questions and updates only the candidates below.

If your website has changed, sync it in **Knowledges** first. **Regenerate suggested questions** does not fetch webpages again. You can regenerate suggestions from unchanged content, but this is not guaranteed to produce different questions.

## If the suggestions are not suitable

- **Adjust what visitors see:** Add a candidate to the list above, then edit, remove, or reorder it. You can also write your own question and save. The candidate chips themselves cannot be edited directly.
- **Improve automatic suggestions:** Add or improve the business overview, core products or services, intended audience, and getting-started instructions in this Agent’s knowledge. Wait for processing to succeed, then check the candidates again or select **Regenerate suggested questions**. If they still miss the mark, edit and save your display list directly instead of repeatedly regenerating.
- **Return to automatic selection:** Select **Restore automatic** to the left of **Add question**, then save. This replaces your custom display list; it does not generate a fresh set of candidates.
