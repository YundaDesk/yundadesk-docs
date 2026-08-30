---
title: Fix missing Inbox notifications
description: Troubleshoot browser notifications, sounds, and unread reminders.
category: Troubleshooting
order: 5
updated_at: 2026-08-29
---

# Fix missing Inbox notifications

Notifications require permission in YundaDesk, the browser, and the operating system.

## Troubleshoot

1. Open YundaDesk notification settings and enable the intended alert.
2. Allow notifications and sound for the site in the browser.
3. Check system notifications, focus mode, and audio settings.
4. Stay signed in to the correct workspace.
5. Ask another member or a test visitor to send a new message.

Test four states separately: sign in without opening the Inbox, keep the target conversation open, move to another YundaDesk page, and put the YundaDesk tab in the background. The first three should produce an in-app alert and short sound; the background state also attempts the short sound and is backed by the browser's system notification.

If notifications work only while the page is open, also check:

- Turn **Browser notifications** off and on again in **Settings → Message notifications**, then allow notification permission for the current browser again.
- Confirm that site data was not cleared, the browser is not in private mode, and site permissions were not automatically removed.
- In Safari, allow notifications for this site. Background web notifications on iPhone and iPad also depend on the operating-system version and Add to Home Screen support.
- Check whether a company network or browser extension blocks the browser's push service.

For a real test, close the YundaDesk tab and have another member or visitor trigger a new event that matches your notification preferences. Refreshing an old notification does not send it again.

## Incorrect unread count

If the unread count is wrong, refresh and verify whether conversations are actually read. Preserve the steps and time if the count and list remain inconsistent; do not repeatedly click items just to hide the mismatch.

## Understand a failure notification

Open the relevant category from the notification bell. When reliable details are available, a failure notification shows a concise reason and log. Select **Ask Yuna** to have Yuna explain what is known, what may be affected, and whether you need to do anything.

A failure notification does not send you directly to technical logs, an Agent page, or a broad list. If the notification is linked to a specific conversation or message, Yuna can identify it in the answer. If the available facts are incomplete, Yuna says so instead of guessing. Asking marks the notification as read; it does not retry the task or change workspace settings.

## Mobile notifications

Mobile notifications also depend on the available app and operating-system permissions. Test only officially available clients.
