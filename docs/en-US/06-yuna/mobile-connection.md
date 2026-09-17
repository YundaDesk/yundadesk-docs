---
title: Connect Yuna to a phone channel
description: Continue using the same Yuna through a supported messaging app.
category: Yuna
order: 4
updated_at: 2026-09-07
---

# Connect Yuna to a phone channel

A phone connection lets an authorized workspace member use Yuna through a supported messaging app and receive important reminders. It is not a customer channel and does not create customer or visitor conversations.

## Connect

1. Open Yuna's phone connection page.
2. Select one of the connection methods shown.
3. Follow the QR, account verification, or secure credential steps.
4. Wait for the connected state, then send a read-only test question.

Available providers are shown on the current page. Submit credentials only through the secure setup flow.

## Sessions and reminders

Web and phone access use the same workspace context. Workspace memory and personal preferences help Yuna stay consistent, while the content mirrored to a phone provider may be limited by policy and permission.

## Approve an action from your phone

Review the action in the pending approval message. If this conversation has one pending approval, reply `/approve` to approve it or `/deny` to reject it. When several approvals are pending, use `/approve ID` or `/deny ID` from the message to select one.

Commands apply only to valid approvals already shown in the current phone conversation. Expired, resolved, or other-conversation approvals cannot be executed this way. Repeating a command does not repeat the action. Check the execution result afterward: approval alone does not mean the action or delivery has completed.

Phone actions use the connection owner's current workspace permissions. Revoked permissions cannot be reused through an older connection.

## Revoke or transfer

Use the same page to revoke a connection, update its state, or transfer ownership where supported. Revoke immediately and rotate relevant credentials when a phone is lost, a member leaves, or an account is compromised.
