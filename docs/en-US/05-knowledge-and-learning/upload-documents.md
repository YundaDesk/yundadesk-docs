---
title: Upload knowledge documents
description: Add reliable customer-service material to the knowledge base.
category: Knowledge and learning
order: 6
updated_at: 2026-10-07
---

# Upload knowledge documents

After product guides, policies, and procedures are uploaded, YundaDesk processes them so managed AI can use the content in answers.

## Prepare the files

Remove outdated, duplicate, or conflicting versions. Do not include secrets or unnecessary customer data. Use clear headings, and keep each document focused on a stable topic.

Supported formats include DOC/DOCX/DOCM, PPT/PPS/POT/PPTX/PPTM/PPSX/PPSM, XLS/XLSX/XLSM/XLSB, ODT/ODS/ODP, RTF, EPUB, CSV, PDF, TXT, Markdown, JSON, YAML, and EML.

## Upload steps

1. Open the knowledge document page.
2. Select the file upload action.
3. Choose a format currently supported by the product.
4. Wait for processing to finish.
5. Select **Test knowledge**, ask a real question from the document, and inspect its source.

## Select material from GitHub

If **GitHub** appears in **New document**, you can sync text material from a public repository without uploading the entire repository.

1. Open **New document → GitHub** and enter the public repository URL. Leave the branch empty to read the default branch.
2. Select **Next** to read the repository and open **Select and filter**. Expand folders and select the folders or files you need. Clicking a name also selects it. To include everything, select **Entire repository**.
3. Optionally expand **Path filters (optional)** and enter include and exclude paths, separated by commas. Both `*` and `**` are supported. For example, include `help/**` and exclude `help/examples/**` to keep demonstration material out of the knowledge base.
4. Select at least one file type: `.md`, `.markdown`, `.mdx`, `.txt`, or `.rst`.
5. Select **Next** to open **Preview and import**. Check the matched file count and list, then select **Import and sync**. Select **Back** to make changes; your selections and filters are retained. Open the preview again after editing.

A folder selection includes matching files below it, including new files in later syncs. An individual file selection syncs only that file. Path and file-type filters apply together, and exclusions take priority. Import is unavailable without a selection or a matching file.

The import button appears only when the preview has matching files. You can also select a completed step at the top to go back and edit. You cannot skip to import before completing the preview. If no files match, go back and adjust your selections or filters. Longer file lists scroll within the list while the bottom actions remain visible.

After syncing, material appears under its repository source in the document list. Find the source row in **All content**, inspect its sync status, and open the action menu on the right:

- **Sync now** reads your selected material again. Wait for an active sync to finish.
- **Auto-sync** enables or pauses future automatic syncs. The setting is retained after a page refresh.
- **Disconnect and keep documents** stops syncing after confirmation. Imported documents can still be used in AI replies.
- **Delete connection and documents** stops syncing after confirmation and moves this source's documents to Trash, excluding them from answers. The remote repository and other sources are not changed. You can restore documents from Trash if needed.

Older disconnected sources also offer deletion of their retained documents from the list. Deletion and disconnection are unavailable while syncing. If a rate-limit error appears, try again later instead of repeatedly clicking.

## After upload

A listed file is not necessarily searchable. AI can rely on it only after successful processing into the current knowledge version. If processing fails, inspect the reason before uploading the same file again.

Successfully processed documents show a **Use in AI replies** status tag. To keep a document without using it in answers, turn off **Use in AI replies** from the document menu or detail page. The original content and automatically generated FAQs stop participating in answers, but the document remains in the knowledge base and can be enabled again without another upload. FAQs disabled individually are not restored automatically.
