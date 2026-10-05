---
title: Enable business skills in Dataverse for Sales agent (preview)
description: Learn how to enable business skills in Dataverse, make them available to Sales agent, and verify the connection.
ms.date: 10/05/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# Enable business skills in Dataverse for Sales agent (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[Business skills](/power-apps/maker/data-platform/data-platform-business-skill-overview) are natural-language instructions that help agents follow your organization's processes, policies, and domain knowledge to complete specific tasks. Each skill defines the required steps, information, and business rules. After you enable the required Dataverse features, Sales agent can discover and use these skills with your Dynamics 365 data through the Dataverse Model Context Protocol (MCP) server.

This article explains how to enable the required features, create a business skill, connect Sales agent, and verify the setup.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

## Prerequisites

Before you begin, make sure that:

- Administrators and skill authors have the **System Administrator**, **System Customizer**, **Environment Maker**, or **Power Platform Administrator** [permissions](/power-apps/maker/data-platform/data-platform-business-skill-overview) for the Dynamics 365 environment in Power Platform.
- Each user who needs to use business skills has at least the **Basic User** security role in the Dynamics 365 environment in Power Platform. Without this role, users can't see the organization-level business skills.
- The environment has an appropriate license for Dynamics 365 Sales and Dataverse.
- Skill authors have access to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
- Users who access Sales agent have the required Microsoft 365 Copilot and Dynamics 365 Sales licenses.

## Enable business skills in Dataverse

Enable the required features in the environment where you want Sales agent to use business skills.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. Go to **Manage** > **Environments**, and then select the environment.
1. On the command bar, select **Settings**.
1. Expand **Product**, and then select **Features**.

	:::image type="content" source="media/biz-skill-feature.png" alt-text="Screenshot of the environment Settings page with Product expanded and Features highlighted.":::

1. In the **Dataverse intelligence** section, select **Turn on Dataverse intelligence for agents and AI experiences**. This action enables business skills for the environment and allows agents to use them.
1. In the **Dataverse search** section, ensure that **Show global search bar in all model-driven apps** and search indexing are selected. This action ensures skills and data are discoverable by agents. 
1. In the **Dataverse Model Context Protocol** section, select **Allow MCP clients to interact with Dataverse MCP server (GA version)**.

	:::image type="content" source="media/biz-skill-features-page.png" alt-text="Screenshot of the Features page showing the Dataverse intelligence, Dataverse search, and Dataverse Model Context Protocol settings.":::

1. In the **Dataverse Model Context Protocol** section, select **Go to Advanced Settings**.
1. In the **Active Allowed MCP Clients** list, find **Enterprise Copilot Platform** and verify that **Is Enabled** is set to **Yes**. Its unique name is `enterprisecopilotplatform`. Sales agent uses this client to access the Dataverse MCP server. 

	:::image type="content" source="media/biz-skill-mcp-allow.png" alt-text="Screenshot of the Active Allowed MCP Clients list showing Enterprise Copilot Platform enabled.":::

1. If the client isn't enabled, open **Enterprise Copilot Platform**, set **Is Enabled** to **Yes**, and then select **Save & Close**.

	:::image type="content" source="media/biz-skill-mcp-enable.png" alt-text="Screenshot of the Enterprise Copilot Platform client record with Is Enabled set to Yes.":::

For more information about controlling access to the Dataverse MCP server, see [Allow or disable MCP clients](/power-apps/maker/data-platform/data-platform-mcp-disable).

## Create a business skill

Create a simple business skill to test the connection before you create skills for your business scenarios.

1. Follow the steps in [Manage business skills](/power-apps/maker/data-platform/data-platform-business-skills#manage-business-skills) to create a skill.
1. Create a basic read or query skill that Sales agent can use for testing.
1. Give the skill a specific name and description. This information helps the agent determine when to use the skill.

## Connect Sales agent and verify the setup

1. Open [Sales agent](https://m365.cloud.microsoft/agents/saleschat).
1. Select **Sources**.
1. Verify that Sales agent is connected to the same Dynamics 365 organization in which you enabled business skills. If it isn't, select **Switch sources**, and then connect to the correct organization.

	:::image type="content" source="media/biz-skill-sources.png" alt-text="Screenshot of Sources in Sales agent showing the connected Dynamics 365 organization.":::

1. Ask Sales agent, **What business skills do I have?**

Sales agent should list the skill that you created. If the created skill appears, the connection is ready to use. Once you verify that the connection is working, create business skills for your business scenarios. Examples could be reviewing your pipeline, creating an opportunity playbook, or writing an account brief. To get started, see [example business skills](https://aka.ms/DVBusinessSkillRepo).

## Disable business skills or MCP access

In the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), open the Dynamics 365 environment, and then choose an option based on the access you want to remove.

|Scope|Action|
|---|---|
|Disable Dataverse intelligence for the environment|On the environment's **Features** page, clear **Turn on Dataverse intelligence for agents and AI experiences**. This change prevents agents from using Dataverse business skills in the environment.|
|Block MCP access for Sales agent|In **Advanced Settings** > **Allowed MCP Clients**, open **Enterprise Copilot Platform**, set **Is Enabled** to **No**, and then select **Save & Close**. You can also remove the client from the allow list.|
|Block all MCP clients|On the environment's **Features** page, clear **Allow MCP clients to interact with Dataverse MCP server (GA version)**.|
|Remove one skill|Deactivate or delete the business skill. For instructions, see [Manage business skills](/power-apps/maker/data-platform/data-platform-business-skills#manage-business-skills).|

> [!NOTE]
> Changes apply to new agent interactions. Users might need to refresh an existing session. To restore access, turn the corresponding setting back on.

## Related information

- [Dataverse intelligence](/power-apps/maker/data-platform/data-platform-intelligence)
- [Business skills in Microsoft Dataverse](/power-apps/maker/data-platform/data-platform-business-skills)
- [Allow or disable MCP clients](/power-apps/maker/data-platform/data-platform-mcp-disable)
- [Manage business skills](/power-apps/maker/data-platform/data-platform-business-skills#manage-business-skills)
