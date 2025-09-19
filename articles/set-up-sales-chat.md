---
title: Set up Sales Chat (preview)
description: 
ms.date: 08/13/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Set up Sales Chat (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Sales Chat is a conversational agent available within Microsoft 365 Copilot Chat. It enables sellers to efficiently search, synthesize, and take action on sales data from various applications they use. Sales Chat is useful only when users are connected to a CRM system. Currently, it supports Dynamics 365 Sales and Salesforce.

Sales Chat is available to users who have a Copilot for Sales license. If you don't have the license, you can install Copilot for Sales and use Sales Chat on a consumption basis.

> [!NOTE]
> - Users who don't have a Copilot for Sales license can't use Sales Chat until consumption-based billing is set up.
> - If your team already uses Copilot for Sales, they'll see the Sales Chat in the list of agents in Microsoft 365 Copilot Chat.
> - If all agents for Microsoft 365 Copilot Chat are disabled for your organization, users won't see Sales Chat in the list of agents even if they have a Copilot for Sales license. Learn more about [managing agents for Microsoft 365 Copilot](/microsoft-365/admin/manage/manage-copilot-agents-integrated-apps?view=o365-worldwide#enable-or-disable-copilot-extensibility).

## Prerequisites

- [The Copilot for Sales app is installed in either Outlook or Teams.](install-viva-sales.md)
- You have access to environment-level settings in the [Copilot for Sales admin settings](administrator-settings-for-viva-sales.md).
- [The Dataverse environment connected to Copilot for Sales is a production environment.](convert-trial-prod.md)
- Right licenses and [message capacity](manage-consumption-based-billing.md) have been set up.
- Sales Chat must be turned on in Access settings.
- Copilot for Sales must be connected to a CRM system.

## Step 1: Configure CRM record types (tables)

The CRM information that Sales Chat can access is determined by the record types (tables) added in the Copilot for Sales admin settings. Learn how to [configure record types in Copilot for Sales](customize-forms-and-fields.md).

## Step 2: Enable Sales Chat to use CRM as a knowledge source

After configuring the record types (tables), you must enable Sales Chat to use CRM as a knowledge source to provide relevant responses to user queries.

1. Go to the [Copilot for Sales admin settings](administrator-settings-for-viva-sales.md#access-administrator-settings).
1. Under **Features**, select **Sales Chat**.
1. In the status message, select **Set up**.

Setting up CRM knowledge for Sales Chat may take a few minutes. During this process, a banner will display the current setup status. If any errors occur, the banner will provide details about the issue and the actions you need to take.

> [!NOTE]
> - Before users can access CRM information through Sales Chat, CRM knowledge for Sales Chat must be set up at least once. This is required even if your organization has previously used Copilot for Sales and has already customized record types (tables).
> - Once CRM knowledge for Sales Chat has been set up, any changes you make to record types in the Copilot for Sales admin settings, such as adding or removing record types, will automatically update the CRM knowledge for Sales Chat.
> - It is recommended to monitor the status of CRM knowledge setup periodically to ensure that Sales Chat continues to function correctly.

## Step 3: Set up additional synonyms and glossary terms

Sales reps can use natural language in Sales Chat to access CRM information. However, the terms they use may not always match the standard field names in the CRM. Sales Chat relies on CRM metadata about record types to interpret user requests and provide relevant information. Because this metadata is often incomplete, you can supply additional guidance—such as synonyms and glossary terms—to help the AI better understand and map user language to CRM data. Providing this extra information improves the AI’s ability to recognize user requests and generate accurate, helpful responses.

### Synonyms

Synonyms are alternative names or phrases that users might use to refer to specific CRM fields. For example, a user might refer to the "Account" field as "Company" or "Client." By adding these synonyms, you help Sales Chat understand and respond to user queries more effectively.

To add a synonym:

1. [Create a custom model-driven app with PowerApps](/power-apps/maker/model-driven-apps/build-first-model-driven-app).
1. Add a new table named **CopilotSynonyms** with the following columns, and then publish the app.
   - Logical Name
   - Synonyms
   - Description
   - Skill Entity
1. Run the app, navigate to the **CopilotSynonyms** table and open the **Active CopilotSynonyms** view.
1. Select **New** to create a new synonym entry.
1. Fill in the fields as follows:
   - **Logical Name**: Enter the exact logical name of the CRM field you want to add synonyms for.
   - **Synonyms**: Enter one or more synonyms for the field, separated by commas.
   - **Description**: Provide a description of the synonym entry.
   - **Skill Entity**: If you're connected to Salesforce CRM, set the value to **SalesChatSalesforceQnA**. If you're connected to Dynamics 365 Sales, set the value to **SalesChatDVQnA**.

### Glossary terms

Glossary terms are specific terms or phrases that are relevant to your organization. These terms may not be commonly used outside your organization but are important for understanding your CRM data. By adding glossary terms, you help Sales Chat recognize and interpret these terms correctly.

The following table shows examples of how adding glossary definitions can give your agent valuable context and improve its responses.

| Scenario                | Glossary term        | Example description     |
|-------------------------|---------------------|----------------------|
| Acronym                 | VP                  | VP stands for Vice President and refers to the value in the **JobTitle** column of the **Contact** table.                                                     |
| Custom ownership        | activity owner      | The activity owner is determined by the **PartyId** column in the **ActivityParty** table.                                                                    |
| Custom field            | opportunity revenue | Opportunity revenue refers to the **Custom Revenue** column in the **Opportunity** table.                                                                     |
| Complex rules or filter | overdue task        | An overdue task is a record in the **Task** table where the **State code** column is set to open and the **Scheduled end date** column is earlier than today.    |

> [!NOTE]
> - The descriptions in the table are provided as examples. Test your own descriptions to see which ones produce the best results.
> - Updates to glossary terms and definitions may take up to 15 minutes to become available.

To add a glossary term:

1. [Create a custom model-driven app with PowerApps](/power-apps/maker/model-driven-apps/build-first-model-driven-app) or use the same app you created for adding synonyms.
1. Add a new table named **CopilotGlossaryTerms** with the following columns, and then publish the app.
   - Term
   - Description
   - Skill
1. Run the app, navigate to the **CopilotGlossaryTerms** table and open the **Active CopilotGlossaryTerms** view.
1. Select **New** to create a new glossary entry.
1. Fill in the fields as follows:
   - **Term**: Enter the specific term or phrase users might use in their prompts.
   - **Description**: Provide a clear description of the term.
   - **Skill**: If you're connected to Salesforce CRM, set the value to **SalesChatSalesforceQnA**. If you're connected to Dynamics 365 Sales, set the value to **SalesChatDVQnA**.

## Step 4: Configure account summary

Sales reps can get a summary of their accounts in Sales Chat. To enable this feature, you need to configure the account summary settings in the Copilot for Sales admin settings.

Generating the account summary involves two main components:

1. Getting information about the account

    Sales Chat gathers all account-related information that is configured to be available to Copilot for Sales through admin settings. This includes:

    - Columns from the **Account** record type (table) in CRM that are enabled for Copilot for Sales.
    - Related record types (tables) in CRM that are enabled for Copilot for Sales.
    
    Additionally, any meeting insights linked to the account from the past 30 days are included in the summary.

To change the CRM information included in the account summary, update the CRM data available to Copilot for Sales. Learn how to [configure record types in Copilot for Sales](customize-forms-and-fields.md).

1. Curating the summary

    Sales Chat uses natural language instructions to organize and present the account information in a summary that is meaningful and useful to users. Out-of-the-box instructions are provided, but you can customize them to better fit your organization's needs.

    To customize the AI instructions for the account summary:

    1. Go to the [Copilot for Sales admin settings](administrator-settings-for-viva-sales.md#access-administrator-settings).
    1. Under **Environment**, select **Custom AI instructions**.
    1. For the **Account summary** report name, select **Edit**.
    1. Select Customized instructions and then enter your custom instructions.
    1. Select **Save**.

        The new instructions will be applied the next time a user requests an account summary in Sales Chat. You can test the instructions by requesting an account summary in Sales Chat.

    > [!NOTE]
    > - You can't test the custom instructions before saving them. To validate your changes, connect to a test CRM environment before applying them in your production environment.
    > - The effectiveness of a custom instruction depends on the information included in the account summary. Whenever you update either the custom instructions or the summary content, review and adjust both to ensure they work well together.

## Step 5: Configure past customer meetings

Meeting insights generated by Copilot for Sales are accessible in Sales Chat. You can [manage access to meeting insights through the Copilot for Sales access settings](access-settings.md#meeting-insights). There are no separate settings for meeting insights specific to Sales Chat.