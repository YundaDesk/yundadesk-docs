---
title: Build and maintain the knowledge base
description: Give the AI reliable business knowledge from documents, websites, and FAQs.
category: Knowledge and learning
order: 1
updated_at: 2026-08-14
---

# Build and maintain the knowledge base

The knowledge base is the primary source for product, policy, and service answers. Each workspace uses its own content; knowledge is not shared across workspaces.

## Add knowledge

Open **AI → Knowledge base** and use the methods available on the page:

- upload product guides, policies, or service documents;
- add a website URL and crawl public pages;
- add structured frequently asked questions.

After upload or crawling, YundaDesk parses, compiles, and indexes the content. Only successfully processed content is available to AI search.

You can turn off **Use in AI answers** for an individual FAQ without deleting it. The FAQ remains in the list and can be enabled again later. A website can also be paused as a whole without changing its automatic sync setting.

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

After a successful website resync or document update, the new compiled result replaces the previous one. If a new compilation fails, the last successful result may remain available. Test different phrasings in the Playground and verify that answer details use the latest content.

## Delete content

Before deleting knowledge, check whether any AI skills or customer processes still depend on it. Retest after the index updates.
