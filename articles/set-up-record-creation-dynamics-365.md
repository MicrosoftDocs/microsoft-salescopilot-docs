---
title: Set up record creation in Dynamics 365 with Sales agent (preview)
description: Dynamics 365 integration made easy—discover how to set up record creation with Sales agent in Microsoft 365 Copilot and boost your productivity.
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.date: 04/14/2026
---

# Set up record creation in Dynamics 365 with Sales agent (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Sellers can create contacts, accounts, opportunities, and other record types in Dynamics 365 directly from the Sales agent in Microsoft 365 Copilot. When a seller asks the Sales agent to create a record, an interactive form appears inline in the chat. The seller can then review and edit the details before submitting the form to create the record in Dynamics 365.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

## Prerequisites

Before setting up record creation in the Sales agent, make sure the following prerequisites are met:

- **Model-driven Dynamics 365 app**: You have Sales Hub or another Dynamics 365 model-driven app that includes the tables you want users to create records in.
- **Permission to upload custom apps in Microsoft 365 admin center**: Your Microsoft 365 AI admin has enabled this permission.
- **Dynamics 365 administrator roles**: You need the System Administrator or System Customizer security role in Dynamics 365, and the AI Administrator role to manage the Sales agent in Microsoft 365 admin center or Agent 365.

## Set up record creation in the Sales agent

To enable record creation in the Sales agent, download your model-driven app package from Power Apps, upload it as a custom agent in Microsoft 365 admin center, and then copy its tools and knowledge to the Sales agent. After setup, test the experience to confirm users can create records from Microsoft 365 Copilot.

### Step 1: Download the app package from Power Apps

1. Sign in to [Power Apps](https://make.powerapps.com) and open the model-driven app in the app designer.
1. On the command bar, select **Settings**.
1. Select the **Upcoming** tab.
1. Under **Enable your app in Microsoft 365 Copilot**, select **Download app package**.
    A compressed file named similar to `declarative-agent-<app name>.zip` is downloaded to your computer.

> [!NOTE]
> The **Upcoming** tab displays preview features. If you don't see the **Enable your app in Microsoft 365 Copilot** option, verify that preview features are available in your environment.

### Step 2: Upload the app package in Microsoft 365 admin center

After you download the package, [upload it as a custom agent using Microsoft 365 admin center](/microsoft-365/copilot/agent-essentials/agent-lifecycle/agent-upload-agents).

> [!NOTE]
> You don't need to deploy the agent. You only need to upload it and make it available in your organization's agent catalog.

### Step 3: Add the custom tools and knowledge to the Sales agent

Use the instructions in [Extend Sales agent with custom tools and knowledge in the Microsoft 365 admin center](extend-sales-chat-custom-tools.md) to copy the tools and knowledge from the custom agent you uploaded to the Sales agent.

### Step 4: Test the record creation experience

After you add the tools and knowledge from the custom agent to the Sales agent, test the record creation experience by asking the Sales agent to create a record.

1. Open Microsoft 365 Copilot and select the Sales agent.
1. Ask the Sales agent to create a record, such as:
    1. Create an opportunity for Contoso.
    1. Log a new sales opportunity for the Fabrikam license renewal.
    1. Create an opportunity worth $50,000, closing next quarter, for Northwind Traders.
1. The Sales agent displays an inline form that includes fields from your Dynamics 365 record's quick create form. Some fields might be prepopulated from the context in your prompt.
1. Review and update the fields as needed.
1. Select **Create** to save the opportunity in Dynamics 365.

After the record is created, the Sales agent displays a confirmation message with the record name.

> [!NOTE]
> - Data access and record creation follow your Dynamics 365 security roles and field-level security. If you don’t have permission to create a record, the Sales agent shows an error.
> - The form shows fields from the first tab of the default main form configured for the table in your model-driven app. To change the fields that appear, [customize the quick create form in Power Apps](/power-apps/maker/model-driven-apps/create-edit-quick-create-forms).

## Related information

- [Add interactive UI widgets to declarative agents](/microsoft-365/copilot/extensibility/declarative-agent-ui-widgets)
- [Manage model-driven app settings in the app designer](/power-apps/maker/model-driven-apps/app-properties#set-up-power-apps-in-copilot)
- [Extend Sales agent with custom tools and knowledge in Microsoft 365 admin center](extend-sales-chat-custom-tools.md)
- [Create or edit model-driven app quick create forms](/power-apps/maker/model-driven-apps/create-edit-quick-create-forms).