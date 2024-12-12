---
title: Connect to CRM from Teams
description: Connect to a CRM environment from Teams to get an enriched experience with CRM data.
ms.date: 12/12/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Connect to CRM from Teams

After you open the Microsoft 365 Copilot for Sales app in Teams, you must connect your CRM account to get an enriched experience with CRM data. You can either connect automatically or manually to your CRM environment.

Once you're connected to your CRM, the environment name is displayed at the top-right corner of the **Home** tab in the Copilot for Sales app. When you select the environment name, it shows the friendly name, type (Production/Sandbox), and URL for the environment. It also shows the following options:

- **Switch environments**: Select this option to switch to another Dynamics 365 environment. In the **Connected to Dynamics 365** dialog box, select another environment from the **Choose a Dynamics 365 environment** list, and then select **Switch environment**.
- **Switch to Salesforce CRM**: Select this option to connect to Salesforce CRM. Follow the steps shown in the wizard.
- **Disconnect**: Disconnect from the current environment. You can connect to another environment later.

:::image type="content" source="media/single-env-teams.png" alt-text="Screenshot showing connected to a single environment.":::

> [!NOTE]
> The option to switch environments is available only when connected to a Dynamics 365 environment and there are other Dynamics 365 environments available to connect to.

## Automatically connect to CRM

If you have a Dynamics 365 environment (production or non-production) with the Copilot for Sales solution, you're automatically connected to your environment the first time you open the Copilot for Sales app. The environment you're connected to is determined based on the following rules:


|Scenario  |Auto connect rule  |You see  |
|---------|---------|---------|
|Single environment (production or non-production)     |  Connected to the available environment       | Message in the **Home** tab of the Copilot for Sales app        |
|Single production environment and multiple non-production environments     |Connected to the production environment         |  Message in the **Home** tab of the Copilot for Sales app       |
|Multiple production and non-production environments     |  Connected to the first production environment       |  Dialog box to confirm or change the connected environment       |
|Multiple non-production environments but no production environment     |  Connected to the first non-production environment       |  Dialog box to confirm or change the connected environment       |

> [!NOTE]
> Copilot for Sales doesn't have access to data on your most frequently accessed or most recently accessed environment to automatically connect. Copilot for Sales fetches a list of environments that have the Copilot for Sales solution and then connects to the first environment in the list.

### Single environment or single production environment

For the first and second scenarios, a message is displayed at the top-right corner in the **Home** tab of the Copilot for Sales app. It shows the environment you are connected to automatically.

### Multiple environments

For the third and fourth scenarios, a dialog box is displayed to confirm the environment the user has been connected to or to select another environment. Select **OK** to confirm the environment or select another environment from the **Choose a Dynamics 365 environment** list. The list displays the friendly name for each environment.

:::image type="content" source="media/multiple-env-teams.png" alt-text="Screenshot showing environment confirmation when there are multiple environments.":::

## Manually connect to CRM

You must manually connect to your CRM in the following cases:

- If you're using Dynamics 365 environment and have disconnected your CRM from the Copilot for Sales app.
- If you're using Salesforce CRM.

You must be connected to your CRM to interact with CRM data in the Copilot for Sales app. Follow these steps to connect to your CRM:

1. Sign in to Teams.

1. On the left navigation pane, select **View more apps** (**...**), and then search and select **Copilot for Sales**. 

1. On the **Home** tab, select **Connect to CRM** in the upper-right corner, and then connect to your CRM using one of the following options:

    - **Dynamics 365**: You're connected automatically using your Office credentials. Select your Dynamics 365 environment, and then select **Connect to environment**.

        Your Dynamics 365 environment matches the URL your browser shows when you sign in to Dynamics 365. For example, if the URL is `salesorg.crm.dynamics.com`, select **salesorg.crm.dynamics.com** in the list.
    
    - **Salesforce® CRM**: Select your Salesforce environment, and then select **Connect to Salesforce® CRM**. In the confirmation message, select **Allow**. Enter your Salesforce credentials, and then select **Log In**. Select **Allow**, and then select **Allow access**.
    
    :::image type="content" source="media/manual-sign-in-teams.png" alt-text="Screenshot showing sign in button.":::


    Once you're connected, the Copilot for Sales pane is populated with personalized action items and relevant CRM information to help you work more efficiently.

## App refresh

When you switch the connected environment in Outlook, you receive a notification to refresh the Copilot for Sales app in Teams. Select **Refresh** to see the updated data from the new environment.
