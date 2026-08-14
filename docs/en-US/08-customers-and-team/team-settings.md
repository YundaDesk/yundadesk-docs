---
title: Manage members, permissions, and shared resources
description: Invite teammates, assign access, and maintain shared labels and quick replies.
search_terms: use saved team quick replies, insert quick reply in agent composer, shared quick reply location
category: Customers and team
order: 2
updated_at: 2026-08-11
---

# Manage members, permissions, and shared resources

Team settings determine who can view customers, handle conversations, change AI configuration, and access reports.

## Invite a member

Open **Settings > Members and permissions**, enter the member's email address, and select Administrator or Agent. The invited member follows the page instructions to join before accessing the workspace.

Administrators can invite either administrators or agents. **Invite agents** is a separate sensitive permission: a regular agent who receives it can see the invitation action and invite regular agents, but cannot create an administrator.

For members with team-management access, the member list shows each person's most recent successful Web or App sign-in and most recent workspace use, helping identify accounts that have been inactive for a long time. Members who have never signed in or used the workspace show the corresponding empty state, while pending invitations show an em dash. The regular member directory does not expose these activity times.

## Roles and permissions

- **Administrators** always have every workspace permission. Their permissions are fixed and cannot be changed in the matrix.
- **Agents** receive individual permissions based on their responsibilities. A separate manager role is not required.

Open **Permission management** to view permissions as rows and members as columns. Apply a preset to an individual agent, or use a module-level selector to grant or clear a group of permissions. Filters change only the view and never change grants implicitly. When changes are pending, the summary, reason field, and save action appear in the existing right side of the dialog header without adding a footer or covering, moving, or resizing the matrix. Enter a reason and save the changes together.

**All permissions** covers every delegable tenant feature, including the YundaDesk AI overview, Yuna, AI Learning, AI Skills, Knowledge, Customer Memory, Playground, Reception settings, and advanced settings such as General, Branding, Billing, Security, Webhooks, and Proactive Outreach. Identity-level or irreversible capabilities—creating administrators, granting **Manage agent permissions**, connecting Yuna to a phone, and deleting the workspace—remain administrator-only. Follow least privilege: service agents usually need conversation and customer access, while channel, AI, reporting, or team-management permissions should go only to members who need them.

**Manage agent permissions** is sensitive. Only an administrator can grant or revoke it. An agent who has it may manage permissions for other regular agents, but cannot change an administrator, change their own permissions, or grant this permission to someone else. They may delegate only permissions they already hold, so permission management cannot expand their own authority.

## Maintain shared resources

- **Quick replies:** Shared answers that agents can insert in the composer.
- **Labels:** A consistent customer classification system for the whole team.
- **Brand and language:** Workspace and customer-facing identity settings.
- **Notifications:** Personal reminder preferences based on each member's responsibilities.

## Security recommendations

Review permissions when responsibilities change. Disable or remove access promptly when a member leaves, inspect login records, and never share one account between multiple people.
