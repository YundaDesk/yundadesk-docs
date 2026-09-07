---
title: Create and manage Yuna Automations
description: Run workspace tasks on demand or on a schedule, and execute customer outreach safely.
category: Yuna
order: 8
updated_at: 2026-09-07
---

# Create and manage Yuna Automations

Yuna Automations are for work that needs to run on demand or repeat on a schedule. Yuna can run an internal report directly, or you can delegate a workspace task to one explicit Agent. When **Customer outreach** is available on the page, you can also repeat prepared outreach with human approval before every send.

## Before you begin

- You need permission to use Yuna and read the data required by the task. If **Automations** is missing, ask a workspace administrator to check your access.
- If you select an Agent, it must be enabled with the required read-only capabilities. Internal reports run directly by Yuna do not require a separate Agent.
- Customer outreach appears only when your access and the current workspace make that task type available. If nothing is ready to select, you can prepare it with Yuna directly from the Automation setup.

## Create with Yuna

1. Expand **Yuna** in the main navigation and select **Automations**.
2. Select **Create**. This opens Yuna by default. You can also open the adjacent menu and explicitly select **Create with Yuna**.
3. Describe the task, time, and recipient, for example “Send me visitor conversation statistics every day at noon.” Yuna uses available workspace information and asks only for missing required details.
4. Review the schedule and time zone. Yuna can run an internal report directly; select an Agent when the task needs one.
5. After the required information is complete, Yuna creates the draft and shows the result. Return to the Automations list to review it.

**Create with Yuna** creates a workspace-task draft. It does not prepare or send customer outreach.

## Set up manually

1. Open the menu beside **Create** and select **Set up manually**.
2. Enter the instruction. The page derives the list title from the first sentence, so there is no separate name field.
3. Select a task type:
   - **Workspace task:** Select an enabled Agent. The page loads the read-only capabilities currently available to that Agent, and results stay in the workspace.
   - **Customer outreach:** Select the executing Agent, then select prepared customer outreach. If nothing is ready, select **Prepare customer outreach with Yuna** and follow the prompts to confirm the audience, sending channel, message, and sending limits. After reviewing and confirming it, return to the Automation setup and select it. Every real send still requires human approval.
4. Select **On demand**, **Every day**, **Weekdays**, or **Every week**. Scheduled work uses the time zone shown on the page.
5. Select **Create**.

A new Automation is saved as a draft. Open its details to check the task type, execution target, frequency, and instruction, then turn on the switch on its card.

## Run, pause, and edit

- Search by name, Agent, or instruction, and filter by Draft, Active, or Paused.
- Open the details to edit an Automation. Saving an edit creates a new version, and later runs use that version.
- **Run now** is available only in the details. You can run a draft, active, or paused internal read-only Automation once without enabling future scheduled runs.
- Turning off the card switch pauses future automatic triggers without disabling a one-time manual run from the details. Scheduled runs missed while paused are not backfilled.
- Open **Run history** to review the time, version, status, and result summary for each run. You can stop a run that is still queued or running.

## When confirmation is needed

Saving or editing a draft, pausing a task, and running an internal read-only report once need no extra approval. Activating a schedule for the first time requires confirmation. Changing an active task's content or time requires one confirmation; it stays active when its execution scope is unchanged. An internal task with unchanged authorization can resume directly. Customer sends and expanded execution scope still require the review shown by the product.

## Approve customer outreach

Customer outreach does not send automatically just because its run time arrives:

1. Open **Run history** for the Automation.
2. Select **Review and approve** for a run that is waiting for approval.
3. Check the audience, channel, recipient count, and message preview.
4. Select **Approve and execute** to continue, or **Reject this run** to end it.

The audience and message remain fixed after the preview is prepared; approval cannot silently expand them. Approval allows the sending flow to continue. Check the outreach result and real channel status to confirm final delivery.

## Troubleshooting

- **No Agent is available:** Enable an Agent and confirm that it has a read-only capability shown as available on the page.
- **Customer outreach is unavailable:** This task type appears only when your access allows it. If the type appears but there is nothing to select, choose the executing Agent and select **Prepare customer outreach with Yuna**. Return to Automations after reviewing and confirming it.
- **Run now is unavailable:** Check your current permissions and the task details. Draft and paused internal read-only Automations support a one-time run.
- **A run stays at Waiting for approval:** Open Run history and approve or reject it. Nothing is sent without approval.
- **A run fails:** Read the result summary, correct the permission, Agent, audience, or channel issue shown by the product, then try again.


## Workspace outreach rules

In **Yuna → Automations**, select **Outreach rules** to manage quiet hours, cooldown, and the seven-day customer touch limit. These rules are shared across the workspace and do not affect internal reports sent to you. Viewing and editing require permission to manage outreach.

A limit of zero means no count limit; other outreach restrictions still apply. Save proactive suggestion handling with the single mode selector. Each Automation retains its own activation and approval rules. Select **Save**, then reopen the page to verify your changes.
