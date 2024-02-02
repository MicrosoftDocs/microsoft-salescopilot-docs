---
title: Connect your CRM account for an enriched experience
description: Sign in to CRM from Outlook and connect your CRM account to get a more enriched experience with CRM data.
ms.date: 02/02/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-title
  - ai-seo-date:02/01/2024
  - ai-gen-desc
---

# Sign in to CRM from Outlook

After you open Copilot for Sales, you can sign in to Copilot for Sales and connect your CRM account to get a more enriched experience with CRM data.

## Automatically sign in

If you have any Dynamics 365 environment (production or non-production) that has the Copilot for Sales solution, you're signed in automatically to your environment the first time you open the Copilot for Sales pane. The environment you're signed in to is selected per the following rules:


|Scenario  |Auto sign-in rule  |You'll see  |
|---------|---------|---------|
|Single environment (production or non-production)     |  Signed in to the available environment       | Message at the top of Copilot for Sales pane        |
|Single production environment and multiple non-production environments     |Signed in to the production environment         |  Message at the top of Copilot for Sales pane       |
|Multiple production and non-production environments     |  Signed in to the first production environment       |  Dialog box to confirm or change the signed in environment       |
|Multiple non-production environments but no production environment     |  Signed in to the first non-production environment       |  Dialog box to confirm or change the signed in environment       |

> [!NOTE]
> Copilot for Sales does not have access to data on your most frequently accessed or most recently accessed environment to automatically sign in. Copilot for Sales fetches a list of environments having the Copilot for Sales solution, and then selects the first environment in the list to automatically sign in to.

### Single environment or single production environment

For first and second scenarios, a message is displayed at the top of the Copilot for Sales pane showing the environment the user was signed in to automatically. It includes a link to change the environment or CRM.

:::image type="content" source="media/single-env.png" alt-text="Screenshot showing signed in to a single environment.":::

To change the environment or CRM, select **Switch environment**. In the **Signed in to Dynamics 365** dialog box, select another environment from the **Environment** list, and then select **OK**. The **Environment** list displays the friendly name, type (Production/Sandbox), and URL for each environment.

:::image type="content" source="media/single-env-switch.png" alt-text="Screenshot showing environment switcher for a when signed in to a single environment.":::

To sign in to Salesforce CRM, select **Sign in to Salesforce® CRM** and then follow the steps shown in the wizard.

### Multiple environments

For third and fourth scenarios, a dialog box is displayed to confirm the environment the user has been signed in to, or to select another environment. Select **OK** to confirm the environment or select another environment from the **Environment** list. 

:::image type="content" source="media/multiple-env-switch.png" alt-text="Screenshot showing environment confirmation a when there are multiple environments.":::

To sign in to Salesforce CRM, select **Sign in to Salesforce® CRM** and then follow the steps shown in the wizard.

The **Environment** list displays the friendly name, type (Production/Sandbox), and URL for each environment.

:::image type="content" source="media/env-list.png" alt-text="Screenshot showing the environment list.":::

## Manually sign in

You must manually sign in to your CRM in the following cases:

- If you're using Dynamics 365 environment and have signed out of your CRM from Copilot for Sales

- If you're using Salesforce CRM

You can use basic capabilities of Copilot for Sales without signing in to your CRM. However, to use all the advanced capabilities of Copilot for Sales, you must sign in to your CRM.

1. In the **Copilot for Sales** pane, select **Sign in** in the banner at the top or card at the bottom.

    :::image type="content" source="media/manual-sign-in.png" alt-text="Screenshot showing sign in button.":::

2. Select **Sign in to your CRM** and sign in to your CRM using one of the following options:

    - **Salesforce CRM**: Select your Salesforce environment, and then select **Sign in**. In the confirmation message, select **Allow**. Enter your Salesforce credentials, and then select **Log In**. Select **Allow**, and then select **Allow access**.
    
    - **Dynamics 365**: You’re signed in automatically using your Office credentials. Select your Dynamics 365 environment, and then select **Get started**.

        Your Dynamics 365 environment matches the URL your browser shows when you sign in to Dynamics 365. For example, if the URL is `salesorg.crm.dynamics.com`, select **salesorg.crm.dynamics.com** in the list.
        
        :::image type="content" source="media/sign-in-crm.png" alt-text="Screenshot showing sign in to your CRM button.":::

    Once you're signed in, the Copilot for Sales pane is populated with personalized action items and relevant CRM information to help you work more efficiently.

## Use Copilot for Sales without signing in

You can use Copilot for Sales and AI capabilities in Outlook without signing in to your CRM. You can use basic capabilities like [email drafting](use-copilot-kickstart-email-messages.md#create-an-email-reply-using-pre-defined-categories) and [email summarization](view-save-email-summary-crm.md) without signing in to your CRM. For a more enriched experience with CRM data, you must sign in to your Dynamics 365 or Salesforce CRM account. [Open Copilot for Sales](#open-copilot-for-sales) to get started.

> [!NOTE]
> This feature is available only for customers in United States and Europe.