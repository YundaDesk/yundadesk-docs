---
title: Deactivate, disconnect, uninstall, and use privacy tools
description: Safely manage the YundaDesk plugin lifecycle, WordPress privacy requests, reauthorization, and common failures.
category: Apps and integrations
order: 5
updated_at: 2026-08-05
---

# Deactivate, disconnect, uninstall, and use privacy tools

Deactivation, disconnection, and deletion have different effects. Choose the action that matches whether you intend to pause the plugin, move the site, or remove the integration.

## Understand each lifecycle action

| Action | WordPress Widget | WooCommerce enhancement | Local connection information |
|---|---|---|---|
| Deactivate YundaDesk | Stops loading | Pauses synchronization and YundaDesk-created events | Kept for recovery |
| Disconnect site | Stops loading | Pauses and revokes the YundaDesk connection | Removed after the disconnect completes |
| Delete the plugin | Stops loading | Removes plugin-owned event configuration | Plugin options and temporary data are removed |
| Deactivate WooCommerce only | Continues working | Pauses | WordPress connection remains |

To disconnect, open **Settings → YundaDesk**, select the disconnect action, and wait for confirmation before deleting the plugin. If WooCommerce was authorized, also open **WooCommerce → Settings → Advanced → REST API** and remove the YundaDesk key after disconnection.

Disconnecting one site does not disconnect other WordPress sites in the same YundaDesk workspace.

## Export personal data

1. In WordPress Admin, open **Tools → Export Personal Data**.
2. Enter the verified requester's email address.
3. Send or confirm the request using the normal WordPress process.
4. Generate the export after WordPress marks the request confirmed.

The YundaDesk exporter returns support data associated with the current connected site. Data that belongs independently to another connected site is not included.

## Erase personal data

1. Open **Tools → Erase Personal Data**.
2. Enter the verified requester's email address.
3. Complete the normal WordPress confirmation process.
4. Run erasure and review the result from every participating plugin.

The YundaDesk eraser applies only to the current site's connection. A remote deletion that cannot finish is reported as incomplete so the administrator can retry it. Site administrators must verify the requester and decide whether any data must be retained for legal reasons.

![WordPress personal-data export and erasure tools](/help/assets/docs/wordpress/en/privacy-tools.jpg "Use WordPress privacy tools for the connected site")

## Move the site to another domain

Disconnect YundaDesk on the old address before completing the move. After WordPress uses the new HTTPS origin, open **Settings → YundaDesk** and connect it again. Do not reuse an old pairing link or copy connection values between origins.

## Troubleshooting

### The Widget does not appear

- Confirm that the site says **Connected** under **Settings → YundaDesk**.
- Test a public page rather than WordPress Admin, a login page, a feed, or a REST response.
- Clear page and CDN caches after connecting.
- Confirm that the site's content security policy allows the YundaDesk API and Widget loader listed in [Data and permissions](./data-and-permissions.md).

### WooCommerce is not detected

- Confirm that WooCommerce is active on the same WordPress site.
- Upgrade WooCommerce to version 8.2 or newer.
- Reload **Settings → YundaDesk**.

### Reauthorization is required

Select the read-only WooCommerce connection again and approve **Read**. Do not create and paste a Consumer Key or Consumer Secret into YundaDesk.

### Synchronization or events are degraded

Open **Settings → YundaDesk**, refresh the status, and retry the supported recovery action. If the problem continues, record the site address, approximate time, YundaDesk plugin version, WordPress version, WooCommerce version, and the non-sensitive error shown on the page before contacting [YundaDesk Support](https://yundadesk.com/contact/). Never send passwords, API keys, customer addresses, or full order records in a support ticket.
