---
title: Configure brand and notifications
description: Manage customer-facing identity and team reminder preferences.
category: Customers and team
order: 4
updated_at: 2026-08-30
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

The bell in the top-right corner is the in-app notification entry point. It first shows four categories: Customer conversations, AI & automation, Channels & settings, and System & announcements. Each category shows its unread count and latest notification; the bell does not expand every individual notification.

Categories follow what you need to handle next. For example, channel-delivery failures and configuration reviews appear under **Channels & settings** instead of being placed under **AI & automation** only because AI detected them.

If a category has unread notifications but its latest record is outside the bell's preview range, the category shows its notification count. Select the category to load its concrete notifications; it is not incorrectly labeled as empty.

- Select a category to view its notifications, or select **View all notifications** for the complete list.
- The detailed list supports All/Unread, search, category filtering, and pagination.
- Failure notifications remain normal rows. A plain-language reason appears only when a reason fact exists, and a log appears only when it can be shown safely. Older notifications without a stored reason do not invent a failure-reason block.
- Notification rows do not navigate. A normal notification shows **Open conversation** or **Open channel** only when it can identify one exact destination. It does not send you to an Agent page, list, settings home, or generic details page to investigate on your own.
- A failure notification shows **Ask Yuna**. Yuna opens in a new conversation with the exact failure task already selected, explains the known reason and impact, and provides an exact conversation location only when that fact exists. It does not retry, change settings, guess an unknown cause, or mark the failure as resolved.
- **Mark all read** clears unread notification state but does not complete the underlying conversation, task, or failure.

## Recommendations

- Use a name and avatar customers recognize.
- Avoid frequently changing the customer-facing identity.
- Members responsible for channel failures and high-risk tasks should retain the relevant alerts.
- Agents should retain new and assigned conversation alerts.
- After a change, verify the web UI, browser notification, and connected phone channel separately.
- To receive alerts after closing the page, do not clear site data or revoke the site's notification permission.
