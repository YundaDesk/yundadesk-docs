---
title: Create and configure an Agent
description: Select one Role, then configure the Agent's knowledge scope, tools and actions, skills, reception settings, and channels.
search_terms: default AI customer service, configure reception behavior, AI reception settings
category: AI customer service
order: 1
updated_at: 2026-08-29
---

# Create and configure an Agent

Open **AI Agents** from the main navigation to manage customer-facing Agents by business responsibility. An Agent has one Role and can handle multiple channels. A channel can be bound to only one Agent at a time.

## Create an Agent

1. Open **AI Agents** and select **New Agent**.
2. Choose the Role that best matches the reception goal.
3. Enter a name your team can recognize, then confirm creation.
4. Continue setup on the new Agent's detail page.

A new Agent does not serve customers or take over existing channels automatically. Its Role defines the reception goal; it does not add knowledge or enable tools by itself.

## Complete setup

Review each section on the detail page:

- **Role & behavior:** Confirm the name, Role, service style, additional instructions, tone, and reply behavior. To create or adjust the service style, select **Create/Adjust with Yuna**.
- **Knowledge scope:** Select the files, folders, Notion content, or websites this Agent may use in answers.
- **Tools & actions:** Enable only the query or action tools this Agent needs.
- **Skills:** Enable or disable customer-reception skills that belong to this Agent. For repeated outreach, use **Yuna → Automations**.
- **Reception settings:** Define when an unknown, sensitive, or unsupported request should go to a person.
- **Reception channels:** Select the channels this Agent should handle.
- **Run history:** Review recent test or reception runs and open answer details to inspect supporting evidence.

If a selected channel is already bound to another Agent, the page asks you to confirm the transfer. New customer conversations use the new binding; active conversations continue with their original Agent.

Service style keeps the same Agent's self-description, character, and expression habits stable. The Agent page shows the current summary. After you select **Create/Adjust with Yuna**, Yuna opens as a floating conversation on the current page, so you do not lose your place in the configuration. Yuna reads the existing service style and asks one necessary question at a time about the customer experience, speaking habits, and expressions to avoid. Once the request is clear, Yuna saves it directly and reports the result in the conversation without an extra confirmation card.

Service style remains the same when the Role's active skill changes, so customers experience one continuing service representative across different tasks. Service style changes how the Agent speaks; it does not add knowledge, enable tools, bypass approvals, or change business policies. Examples are not factual knowledge. Prefer observable behavior such as “give an anxious customer the clearest next step first” instead of making permanent personality judgments from one conversation.

You can also open **Channels**, enter a channel's **Reception settings**, and choose its **Reception Agent** directly. Select **Human reception** to remove the Agent binding. This selector and **Reception channels** on the Agent detail page edit the same setting, so a change in either place appears in the other. Selecting a disabled Agent retains the binding, but the Agent must be enabled before it handles new conversations automatically.

The picker separates files and folders, Notion and other connections, and websites. Folder contents keep their hierarchy, so you can select one file or the whole folder. Websites are selected as a whole; individual crawled pages are not selectable. A folder, connection, or website also includes newly synced content within that scope. Choose at least one item before saving; the system never expands the scope automatically.

Tools and actions from connected apps or plugins appear alongside built-in tools. An extension that is not connected does not appear in the Agent form; follow the page prompt to install or connect an app when needed. Enabling a tool does not bypass member permissions. Actions such as refunds, order cancellations, or sending messages may still require confirmation from an authorized member because they change money, orders, or customer communications.

Run history helps the team review answers, identify knowledge gaps, and decide on the next follow-up or learning suggestion. Reviewing a run never sends customer messages or updates knowledge or skills by itself.

## Enable and verify

1. On the **AI Agents** page, select **Test conversation** in the top-right corner, then choose the Agent to test.
2. Confirm that replies use the intended knowledge and tools.
3. Test unknown, sensitive, and handoff cases.
4. Bind at least one connected channel under **Reception channels**, then select **Enable Agent** from the disabled notice or **More Agent actions**.
5. Prefer the Web Widget for one real inbound and reply check.

An enabled Agent with no bound channel still does not serve customers and appears as a draft in the list. A saved configuration is not proof that the customer received a reply; verify the customer-visible message.

## Disable, archive, or delete

Role, knowledge scope, tools, and reception settings are configuration. Whether the Agent runs is a separate state. Saving configuration does not enable or disable the Agent.

To stop an Agent, open **More Agent actions** on the detail page, select **Disable Agent**, review the impact, and confirm. Assigned channels and configuration are retained, but the Agent no longer answers new messages or starts new proactive outreach. Conversations currently handled by AI return to the waiting queue, while human agents can continue handling them. The page shows **Agent disabled**; later, select **Enable Agent** from the notice or the same menu. Re-enabling applies only to new eligible work and does not automatically reclaim conversations that already moved to the waiting queue or a human agent.

Archive and delete are also under **More Agent actions**. Review how channels and active conversations will be handled before continuing. A workspace must retain at least one Agent, so the last Agent cannot be archived or deleted.

## Troubleshooting

- Cannot create: Refresh the Role list. If no Role is available, contact an administrator or YundaDesk support.
- No automatic reply: Confirm that the Agent is enabled and the connected channel is explicitly bound to it.
- Knowledge, tool, or skill is not applied: Review the relevant section, save, and run the test again.
- Channel cannot be selected: It may belong to another Agent. Review the transfer notice and confirm the intended target.
