---
title: Build and maintain the knowledge base
description: Give the AI reliable business knowledge from documents, websites, and FAQs.
category: Knowledge and learning
order: 1
updated_at: 2026-08-30
---

# Build and maintain the knowledge base

The knowledge base is the primary source for product, policy, and service answers. Each workspace uses its own content; knowledge is not shared across workspaces.

## Add knowledge

Expand **AI Agents** in the main navigation, select **Knowledges**, and use the methods available on the page:

- upload product guides, policies, or service documents;
- add a website URL and crawl public pages;
- add structured frequently asked questions.

After upload or crawling, YundaDesk parses, compiles, and indexes the content. Only successfully processed content is available to AI search.

You can turn off **Use in AI answers** for an individual FAQ without deleting it. The FAQ remains in the list and can be enabled again later. A website can also be paused as a whole without changing its automatic sync setting.

## Browse and locate content

The knowledge base uses a file-manager layout to organize real sources:

- **All content** shows uploaded documents, websites, and connected sources.
- **Needs attention** collects documents that failed processing and need review.
- **Recent** sits above **Trash** at the bottom of the source rail and uses the times you actually opened documents. Each member has their own recent list.
- Create single-level folders and move standalone uploaded documents into them. Select a folder, then choose **New document → Upload file**. The upload area shows the destination as **data source / folder** before you choose a file, and the new file is saved directly in that folder. Folders cannot be nested.
- Every folder, including an empty folder, keeps a disclosure arrow. Expand it to view and open documents without leaving the current file-manager view.
- Each website domain and connected source is its own directory. Open it to browse only that source's documents.
- Website and connected-source directories are managed by their sync source and cannot be renamed or moved into custom folders.
- **Trash** keeps removed documents so you can restore or permanently delete them.
- After opening a document, use the clickable **All content** and current source or folder segments in the path above the document list to return.
- Open a document to read it inside the current file-manager view; the source rail stays visible. Select **Back to documents** to return to the same directory.
- **Documents** and **FAQ** remain separate content types and are managed on their own tabs.

Custom folders only organize documents; they do not change how AI uses the knowledge. Deleting a folder does not delete its documents. The documents return to the root.

The reader formats Markdown headings, lists, tables, quotes, and code. Word, PDF, and website sources are first converted into a safe text structure; HTML or scripts carried by a document are not executed. If a source depends on complex layout, images, or scanned pages, the reader may show only the successfully extracted text, which is also the content available to AI search.

## File formats and limitations

- Documents: DOC, DOCX, DOCM, ODT, RTF, and EPUB.
- Spreadsheets: XLS, XLSX, XLSM, XLSB, ODS, and CSV.
- Presentations: PPT, PPS, POT, PPTX, PPTM, PPSX, PPSM, and ODP.
- Other text sources: PDF, TXT, Markdown, JSON, YAML, and EML.
- Standalone PNG, JPG, JPEG, and WebP images can be uploaded. YundaDesk uses OCR to extract readable text; clear, high-contrast Chinese or English text works best.
- A scanned or image-only PDF is not OCR-processed as a PDF. Export its pages as supported image files or add a selectable text layer before uploading.
- Images embedded inside another document are not read separately. Include important information in the document text.
- Only successfully processed text becomes available to AI search. If OCR cannot extract readable text, improve the image quality or upload a text version.

## Write reliable content

- Keep one clear topic per source or section.
- State the scope and effective period of prices, timelines, and refund policies.
- Remove conflicting outdated versions.
- Never upload keys, identity documents, payment data, or unrelated sensitive information.
- Connect the appropriate business app for real-time orders, inventory, and tracking. Static documents cannot stand in for live facts.

## Update and verify

After a successful website resync or document update, the new compiled result replaces the previous one. If a new compilation fails, the last successful result may remain available. Select **Test knowledge** at the top of the knowledge base; it appears immediately before **New folder**. Test different phrasings and verify that answer details use the latest content.

## Delete content

Before deleting knowledge, check whether any AI skills or customer processes still depend on it. Moving a document to Trash removes it from new AI answers immediately. You can restore it to its previous folder when needed. Permanent deletion is available only in Trash and cannot be undone. Retest related questions after making changes.
