---
title: Configure Custom API and event webhooks
description: Set up developer integrations, callback URLs, signatures, and fixed egress IPs.
category: Channels
order: 4
updated_at: 2026-07-31
---

# Configure Custom API and event webhooks

Custom API channels and event webhooks connect your own systems to YundaDesk. They are grouped as developer integrations. Current availability is shown on the in-product plan page; Pro, Enterprise, and custom plans that inherit the entitlement can create and enable them.

## What happens after a plan change

If the workspace moves to a plan without developer integrations:

- Existing configuration, signing secrets, and delivery history are preserved.
- Enabled Custom API channels and event webhooks are disabled and stop sending new requests.
- You can still view, disable, or delete existing configuration, but you cannot create, enable, test, replay, or rotate secrets.
- Regaining the entitlement does not restore integrations automatically. Review the configuration and enable it manually.

## Configure a callback URL

A callback or event webhook URL must:

- Be a public `https://` URL on port 443.
- Contain no username, password, or `#` fragment.
- Match the saved allowed domain. Use an explicit, controlled wildcard when multiple subdomains are required.
- Accept traffic from the fixed egress IPs published by YundaDesk.

After saving, use the page's test action. A successful test proves that the current request is reachable; before going live, also verify the signature, event payload, and source IP in the receiving system.

## Fixed egress IPs

YundaDesk sends Custom API callbacks and event webhooks from fixed egress IPs. The page keeps egress IPs collapsed by default. When configuring the receiver, select the blue **View allowlist IPs** link, then add the displayed addresses to the receiving server's allowlist.

If the page says no egress IPs have been published, contact YundaDesk support instead of allowing traffic from every source. The page may show multiple IPs; allow all of them.

## Verify requests

Verify the YundaDesk signature and timestamp in the receiving system, and use the event or delivery ID for idempotency. Do not use source IP as the only authentication control.

Use the public Custom API inbound URL shown in the product. Sending the same signed receipt again does not apply the delivery transition twice.

## Troubleshoot delivery failures

Start with the delivery status and error type on the relevant Custom API or event webhook page:

- Plan or quota blocked: check the current plan and usage.
- URL or domain rejected: verify HTTPS, port, domain, and URL contents.
- Timeout or target unavailable: confirm that the target is online and allows every published egress IP.
- Signature rejected: verify the current secret; after rotation, confirm that the receiver uses the new secret.

Temporary network or DNS failures are retried automatically. After the retry limit is reached, use the replay action provided by the product.
