# YundaDesk Help Center Content

This repository is the source of truth for YundaDesk customer-facing product documentation.

It intentionally contains **content only**. It does not include a documentation framework, theme, deployment configuration, or application runtime. Any help-center frontend may consume these Markdown files.

## Languages

- Simplified Chinese: [`docs/zh-CN`](./docs/zh-CN)
- English: [`docs/en-US`](./docs/en-US)

Both locales use the same relative paths and slugs. A link can switch locale by replacing `zh-CN` with `en-US`, or the other way around.

## Content principles

1. Write for merchants, support managers, and agents, not for engineers.
2. One article should help the reader complete one task or understand one product concept.
3. Never present an unreleased, unavailable, or integration-dependent capability as ready.
4. Do not hard-code plan quotas, prices, or channel availability. Direct readers to the current product page.
5. Chinese and English articles must stay structurally equivalent, but translations should sound natural rather than literal.

## Public repository boundary

Every tracked file in this repository is public, even when the help-center frontend does not render it.

- Keep Ops and platform-operator tooling, internal APIs and services, source paths, schemas, migrations, deployment details, runbooks, incidents, logs, trace IDs, and private release gates out of this repository.
- Never commit credentials, private endpoints, real tenant/customer/employee data, or personal identity information such as names, usernames, local account names, email addresses, and home-directory or absolute paths.
- Use internal product evidence only to verify customer-visible behavior. Do not copy raw evidence into public files.
- Keep verification notes and source evidence only in the private product repository. Do not add trace or evidence files to this public repository.

## Repository structure

```text
docs/
  zh-CN/
    index.md
    01-getting-started/
    02-channels/
    03-inbox/
    04-ai-customer-service/
    05-knowledge-and-learning/
    06-yuna/
    07-proactive-outreach/
    08-customers-and-team/
    09-reports-and-billing/
    10-troubleshooting/
  en-US/
    ...same paths and slugs...
CONTENT_MAP.md
STYLE_GUIDE.md
```

## Updating documentation

When product behavior changes:

1. Verify the current UI and backend behavior in the YundaDesk product.
2. Update both locales in the same change.
3. Update `updated_at` in article front matter.
4. Check links, headings, and terminology.
5. Keep implementation notes and internal evidence out of this customer-facing repository, including non-rendered root files and Git history.

## Current release

The current bilingual release contains 65 customer articles per locale. It covers onboarding, channels, the Inbox, AI customer service, knowledge and learning, Yuna, proactive outreach, customers and teams, reporting and billing, troubleshooting, and security boundaries.

The content is intentionally task-based. It documents only capabilities that exist in YundaDesk or clearly marks integration and availability boundaries; it does not copy unrelated features from other help centers.
