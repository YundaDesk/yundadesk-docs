---
title: Manage skills and customer memory
description: Inspect learned capabilities, disable incorrect skills, and manage customer-specific memory.
category: Knowledge and learning
order: 4
updated_at: 2026-08-30
---

# Manage skills and customer memory

Skills and customer memory solve different problems. Skills are reusable business capabilities. Customer memory adds context for one specific customer.

## Skills

Expand **AI Agents**, select **Skills**, and inspect adopted and generated capabilities. A skill detail can show:

- trigger or applicable customer question;
- response steps, required business information, and handoff boundaries;
- learning source and version;
- tests, runs, and real usage;
- current enablement state.

Skill details explain how the skill handles a request without requiring merchants to configure internal processes. If a skill is wrong, pause or roll it back, then create a corrected version through correction and an improvement suggestion.

## Customer memory

Customer memory stores preferences, restrictions, or durable context for one customer, such as language preference or a material allergy. It does not become a skill shared with every customer.

Open **Customer memory** from an adopted improvement suggestion, a skill source, or the customer profile. Repeated statements of the same preference are merged for that customer. A clear and newer preference automatically replaces the old value while preserving version history. If a new statement is ambiguous, the system keeps the current trusted value instead of letting uncertain content overwrite it or waiting for team approval. Incorrect memory can still be edited or removed.

Customer memory cannot override policy facts in the knowledge base and should not contain unnecessary sensitive data.

## How to choose

Use skills or knowledge for behavior shared across customers, customer memory for one customer's preferences, and Yuna long-term memory for the merchant team's own working preferences.
