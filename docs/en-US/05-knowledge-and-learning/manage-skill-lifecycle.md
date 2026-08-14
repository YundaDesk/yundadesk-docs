---
title: Test, pause, roll back, and delete an AI skill
description: Manage an adopted skill from testing through activation, pause, rollback, and deletion.
category: Knowledge and learning
order: 11
updated_at: 2026-08-10
---

# Test, pause, roll back, and delete an AI skill

An AI skill is a manageable answer or action. Verify when it applies, what it does, and its boundaries before enabling it.

## Test before activation

1. Open the skill detail and select the customer scenario you want to verify.
2. Review the handling steps and confirm the order of questions, decisions, actions, replies, or handoff.
3. Run the simulation, continue as a real customer, and inspect the result.
4. Cover structurally relevant paths such as successful completion, missing information, tool failure, declined confirmation, or handoff.
5. Check required knowledge, connected apps, and confirmation steps.

Scenario tests never message customers or perform real external actions. A skill can be enabled only after every required scenario passes and all required capabilities are available.

## Review live usage

The Logs view shows real skill calls from customer conversations and excludes scenario simulations. Each record includes the customer question, the AI's final answer, and the run status. When a conversation is linked, you can open the original customer conversation for further review.

## Pause a skill

Pause the skill when its rule changes or an error is found. Pausing prevents automatic use while preserving history and learning provenance.

## Roll back a skill

If a new version performs worse, roll back to the previous working version and rerun key tests. Rollback is not deletion.

## Delete a skill

When the entire skill should no longer be used, select **Delete skill** from the skill detail and confirm again. A deleted skill is hidden from the default list and cannot participate in AI reception, while historical runs, learning provenance, and audit records are retained. Prefer rollback when only the latest change is wrong, and prefer pause when you may restore the skill later.
