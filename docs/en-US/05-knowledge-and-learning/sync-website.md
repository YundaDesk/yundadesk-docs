---
title: Sync website content
description: Crawl public pages and refresh knowledge after the website changes.
category: Knowledge and learning
order: 7
updated_at: 2026-08-07
---

# Sync website content

Website sync is intended for public, stable, crawlable help content. Authenticated pages, live order data, and customer data require proper integrations instead.

## Add a website source

1. Open the knowledge base and choose a website source.
2. Enter the full starting URL. HTTPS is used by default. If a public website intentionally supports HTTP only, enter the complete `http://` URL.
3. Review the discovered page scope.
4. Start the sync and wait for processing.
5. Test important page questions in the Playground.

## After the website changes

After the website changes, resync it. The previous successful version should remain available until a new version succeeds; a failed refresh must not erase working knowledge.

## Missing content

The bell in the top-right corner of the knowledge page shows crawl messages that need attention. Open it to review failed pages and their reasons.

If content is missing, check public access, the URL, crawl restrictions, and whether the page displays content only after interaction. Certificate problems may affect synchronization, so fix the certificate and try again. If the public site truly supports HTTP only and the HTTP address works, add it again with the complete `http://` URL. Website sync cannot replace a connected store app for private business data.
