---
title: Connect Notion knowledge
description: Authorize a read-only scope and import Notion pages into the knowledge base.
category: Knowledge and learning
order: 8
updated_at: 2026-08-01
---

# Connect Notion knowledge

You can connect Notion pages to YundaDesk. Content is synchronized into the local knowledge base and then follows the existing processing, retrieval, and answer pipeline. The AI does not query Notion while answering a customer.

## Connect a source

1. Open Knowledge and select **New document**.
2. Open the **Notion** entry, then select **Connect Notion**.
3. YundaDesk opens a new tab. Confirm the read-only access scope on the Notion authorization page.
4. After authorization returns, choose a page as the sync root in the new tab.
5. Confirm and start the first sync.
6. Wait for the status to become **Healthy**, then test important questions in the AI Playground.

**New document** currently provides three entries: **Upload file / Crawl web page / Notion**. If the connect button is disabled, Notion is not available for this workspace yet. Contact YundaDesk support to confirm availability; once it is enabled, you can authorize it without creating another knowledge base. Feishu knowledge connections are not currently available.

If the expected scope is missing:

- Share the page with this connection, then reload the scope list.

## Read sync status

Under **New document → Notion**, each connection shows its synchronized document count, last successful sync, next scheduled sync, and latest error. The list refreshes automatically while syncing. You can also select **Sync now**. After synchronization starts, the Knowledge list follows its progress and shows documents as they are stored. It refreshes once more as soon as synchronization finishes, so no manual refresh is required.

Synchronized documents appear in the existing Knowledge table as one expandable source folder named after the selected Notion page. Expand it to view and open its documents. Connection, sync, and disconnect controls remain under the Notion entry and do not occupy the main page.

- **Healthy**: the latest complete sync succeeded.
- **Partial failure**: some documents or provider requests failed. Existing usable knowledge is preserved and is not removed by an incomplete round.
- **Authorization invalid**: the credential expired or the connection must be authorized again.

New or changed content must still finish knowledge processing before the AI can retrieve it. Check document processing status and the Playground for confirmation.

## Updates and limits

YundaDesk runs scheduled refreshes and supports manual sync. Unchanged content is not processed again, while title-only changes can be updated without recompiling the body. Each round has document, pagination, and cumulative content-size limits to keep knowledge processing bounded.

If the provider is rate-limited or temporarily unavailable, documents from the last successful sync remain active. Retry after the provider recovers.

## Disconnect

Disconnecting deletes the connection credential and stops future synchronization. Previously imported local documents are not deleted automatically. Delete those documents from Knowledge if the AI should no longer use them.
