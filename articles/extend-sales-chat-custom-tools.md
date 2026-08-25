---
title: Extend Sales agent with custom tools and knowledge in the Microsoft 365 admin center
description: Extend your Microsoft Sales agent with custom tools and knowledge to integrate data, enhance insights, and provide accurate responses. Learn how to get started.
ms.date: 08/25/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# Extend Sales agent with custom tools and knowledge in the Microsoft 365 admin center 

You can extend the Sales agent with custom tools and knowledge from a custom declarative agent. Declarative agents are specialized agents that combine tools and knowledge sources to support specific business scenarios, such as account research, renewal planning, and order management.

In this extensibility model, the custom declarative agent serves as the source of the tools and knowledge added to Sales agent. This setup enables users to access your organization's sales data, perform business actions, and receive grounded responses directly in the Sales agent.

## How do declarative agents extend Sales agent?

A declarative agent provides the custom tools and knowledge that extend Sales agent for your organization's specific scenarios.

Tools enable users to interact with sales applications using natural language. Depending on the configured [API plugin](/microsoft-365-copilot/extensibility/overview-api-plugins) or MCP server, users can:

- Retrieve data and insights from sales applications.
- Create, update, and delete records.
- Perform supported business actions.

[Knowledge sources](/microsoft-365-copilot/extensibility/knowledge-sources) ground responses in your organization's content, such as SharePoint sites, websites, documentation, and policies. This content helps Sales agent provide more accurate and contextual answers.

### Key details

**Limitations**
- You can copy tools and knowledge from only one declarative agent (either built by your organization or from the store).
- The combined size of all copied custom tools and knowledge cannot exceed 150 KB.

**Built-in content**
- Administrators can't remove the out-of-the-box tools and knowledge in Sales agent.

**Access requirements**
- Ensure all users have the necessary permissions to access the tools and knowledge added to Sales agent.

> [!NOTE]
> Custom tools and knowledge are added to Sales agent as a snapshot of the selected source-agent version. Publishing a new version of the source agent doesn't automatically update the extension in Sales agent. You must [update to the new source version](#update-custom-tools-and-knowledge) in the Microsoft 365 admin center. After you publish or update the extension, the changes can take up to 24 hours to become available.

## Build a custom declarative agent for Sales agent

You can build a custom [declarative agent](/microsoft-365-copilot/extensibility/overview-declarative-agent) around specific sales scenarios, such as account research, renewal planning, or order status. Add the required [API plugins](/microsoft-365-copilot/extensibility/overview-api-plugins) for business actions, and attach relevant [knowledge sources](/microsoft-365-copilot/extensibility/knowledge-sources) for grounding. After validating responses and access permissions for the target users, publish the agent, and then copy its tools and knowledge into Sales agent from the **Custom tools & knowledge** tab.

To learn how to create a declarative agent with Microsoft 365 Agents Toolkit, see [Create declarative agents using Microsoft 365 Agents Toolkit](/microsoft-365/copilot/extensibility/build-declarative-agents). You can enhance the agent with MCP endpoints by [building a plugin from an MCP server](/microsoft-365/copilot/extensibility/build-mcp-plugins). To add citations to responses from custom tools, see [Configure citations and source links](#configure-citations-and-source-links).

## Configure citations and source links

When you extend Sales agent with custom MCP or OpenAPI tools, structure the tool responses so that Copilot can display citations with clickable source links. Configure `response_semantics` in the plugin manifest to identify the citable items in the response and map each item's source title and URL. Citation behavior depends on the response structure and these field mappings. For configuration details and examples, see [Show citations with response semantics](/microsoft-365/copilot/extensibility/plugin-citations).

## Extend Sales agent with custom tools and knowledge

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Agents** > **All agents**.
1. Select **Sales** and then go to the **Custom tools & knowledge** tab.
   :::image type="content" source="media/custom-tools-and-knowledge-tab.png" alt-text="Screenshot of the Custom tools & knowledge tab.":::
1. Select **Choose agent**.
1. In the **Extend Sales** pane:
    1. Find the agents using the search box.
    1. Select the agent you want to copy tools and knowledge from.
    > [!NOTE]
    > All tools and knowledge from the selected agent are copied to the Sales agent.

    :::image type="content" source="media/extend-sales-panel.png" alt-text="Screenshot of the Extend Sales panel.":::
1. Select **Next**.
1. In the **Assign Users** pane, select the users or security groups who should have access to the custom tools and knowledge in the Sales agent.
1. Select **Save**.

## Update custom tools and knowledge

Custom tools and knowledge are copied from a specific version of the source agent and don't update automatically when a newer version is published. When an update is available, use **Update from store** to replace the current copy with the latest source-agent version. The update preserves the users and security groups assigned to the extension. For availability conditions, limitations, and detailed steps, see [Update custom tools and knowledge in Sales agent](update-sales-chat-custom-tools.md).

## Remove custom tools and knowledge

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Agents** > **All agents**.
1. Select **Sales** and then go to the **Custom tools & knowledge** tab.
1. Select **Remove agent extension**.
1. In the **Remove agent extension** pane, select **Remove** to confirm.

## Related information

- [Declarative agents for Microsoft 365 Copilot](/microsoft-365-copilot/extensibility/overview-declarative-agent)
- [Choose the right tool to build your declarative agent](/microsoft-365-copilot/extensibility/declarative-agent-tool-comparison)
- [Add knowledge sources to your declarative agent](/microsoft-365-copilot/extensibility/knowledge-sources)
- [Plugins for Microsoft 365 Copilot](/microsoft-365-copilot/extensibility/overview-plugins?tabs=mcp)
- [Use developer mode in Microsoft 365 Copilot to test and debug agents](/microsoft-365-copilot/extensibility/debugging-agents-copilot-studio)
- [Set up record creation in Dynamics 365 with Sales agent](set-up-record-creation-dynamics-365.md)
- [Manage connected agents in the Microsoft 365 admin center](manage-connected-agents.md)