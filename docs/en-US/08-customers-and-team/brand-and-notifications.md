---
title: Configure brand and notifications
description: Manage customer-facing identity and team reminder preferences.
category: Customers and team
order: 4
updated_at: 2026-08-13
---

# Configure brand and notifications

Brand settings affect the identity and widget experience customers see. Notification settings control how team members learn about new messages and system tasks.

## Brand settings

Depending on the current page, you can manage the workspace name, AI service identity, avatar, brand color, and website widget presentation. Verify changes on the real site and customer channel, not only in an admin preview.

White-label and advanced brand controls may depend on plan entitlements. The page is authoritative.

## Notifications

Members can adjust desktop notifications, unread reminders, and Yuna task alerts according to their responsibilities. Browser notifications require separate permission, and operating-system focus modes can suppress them.

After you enable **Browser notifications** in **Settings → Message notifications** and grant browser permission, supported desktop browsers can continue showing new-message alerts after the YundaDesk tab is closed. Signing out stops notifications for the previous workspace.

When a visitor sends a message in the conversation you are currently viewing, the workspace still shows an in-app alert and plays its short sound. Browser notifications continue alerting you when the tab is hidden or closed. Whether the system notification itself makes a sound still depends on the browser and operating system.

Use **Send test** to verify the current browser. It sends a real browser push and, when sound alerts are enabled, plays a short local test tone. The test push is shown even while the page is in the foreground, but it does not appear in the in-app notification list. Whether the system notification itself makes a sound still depends on browser, operating-system notification, and focus-mode settings.

The bell in the top-right corner is the in-app notification entry point. It opens a dedicated panel, lightly dims the current page, and keeps scrolling inside the panel:

- **To do** answers “What needs my attention now?” and separates conversations needing replies, confirmations, and issues to investigate. Unfinished work remains here even after its notification is read.
- **Activity** answers “What happened recently?” and includes messages, announcements, configuration changes, read items, and completed work.
- Repeated reminders for the same conversation, task, or shared diagnostic destination may be grouped. Unrelated work is never merged into one destination.
- Select a notification to open its conversation or destination page.
- **Mark all read** is available in Activity. It clears unread notification state but does not complete the underlying conversation or task.

## Recommendations

- Use a name and avatar customers recognize.
- Avoid frequently changing the customer-facing identity.
- Members responsible for channel failures and high-risk tasks should retain the relevant alerts.
- Agents should retain new and assigned conversation alerts.
- After a change, verify the web UI, browser notification, and connected phone channel separately.
- To receive alerts after closing the page, do not clear site data or revoke the site's notification permission.
