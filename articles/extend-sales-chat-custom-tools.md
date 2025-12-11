---
title: Extend Sales agent with custom tools and knowledge in the Microsoft 365 admin center
description: Extend your Microsoft Sales agent with custom tools and knowledge to integrate data, enhance insights, and provide accurate responses. Learn how to get started.
ms.date: 12/08/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Extend Sales agent with custom tools and knowledge in the Microsoft 365 admin center 

The **Custom tools & knowledge** tab enables you to copy tools and knowledge from other agents in your organization to Sales. This extends the capabilities of Sales by integrating data and insights from your organization's sales applications, providing users with more comprehensive information and answers during their interactions.

## What are custom tools and knowledge?

Tools are [API plugins](/microsoft-365-copilot/extensibility/overview-api-plugins) that can be added to declarative agents. They enable users to interact with your organization's sales applications using natural language in Sales.

With custom tools, users can:
- Retrieve data and insights from any sales application
- Create, update, and delete data and objects
- Execute any action available through the application's REST API or MCP server

[Knowledge sources](/microsoft-365-copilot/extensibility/knowledge-sources) provide additional grounding information for the agent. When you configure SharePoint sites, websites, or other supported content as knowledge sources, Sales searches that content to generate more accurate and contextual responses.

This ensures Sales can reference your organization's specific documentation, policies, and information when answering user questions.

### Key details

**Limitations**
- You can copy tools and knowledge from only one declarative agent (either built by your organization or from the store).
- The combined size of all copied custom tools and knowledge cannot exceed 150 KB.

**Built-in content**
- Out-of-the-box tools and knowledge in Sales cannot be removed by administrators.

**Access requirements**
- Ensure all users have the necessary permissions to access the tools and knowledge added to Sales.

## Extend Sales with custom tools and knowledge

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Agents** > **All agents**.
1. Select **Sales** and then go to the **Custom tools & knowledge** tab.
   :::image type="content" source="media/custom-tools-and-knowledge-tab.png" alt-text="Screenshot of the Custom tools & knowledge tab.":::
1. Select **Choose agent**.
1. In the **Extend Sales** pane:
    1. Find the agents using the search box.
    1. Select the agent you want to copy tools and knowledge from.
    > [!NOTE]
    > All tools and knowledge from the selected agent are copied to Sales.
    :::image type="content" source="media/extend-sales-panel.png" alt-text="Screenshot of the Extend Sales panel.":::
1. Select **Next**.
1. In the **Assign Users** pane, select the users or security groups who should have access to the custom tools and knowledge in Sales.
1. Select **Save**.

## Remove custom tools and knowledge

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Agents** > **All agents**.
1. Select **Sales** and then go to the **Custom tools & knowledge** tab.
1. Select **Remove agent extension**.
1. In the **Remove agent extension** pane, select **Remove** to confirm.
