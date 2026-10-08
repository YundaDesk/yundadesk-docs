---
title: Understand suggested questions
description: Learn how the website widget and test conversation receive knowledge-based suggested questions.
category: Knowledge and learning
order: 2
updated_at: 2026-10-08
---

# Understand suggested questions

Suggested questions help visitors begin a conversation and help merchants test the AI. A Website Widget can use automatic knowledge suggestions or custom questions configured on its reception Agent.

## Manage Widget suggested questions

Open **Agents**, select the built-in Agent receiving website conversations, then choose **Suggested questions**:

- Before you edit, the list automatically shows suggestions from that Agent's knowledge scope.
- Select a chip under **Knowledge recommendations** to add it to the list, or select **Add question** to write your own.
- Use the pencil to edit, the trash icon to remove, and the left handle to drag questions into order. Select **Apply question** after editing a row, then **Save** at the top. **Discard changes** restores the last saved list.
- Mix knowledge suggestions and custom text in one list of up to four unique questions, each up to 120 characters. Your saved order is used as-is. Select **Restore automatic** and save to return to knowledge-based selection.

Custom questions only define the visitor's opening text, not an answer or a guarantee that AI can answer. Clicking still uses the normal AI answer flow. Text is translated for the Widget interface language; if translation is unavailable, the source text is not shown in another language.

Websites received by the same Agent share this question list. Each website keeps independent display switches. **Debug preview** on the right of the Agent configuration reflects your current edits so you can try them before saving.

## How questions are selected

After knowledge processing succeeds, YundaDesk selects questions from the latest successful compilation that are:

- useful to a broad set of visitors;
- clear and low risk;
- independent of an order number, live inventory, or an unconnected app;
- free from internal, sensitive, or temporary context.

The system aims for topic diversity instead of repeating several versions of the same question.

## Where they appear

- **Widget Home:** When **Show suggestions on Home** is enabled, up to four questions appear in one list card between **Chat with support** and **Contact us**, separated by dividers. Selecting one immediately sends it as a real visitor message.
- **First empty conversation:** When **Show suggestions in empty chats** is enabled and the visitor enters chat without selecting a Home question, the same questions appear below the welcome message in the same order. They disappear after the first visitor message.
- **Agent Debug preview:** An empty conversation shows the current welcome message and question list. **Restart** shows them again, and refreshing does not bring back messages from before the restart.
- **Knowledge test conversation:** Load another set of knowledge-validation questions separately from the Agent's display list.

Clicking a question sends it through the normal AI answer flow. It does not reveal a static stored answer.

Open **Channels**, select the Website Widget, and expand **Display settings** to adjust **Show suggestions on Home** and **Show suggestions in empty chats**. The switches are independent. To edit content, select **Manage suggested questions** beside **Show suggestions on Home**, which opens that exact Agent.

Visitors see questions only from the enabled built-in Agent bound to that channel. Automatic mode also requires knowledge retrieval; custom mode does not require knowledge compilation. With human reception, no binding, or an unavailable Agent, no questions appear, but display switches can still be configured in advance.

## When they update

Automatic questions follow the latest successful knowledge compilation; a failed compilation keeps the previous successful candidates. Custom questions apply on the next Widget configuration load after saving the Agent and are not overwritten by knowledge sync.
