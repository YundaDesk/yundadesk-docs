---
title: Sync website content
description: Crawl public pages and refresh knowledge after the website changes.
category: Knowledge and learning
order: 7
updated_at: 2026-10-06
---

# Sync website content

Website sync is intended for public, stable, crawlable help content. Authenticated pages, live order data, and customer data require proper integrations instead.

## Add a website source

1. Open the knowledge base and select **New document → Crawl website**.
2. Enter the full starting URL. HTTPS is used by default. If a public website intentionally supports HTTP only, enter the complete `http://` URL.
3. Choose whether to crawl subpages. If enabled, set the crawl depth and page limit as needed.
4. Start the sync and wait for processing.
5. Select **Test knowledge** at the top of the knowledge base and ask important page questions.

The website entry shows the full starting URL of the latest crawl, including its path, so you can check where the crawl started. Pages on the same domain still appear under one website entry.

## Use this knowledge in website support

A completed crawl does not mean your website's Agent uses it. Open **AI Agents**, select the Agent serving that website channel, choose the website under **Knowledge scope**, and save. Check the bound Agent in **Channels → Reception settings** too.

Websites are selected as a whole source, not page by page. Help articles, blogs, and marketing pages can have different purposes or outdated information. Start from the help directory you need, then inspect the resulting document list. A starting path alone is not proof that unrelated content was excluded. Also check existing content if other directories on the same domain were crawled before.

Avoid conflicting answers from an outdated combined document and the new website. When replacing a source, deselect the old file or source in the Agent's knowledge scope, keep the new one, and save; you do not need to delete the old file. Use that Agent's **Test conversation**, inspect answer details for the new content, and check that unsupported features are not described as available.

## After the website changes

After the website changes, resync it. The previous successful version should remain available until a new version succeeds; a failed refresh must not erase working knowledge.

**Automatic sync** and **Use in AI answers** are independent settings in the website menu. Turn off **Use in AI answers** when the AI should temporarily ignore a site. Existing pages and automatically generated FAQs stop participating in answers, while the content and sync schedule remain available. You can turn it back on without adding the site again.

## Missing content

The bell in the top-right corner of the knowledge page shows crawl messages that need attention. Open it to review failed pages and their reasons.

If content is missing, check public access, the URL, crawl restrictions, and whether the page displays content only after interaction. Certificate problems may affect synchronization, so fix the certificate and try again. If the public site truly supports HTTP only and the HTTP address works, add it again with the complete `http://` URL. Website sync cannot replace a connected store app for private business data.
