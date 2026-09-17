---
title: Connect WhatsApp
description: Bring WhatsApp customer messages into the YundaDesk Inbox by registering a number with Meta or using a YCloud authorized number.
search_terms: set up WhatsApp channel, WhatsApp Business API setup, YCloud authorized number, WhatsApp API Key
category: Channels
order: 5
updated_at: 2026-09-17
---

# Connect WhatsApp

The WhatsApp channel offers two ways to connect. Messaging works the same once connected. Open "Channels → Add WhatsApp" and choose the option that fits you:

- **Register a number with Meta**: register or migrate a number in Meta's official authorization window. Best if you don't have a WhatsApp API number yet.
- **Authorized number (YCloud)**: already have a WhatsApp number on YCloud? Paste your account API Key to connect. The number stays in your YCloud account.

## Register a number with Meta

1. Open "Channels", find WhatsApp in the channel market, and click "Add".
2. Choose "Register a number with Meta", then click "Connect with Meta login".
3. Sign in inside the Meta authorization window and follow the prompts to select or create the business account and number.
4. After authorization, the remaining setup completes automatically. The channel stays disabled after creation.
5. On the channel settings page, run "Test connection" and enable the channel once the check passes.

You need a Meta account that can manage business assets, plus a business number usable for WhatsApp.

## Authorized number (YCloud)

### Before you start

1. Sign up on the [YCloud website](https://www.ycloud.com/) and log in to the console.
2. Complete the WhatsApp business account and number setup in the YCloud console.
3. Copy the account API Key from the developer settings in the console.

### Connect

1. Open "Channels", find WhatsApp in the channel market, and click "Add".
2. Choose "Authorized number (YCloud)".
3. Paste the API Key and click "Find available numbers".
4. Pick the number to connect. Numbers that are not fully set up or already connected are marked with a reason and cannot be selected.
5. Confirm the channel name and click "Finish connecting". The channel is created first, the connection is checked automatically, and the channel is enabled once the check passes.

You can then receive and reply to customers of that number in the Inbox. The full API Key is never shown again after saving.

### After connecting

- **Check failed**: the channel is saved as disabled. Retry on the connect page later, or run "Test connection" on the channel settings page to troubleshoot before enabling.
- **Rotate the API Key**: after rotating the key in your YCloud console, paste the new key into "New API Key" on the channel settings page and save. Leave it blank to keep the current key.
- **Switch numbers**: disconnect the channel on its settings page, then connect again. Once disconnected, the original number becomes available to select again.
- **Message fees**: billed through your YCloud account, independent of your YundaDesk plan.

## Reply window

Per WhatsApp's official rules, you can reply freely within 24 hours of the customer's last message. After 24 hours, direct replies are temporarily unavailable until the customer messages again.

## Troubleshooting

- **"API Key is invalid"**: check in the YCloud console whether the key is correct or has been rotated, then paste the latest key.
- **No numbers listed**: make sure the WhatsApp number setup is complete under that YCloud account; newly set up numbers may take a moment—search again later.
- **Number marked "setup incomplete"**: finish the number setup in the YCloud console, then search again.
- **Number marked "already connected"**: each number can only be connected once at a time; disconnect the original channel on its settings page first to rebind.
- **Test connection fails**: confirm the key has not been revoked and the number is still under the account in a normal state, then retry.
