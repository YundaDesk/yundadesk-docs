# Customer Documentation Style Guide

## Audience

Write for a merchant owner, support manager, or support agent who wants to finish a task without understanding YundaDesk's internal architecture.

## Voice

- Clear, calm, and direct.
- Use short paragraphs and task-oriented headings.
- Explain a product term the first time it appears.
- Prefer “select”, “open”, and “confirm” over vague phrases such as “handle it in the system”.
- Do not use internal table names, service names, capability codes, trace IDs, enum values, or migration terminology.

## Product terms

| Chinese | English | Meaning |
|---|---|---|
| AI 客服 | AI customer service | The customer-facing capability provided by channel-bound Agents |
| Agent | Agent | One customer-facing AI configuration with one Role and its own knowledge, capabilities, behavior, and channels |
| Yuna | Yuna | The merchant-facing assistant for questions, actions, learning, and reminders |
| 工作台 | Inbox | The workspace where teams manage customer conversations |
| 工作空间 | Workspace | The grouped navigation for Knowledge, Skills, Marketing, and Improvement suggestions |
| 知识库 | Knowledges | Merchant-provided sources used to ground AI answers |
| 改进建议 | Improvement suggestions | The review queue for proposed AI improvements |
| 技能 | Skills | Adopted, manageable AI capabilities and response procedures |
| 客户记忆 | Customer memory | Customer-specific preferences used only for that customer |
| 主动触达 | Proactive outreach | Governed outbound messages initiated by a trigger or schedule |
| 测试对话 | Test conversation | A safe dialog for testing a selected Agent before serving customers |

## Accuracy rules

- Say “available channels are shown on the Channels page” instead of listing every roadmap channel as supported.
- Say “some actions depend on connected store or channel capabilities” when an integration is required.
- A learning suggestion is not active until the merchant adopts it.
- Yuna memory is not customer memory, and neither replaces the knowledge base.
- External AI can answer customers but does not participate in YundaDesk managed learning.
- Never promise that Yuna can execute an action unless the workspace has the required capability and the user confirms the action.
- Describe only what merchants see and can do in the product. Do not describe internal platform tooling or infrastructure. When something is unavailable, tell readers to contact YundaDesk support.

## Confidentiality and public boundaries

- Treat every tracked file and every commit as public, not only Markdown rendered by the help center.
- Never document Ops or platform-operator workflows. “Administrator” in an article may refer only to a merchant workspace administrator.
- Do not include internal repository paths, source files, service or API names, schemas, migrations, deployment topology, runbooks, incidents, logs, trace IDs, credentials, private endpoints, real tenant/customer/employee data, or personal identity information such as names, usernames, local account names, email addresses, and home-directory or absolute paths.
- Public integration requirements may describe what a customer must configure, but must not reveal internal infrastructure or security-control implementation.
- Do not publish internal launch gates or roadmap commitments. State only the capability's current customer-visible availability.
- Keep source evidence private and only in the private product repository. Do not add trace or evidence files here.

## Article template

```markdown
---
title: Article title
description: One-sentence summary
category: Category name
order: 1
updated_at: YYYY-MM-DD
---

# Article title

Short explanation of the outcome.

## Before you begin

Prerequisites and permissions.

## Steps

1. ...

## What happens next

Observable result and boundaries.

## Troubleshooting

Common failure modes.
```
