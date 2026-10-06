---
title: Upload knowledge documents
description: Add reliable customer-service material to the knowledge base.
category: Knowledge and learning
order: 6
updated_at: 2026-10-06
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
2. Select **Load files**, expand folders, and select the folders or files you need.
3. Optionally enter include and exclude paths, separated by commas. Both `*` and `**` are supported. For example, include `help/**` and exclude `help/examples/**` to keep demonstration material out of the knowledge base.
4. Select at least one file type: `.md`, `.markdown`, `.mdx`, `.txt`, or `.rst`.
5. Select **Preview import**, check the matched file count, then select **Import and sync**. Preview again after changing selections or filters.

A folder selection includes matching files below it, including new files in later syncs. An individual file selection syncs only that file. Path and file-type filters apply together, and exclusions take priority. Import is unavailable without a selection or a matching file.

After syncing, material appears under its repository source in the document list. Open **New document → GitHub** to inspect the connection and select **Sync now**. If a rate-limit error appears, try again later instead of repeatedly clicking.

## After upload

A listed file is not necessarily searchable. AI can rely on it only after successful processing into the current knowledge version. If processing fails, inspect the reason before uploading the same file again.

Successfully processed documents show a **Use in AI replies** status tag. To keep a document without using it in answers, turn off **Use in AI replies** from the document menu or detail page. The original content and automatically generated FAQs stop participating in answers, but the document remains in the knowledge base and can be enabled again without another upload. FAQs disabled individually are not restored automatically.
