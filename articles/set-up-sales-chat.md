---
title: Set up Sales agent in Microsoft 365 Copilot (preview)
description: Learn how to set up Sales agent, a conversational agent in Microsoft 365 Copilot Chat that helps sellers access and act on sales data from their CRM system.
ms.date: 02/11/2026
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Set up Sales agent in Microsoft 365 Copilot (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

The Sales agent is a conversational agent available within Microsoft 365 Copilot Chat. It enables sellers to efficiently search, synthesize, and take action on sales data from various applications they use. Sales agent is useful only when users are connected to a CRM system. Currently, it supports Dynamics 365 Sales and Salesforce.

The Sales agent is available to users who have access to a Microsoft 365 Copilot license. To see Sales agent, you must [install the Sales app](install-sales-app.md).

> [!NOTE]
> - If your team already uses Sales in Microsoft 365 Copilot, they'll see the Sales agent in the list of agents in Microsoft 365 Copilot Chat.
> - If all agents for Microsoft 365 Copilot Chat are disabled for your organization, users won't see Sales agent in the list of agents even if they have a Microsoft 365 Copilot license. Learn more about [managing agents for Microsoft 365 Copilot](/microsoft-365/admin/manage/manage-copilot-agents-integrated-apps?view=o365-worldwide#enable-or-disable-copilot-extensibility&preserve-view=true).

## Prerequisites

- [The Sales app is installed in both Outlook and Teams.](install-viva-sales.md)
- You have access to environment-level settings in the [administrator settings for Sales in Microsoft 365 Copilot](administrator-settings-sales-app.md).
- [Sales Chat must be turned on in Access settings.](access-settings.md#sales-agent-in-microsoft-365-copilot-preview)
- The Sales app must be connected to a CRM system.
- [Appropriate privileges must be assigned to admins and users in the CRM system to set up and access the data.](privileges.md) If you are a Salesforce admin, you must assign the security role in the msdyn_viva environment.

## Step 1: Configure CRM record types (tables)

As an administrator, you can customize which CRM information is available to sellers when they ask questions using the Sales agent. The Sales agent accesses CRM information based on the record types (tables) configured in Sales agent admin settings. 

By default, the Sales agent includes a predefined list of record types. You can customize this list by adding out-of-the-box or custom CRM record types. You can also remove record types that are not required.

> [!NOTE]
> - You can customize the list of record types in Sales agent settings independently without affecting Forms settings.
> - For Dynamics 365, if you've set up Sales agent before January 2026 and added record types in Forms settings, those record types will be available in Sales agent by default.

### Default record types

By default, Sales agent can access the following record types depending on your CRM system:

#### Dynamics 365

Sales agent accesses tables for which synonyms are added to Microsoft Copilot Studio associated with Copilot in Dynamics 365. If no synonyms are configured, Sales agent accesses the following default tables:
- Lead
- Product
- Opportunityproduct
- Opportunityclose
- Activitypointer
- Salesorder
- Invoice
- Goal
- Opportunity
- Account
- Contact
- QuoteClose
- Email
- Quote
- Competitor

#### Salesforce

Sales agent accesses the record types configured in [Forms settings](customize-forms-and-fields.md).

### Add new record types to Sales agent

1. [Open the Sales app administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Features**, select **Sales Chat**.
1. Select **Add**.
    :::image type="content" source="media/sales-chat-record-types.png" alt-text="Screenshot showing the Sales Chat record types settings.":::
1. In the **Add a record type** window, search and select the record types you want to add.
1. Select **Add**.

> [!NOTE]
> - You can add multiple record types at once.
> - Sales agent will have access to all columns in the added record types (tables).

### Remove record types from Sales agent

1. [Open the Sales app administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Features**, select **Sales Chat**.
1. Select the record types you want to remove, and then select **Remove**.
1. In the confirmation dialog box, select **Remove**.

> [!NOTE]
> - You can remove multiple record types at once.
> - You must have at least one record type configured for Sales agent to function.
> - When you remove a record, the Sales agent will no longer have access to it. If this record is configured in Forms settings, it will still be available in Forms and can be used in other features of the Sales app.

## Step 2: Set up additional synonyms and glossary terms

Sales reps can use natural language in Sales agent to access CRM information. However, the terms they use may not always match the standard field names in the CRM. Sales agent relies on CRM metadata about record types to interpret user requests and provide relevant information. Because this metadata is often incomplete, you can supply additional guidance—such as synonyms and glossary terms—to help the AI better understand and map user language to CRM data. Providing this extra information improves the AI’s ability to recognize user requests and generate accurate, helpful responses.

### Synonyms

Synonyms are alternative names or phrases that users might use to refer to specific CRM fields. For example, a user might refer to the "Account" field as "Company" or "Client." By adding these synonyms, you help Sales agent understand and respond to user queries more effectively.

#### Dynamics 365

1. Open [Copilot Studio](https://copilotstudio.microsoft.com) and select your Dynamics 365 Sales environment.
1. Select **Agents** > **Copilot in Dynamics 365 Sales**.
1. Select **SalesSpecificQnA** under **Knowledge** section.
1. Select the **Synonyms** section.
1. From the **Select item** list, select the CRM record type (table) for which you want to add synonyms.
1. Select **Add Synonyms** for the column (field) you want to add synonyms for, and then enter one or more synonyms, separated by commas.
1. In the **Description** field, provide a description for the synonym entry.
1. Select **Save**.

    :::image type="content" source="media/set-up-synonym-dynamics.png" alt-text="Screenshot of the set up Synonym option in Microsoft Copilot Studio.":::

> [!NOTE]
> The synonyms you add in Copilot Studio works for both the Sales agent and Copilot in Dynamics 365 Sales.

#### Salesforce

Synonyms are not supported for Salesforce CRM currently.

### Glossary terms

Glossary terms are specific terms or phrases that are relevant to your organization. These terms may not be commonly used outside your organization but are important for understanding your CRM data. By adding glossary terms, you help Sales agent recognize and interpret these terms correctly.

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

#### Dynamics 365

You must add glossary terms in Microsoft Copilot Studio. The glossary terms you add in Copilot Studio works for both the Sales agent and Copilot in Dynamics 365 Sales. Learn more about [adding glossary terms in Copilot Studio](/dynamics365/sales/extend-copilot-chat#add-glossary-to-help-copilot-understand-your-business-terms).

#### Salesforce

Glossary terms are not supported for Salesforce CRM currently.

## Step 3: Configure account summary

Sales reps can get a summary of their accounts in Sales agent. To enable this feature, you need to configure the account summary settings in the Sales app admin settings.

Generating the account summary involves two main components:

1. Getting information about the account

    Sales agent gathers all account-related information that is configured to be available to the Sales app through admin settings. This includes:

    - Columns from the **Account** record type (table) in CRM that are enabled for the Sales app.
    - Related record types (tables) in CRM that are enabled for the Sales app.
    
    Additionally, any meeting insights linked to the account from the past 30 days are included in the summary.

    To change the CRM information included in the account summary, update the CRM data available to the Sales app. Learn how to [configure record types in the Sales app](customize-forms-and-fields.md).
1. Curating the summary

    Sales agent uses natural language instructions to organize and present the account information in a summary that is meaningful and useful to users. Out-of-the-box instructions are provided, but you can customize them to better fit your organization's needs.

    To customize the AI instructions for the account summary:

    1. Go to the [Sales app admin settings](administrator-settings-for-viva-sales.md#access-administrator-settings).
    1. Under **Environment**, select **Custom AI instructions**.
    1. For the **Account summary** report, select **...** > **Edit**.

        :::image type="content" source="media/sales-chat-custom-ai.png" alt-text="Screenshot showing custom AI instructions for account summary.":::

    1. Select **Customized instructions** and then enter your custom instructions.
    1. Select **Save**.

        :::image type="content" source="media/sales-chat-custom-ai-edit.png" alt-text="Screenshot showing edited custom AI instructions for account summary.":::

        The new instructions will be applied the next time a user requests an account summary in Sales agent. You can test the instructions by requesting an account summary in Sales agent.

    > [!NOTE]
    > - You can't test the custom instructions before saving them. To validate your changes, connect to a test CRM environment before applying them in your production environment.
    > - The effectiveness of a custom instruction depends on the information included in the account summary. Whenever you update either the custom instructions or the summary content, review and adjust both to ensure they work well together.

## Step 4: Configure past customer meetings

Meeting insights generated by the Sales app are accessible in Sales agent. You can [manage access to meeting insights through the Sales app access settings](access-settings.md#meeting-insights). There are no separate settings for meeting insights specific to Sales agent.

## Step 5 (optional): Enable Microsoft 365 Copilot chat in model-driven apps

This step is applicable only if you're using Dynamics 365 as your CRM system. Enabling Microsoft 365 Copilot chat in model-driven apps allows users to access Sales agent directly within the Dynamics 365 apps. Learn how to [enable Microsoft 365 Copilot chat in model-driven apps](/power-apps/maker/model-driven-apps/add-microsoft-365-copilot).

## Related information

- [Use Sales agent in Microsoft 365 Copilot](use-sales-chat.md)
- [Turn on Sales agent](access-settings.md#sales-agent-in-microsoft-365-copilot-preview)
- [Privileges required to use Sales app](privileges.md)
