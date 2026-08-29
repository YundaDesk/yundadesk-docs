---
title: Configure Custom API and event webhooks
description: Configure Custom API Callback or local Pull, signatures, and event webhooks.
category: Channels
order: 6
updated_at: 2026-08-29
---

# Configure Custom API and event webhooks

Custom API channels and event webhooks connect your own systems to YundaDesk. Current availability is shown on the in-product plan page.

## What happens after a plan change

If the workspace moves to a plan that no longer includes a developer-integration capability:

- Existing configuration, signing secrets, and delivery history are preserved.
- The corresponding Custom API channel or event webhook is disabled and stops accepting or sending new integration traffic.
- You can still view, disable, or delete existing configuration, but you cannot create, enable, test, replay, or rotate secrets.
- Regaining the entitlement does not restore integrations automatically. Review the configuration and enable it manually.

## Choose a reply mode

When creating a Custom API channel, choose one reply mode:

- **Callback**: YundaDesk pushes agent replies to your public callback URL. Use it when your system already has a public HTTPS service.
- **Pull (local Connector)**: a local Connector long-polls YundaDesk and forwards replies to a service on your machine. Use it for development machines, store computers, or systems without a public ingress.

Both modes are permanent options, not a migration path. One channel selects one mode, while different channels can use Callback and Pull at the same time. Customer-message ingress is unchanged and continues to use the Custom API inbound URL shown on the page.

The creation form does not show the Channel Key or signing secret. YundaDesk generates both values after the channel is saved and provides them in the saved channel details.

## Configure a Callback URL

Only Callback mode needs a callback URL. A callback or event webhook URL must:

- Be a public `https://` URL on port 443.
- Contain no username, password, or `#` fragment.
- Match the saved allowed domain. Use an explicit, controlled wildcard when multiple subdomains are required.
- Accept traffic from the fixed egress IPs published by YundaDesk.

After saving, use the page's test action. A successful test proves that the current request is reachable; before going live, also verify the signature, event payload, and source IP in the receiving system.

## Configure the Pull API

1. Create or edit a Custom API channel, set the reply mode to **Pull (local Connector)**, and save.
2. After selecting Pull, the right-hand guide shows **Send to your development Agent**. The prompt identifies two public endpoints: send customer messages to the Custom API inbound endpoint and pull agent replies from the Pull endpoint. It also includes the authentication headers, request bodies, and offset handling. Before creation, the Channel Key is a placeholder; after saving, the prompt uses the current channel value.
3. The prompt never includes the signing secret. After saving the channel, put the signing secret from the channel details into secure project configuration; never paste it into an Agent conversation, source code, logs, or the offset state file.
4. Your system calls the Pull endpoint directly. A successful response is `{ "success": true, "data": { "updates": [...], "next_offset": 1 }, "error": null }`. Start with `offset=0`, persist `data.next_offset` after processing `data.updates`, and send it with the next request. Do not advance the offset if any update fails. An empty `data.updates` array is a normal long-poll timeout.
5. If you do not want to implement polling, set `YD_CUSTOM_API_SIGNING_SECRET` securely and use the local Connector to forward replies to a local HTTP endpoint such as `http://127.0.0.1:8080/yundadesk/callback`:

```bash
customapi-pull \
  --pull-url "<Pull URL shown on the page>" \
  --channel-key "<Channel Key shown on the page>" \
  --forward-url "http://127.0.0.1:8080/yundadesk/callback" \
  --consumer-id "my-local-connector"
```

The Connector stores only a non-sensitive offset in the user configuration directory. It acknowledges a reply only after the local endpoint returns 2xx. A process interruption can repeat the last reply, but it cannot lose one by acknowledging early. Deduplicate with the `Idempotency-Key` or `X-YD-Update-ID` request header.

Do not run multiple Connectors for the same channel. To move to another machine, stop the old Connector first and securely move the offset state file. If that is not possible, make sure the receiver can deduplicate possible repeats.

## Fixed egress IPs

YundaDesk sends Custom API Callback and event webhooks from fixed egress IPs. Pull is an outbound connection from your local Connector to YundaDesk, so it does not need the YundaDesk egress allowlist. The page keeps Callback/Event Webhook egress IPs collapsed by default. When configuring the receiver, select the blue **View allowlist IPs** link, then add the displayed addresses to the receiving server's allowlist.

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
- Pull returns 401: verify the Channel Key, signing secret, local clock, and that every request uses a new nonce.
- Pull returns 409: retry only `CUSTOM_API_PULL_BUSY` after waiting. For any other 409, first confirm that the channel is still in Pull mode and that the local offset was not advanced beyond received updates; do not retry blindly.
- Pull returns 429: wait for `Retry-After` before retrying; do not add parallel pollers.
- The local receiver keeps failing: the Connector does not advance the offset. Restore the local service and return 2xx to resume.

Temporary network or DNS failures are retried automatically. After the retry limit is reached, use the replay action provided by the product.
