---
title: Enable business skills for Salesforce in the Sales agent (preview)
description: Learn how to enable business skills for Salesforce in the Sales agent, make them available to Salesforce users, and verify the connection.
ms.date: 10/05/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# Enable business skills for Salesforce in the Sales agent (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[Business skills](/power-apps/maker/data-platform/data-platform-business-skill-overview) are natural-language instructions that help agents follow your organization's processes, policies, and domain knowledge to complete specific tasks. Each skill defines the required steps, information, and business rules. When Sales agent is connected to Salesforce, Microsoft provisions a Dataverse environment named `msdyn_viva` for the tenant. Create and manage the business skills for your Salesforce organizations in this environment.

This article explains how to enable business skills in `msdyn_viva`, give Salesforce users access, add the required Salesforce metadata to each skill, and verify the setup in Sales agent.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

## About the msdyn_viva environment

The `msdyn_viva` environment has the following characteristics:

- Microsoft provisions it when the first user signs in to Salesforce through Sales agent.
- It stores business skills and their configuration for all Salesforce organizations connected from the tenant. For other Sales agent features, it stores generated insights and related metadata.

> [!IMPORTANT]
> Don't delete or modify the `msdyn_viva` environment. Doing so might prevent Sales agent from working. For more information, see [Data handling in Sales agent](data-handling.md).

## Prerequisites

Before you begin, make sure that:

- Sales agent is deployed for Salesforce, and users meet the requirements in [Deploy Sales agent for Salesforce](deploy-sales-app-sf.md).
- [At least one user has signed in to Salesforce from Sales agent](deploy-sales-app-sf.md#step-7-first-user-sign-in). This sign-in creates the `msdyn_viva` environment, which stores Sales agent generated insights, metadata, and business skill configuration.
- Administrators and skill authors have the required permissions in `msdyn_viva`. Power Platform administrators and Microsoft 365 global administrators are automatically assigned the System Administrator security role in this environment. Review this list to ensure appropriate access.
- Each user who needs to use business skills has at least the **Basic User** security role in `msdyn_viva`. Without this role, users can't see the organization-level business skills.
- Users have the required Microsoft 365 Copilot licenses and are signed in to Salesforce.

## Enable business skills in msdyn_viva

Enable Dataverse intelligence and MCP access in the `msdyn_viva` environment.

> [!NOTE]
> Some screenshots in this procedure show an example environment. Complete all steps in the `msdyn_viva` environment.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. Go to **Manage** > **Environments**, and then select `msdyn_viva`.
1. On the command bar, select **Settings**.
1. Expand **Product**, and then select **Features**.

	:::image type="content" source="media/biz-skill-feature.png" alt-text="Screenshot of the environment Settings page with Product expanded and Features highlighted.":::

1. In the **Dataverse intelligence** section, select **Turn on Dataverse intelligence for agents and AI experiences**. This action enables business skills for the environment and allows agents to use them.
1. In the **Dataverse search** section, ensure that **Show global search bar in all model-driven apps** and search indexing are selected. This action ensures skills and data are discoverable by agents. 
1. In the **Dataverse Model Context Protocol** section, select **Allow MCP clients to interact with Dataverse MCP server (GA version)**.

	:::image type="content" source="media/biz-skill-features-page.png" alt-text="Screenshot of the Features page showing the Dataverse intelligence, Dataverse search, and Dataverse Model Context Protocol settings.":::

1. In the **Dataverse Model Context Protocol** section, select **Go to Advanced Settings**.
1. In the **Active Allowed MCP Clients** list, find **Enterprise Copilot Platform** and verify that **Is Enabled** is set to **Yes**. Sales agent uses this client to access the Dataverse MCP server.

	:::image type="content" source="media/biz-skill-mcp-allow.png" alt-text="Screenshot of the Active Allowed MCP Clients list showing Enterprise Copilot Platform enabled.":::

1. If the client isn't enabled, open **Enterprise Copilot Platform**, set **Is Enabled** to **Yes**, and then select **Save & Close**.

	:::image type="content" source="media/biz-skill-mcp-enable.png" alt-text="Screenshot of the Enterprise Copilot Platform client record with Is Enabled set to Yes.":::

For more information about MCP client access, see [Allow or disable MCP clients](/power-apps/maker/data-platform/data-platform-mcp-disable).

## Give Salesforce users access to business skills in msdyn_viva environment

Assign a security role to every Salesforce user who needs to use business skills.

1. In the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), open the `msdyn_viva` environment.
1. Go to **Settings** > **Users + permissions** > **Users**.
1. Add the user if they aren't already listed.
1. Assign the **Basic User** security role or a role with equivalent privileges.
1. Repeat these steps for each user who needs access to business skills.

## Create a business skill for Salesforce

Create a simple business skill to test the connection before you create skills for your business scenarios. Create each Salesforce business skill in `msdyn_viva` and include the metadata that identifies its target Salesforce organization.

1. Go to [Power Apps](https://make.powerapps.com/).
1. In the environment selector, select `msdyn_viva`.
1. Follow the steps in [Manage business skills](/power-apps/maker/data-platform/data-platform-business-skills#manage-business-skills) to create a skill.
1. Create a basic read or query skill that Sales agent can use for testing.
1. Give the skill a specific name and description. This information helps the agent determine when to use the skill.
1. Select **Add metadata**, and then add both of the following tags:

	|Label|Value|
	|---|---|
	|`metadata.crm`|`salesforce`|
	|`metadata.orgUrl`|The exact Salesforce organization URL displayed under **Sources** in Sales agent. For example, `https://fourthcoffee-dev-ed.develop.my.salesforce.com`.|

    To find the organization URL, open Sales agent, select **Sources**, and copy the URL under **Connected to Salesforce**.

    :::image type="content" source="media/biz-skills-sf-source.png" alt-text="Screenshot of Sources in Sales agent showing the connected Salesforce organization URL.":::

    > [!IMPORTANT]
    > Both metadata tags are required. The value of `metadata.orgUrl` must exactly match the Salesforce URL under **Sources** in Sales agent. Sales agent doesn't consider a skill if its metadata is missing or doesn't match the connected organization.

1. Save or update the metadata.

	:::image type="content" source="media/biz-skill-sf-metadata.png" alt-text="Screenshot of a business skill in the msdyn_viva environment with the required Salesforce metadata tags.":::

## Verify the setup in Sales agent

1. Open [Sales agent](https://m365.cloud.microsoft/agents/saleschat).
1. Select **Sources** and confirm that Sales agent is connected to the intended Salesforce organization.
1. Verify that the connected organization URL exactly matches the skill's `metadata.orgUrl` value.
1. Ask Sales agent, **What business skills do you have?**

Sales agent should list the skills created for the connected Salesforce organization. If the created skill appears, the connection is ready to use. After you verify that the connection works, create business skills for your business scenarios. Examples could be reviewing your pipeline, creating an opportunity playbook, or writing an account brief. To get started, see [example business skills](https://aka.ms/DVBusinessSkillRepo).

:::image type="content" source="media/biz-skills-sf-verify.png" alt-text="Screenshot of Sales agent listing the business skills available for the connected Salesforce organization.":::

## Configure skills for multiple Salesforce organizations

All Salesforce organizations connected from the same tenant share the business skill store in `msdyn_viva`. You configure each skill to work with one Salesforce organization at a time. When the skill runs, it accesses data or performs actions only in that organization. You can configure multiple skills to work with the same organization.

To use the same skill in a development or sandbox organization and a production organization, create a separate skill for each organization. As a best practice, don't change the `metadata.orgUrl` value of the development skill when you're ready to use it in production. Instead, create a new skill with a unique name, copy the contents of the development skill, and configure the new skill for the production organization.

For each skill:

- Set `metadata.orgUrl` to the URL of the organization that should use the skill.
- Set `metadata.crm` to `salesforce`.
- Give the skill a unique name across all connected organizations. Consider adding an organization-specific suffix.

For example, you can create two versions of a next-best-action skill:

|Skill unique name|metadata.orgUrl|Configured organization|
|---|---|---|
|next-best-action-prod|https://yourco.my.salesforce.com|Production organization|
|next-best-action-dev|https://yourco-dev-ed.develop.my.salesforce.com|Development or sandbox organization|

Each version is configured for one organization. Sales agent considers only the version whose `metadata.orgUrl` value matches the currently connected Salesforce organization.

## Manage or disable business skills

In the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), open the `msdyn_viva` environment, and then choose an option based on the access you want to remove.

|Scope|Action|
|---|---|
|Disable Dataverse intelligence for the environment|On the environment's **Features** page, clear **Turn on Dataverse intelligence for agents and AI experiences**. This change prevents agents from using Dataverse business skills in the environment.|
|Block MCP access for Sales agent|In **Advanced Settings** > **Allowed MCP Clients**, open **Enterprise Copilot Platform**, set **Is Enabled** to **No**, and then select **Save & Close**. You can also remove the client from the allow list.|
|Block all MCP clients|On the environment's **Features** page, clear **Allow MCP clients to interact with Dataverse MCP server (GA version)**.|
|Remove one skill|Deactivate or delete the business skill. For instructions, see [Manage business skills](/power-apps/maker/data-platform/data-platform-business-skills#manage-business-skills).|

> [!IMPORTANT]
> Don't delete or modify the `msdyn_viva` environment to disable business skills. Deactivate or delete individual skills, or turn off the applicable feature setting.

## Related information

- [Data handling in Sales agent](data-handling.md)
- [Deploy Sales agent for Salesforce](deploy-sales-app-sf.md)
- [Business skills in Microsoft Dataverse](/power-apps/maker/data-platform/data-platform-business-skills)
- [Dataverse intelligence](/power-apps/maker/data-platform/data-platform-intelligence)
- [Allow or disable MCP clients](/power-apps/maker/data-platform/data-platform-mcp-disable)
