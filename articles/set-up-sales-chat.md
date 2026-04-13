---
title: Set up Sales agent in Microsoft 365 Copilot (preview)
description: Learn how to set up Sales agent, a conversational agent in Microsoft 365 Copilot that helps sellers access and act on sales data from their CRM system.
ms.date: 04/14/2026
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Set up Sales agent in Microsoft 365 Copilot (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

The Sales agent is a conversational agent available within Microsoft 365 Copilot. It enables sellers to efficiently search, synthesize, and take action on sales data from various applications they use. Sales agent is useful only when users are connected to a CRM system. Currently, it supports Dynamics 365 Sales and Salesforce.

The Sales agent is available to users who have access to a Microsoft 365 Copilot license. To see Sales agent, you must [install the Sales agent](install-sales-app.md).

> [!NOTE]
> - If your team already uses Sales agent, they'll see the Sales in the list of agents in Microsoft 365 Copilot.
> - If all agents for Microsoft 365 Copilot are disabled for your organization, users won't see Sales agent in the list of agents even if they have a Microsoft 365 Copilot license. Learn more about [managing agents for Microsoft 365 Copilot](/microsoft-365/admin/manage/manage-copilot-agents-integrated-apps?view=o365-worldwide#enable-or-disable-copilot-extensibility&preserve-view=true).

## Prerequisites

- [The Sales agent is installed in both Outlook and Teams](install-viva-sales.md).
- You have access to environment-level settings in the [administrator settings for Sales agent](administrator-settings-sales-app.md).
- [Sales Chat must be turned on in Access settings](access-settings.md#sales-agent-in-microsoft-365-copilot-preview).
- The Sales agent must be connected to a CRM system.
- [Appropriate privileges must be assigned to admins and users in the CRM system to set up and access the data](privileges.md). If you are a Salesforce admin, you must assign the security role in the [msdyn_viva environment in Power Platform admin center](privileges.md#access-msdyn_viva-environment-and-assign-security-role).

## Step 1: Configure CRM entities (Dynamics 365 tables or Salesforce objects)

As an administrator, you can customize which CRM information is available to sellers when they ask questions using the Sales agent. The Sales agent accesses CRM information based on the CRM entities configured in Sales agent admin settings. In Dynamics 365, these entities are tables. In Salesforce, these entities are objects.

By default, the Sales agent includes a predefined list of CRM entities. You can customize this list by adding out-of-the-box or custom CRM entities. You can also remove entities that are not required.

> [!NOTE]
> - You can customize the list of CRM entities in Sales agent settings independently without affecting Forms settings.
> - For Dynamics 365, if you've set up Sales agent before January 2026 and added tables in Forms settings, those tables will be available in Sales agent by default.

> [!IMPORTANT]
> To initialize the Sales agent and set up the connection to your CRM, open the **Sales Chat** settings page at least once from the [Sales agent administrator settings](./administrator-settings-sales-app.md#access-administrator-settings). When you load the page for the first time, it triggers the initialization process and loads the supported entities for use in the Sales agent. If you skip this step, the initialization won't be triggered automatically.

### Default CRM entities

By default, Sales agent can access the following CRM entities depending on your CRM system:

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

Sales agent accesses the objects configured in [Forms settings](customize-forms-and-fields.md).

### Add CRM entities to Sales agent

1. [Open the Sales agent administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Features**, select **Sales Chat**.
1. Select **Add**.
    :::image type="content" source="media/sales-chat-record-types.png" alt-text="Screenshot showing the Sales Chat record types settings.":::
1. In the **Add a record type** window, search and select the entities you want to add (tables in Dynamics 365 or objects in Salesforce).
1. Select **Add**.

> [!NOTE]
> - You can add multiple entities at once.
> - Sales agent will have access to all columns in the added entities (tables in Dynamics 365 or objects in Salesforce).

### Remove CRM entities from Sales agent

1. [Open the Sales agent administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Features**, select **Sales Chat**.
1. Select the entities you want to remove, and then select **Remove**.
1. In the confirmation dialog box, select **Remove**.

> [!NOTE]
> - You can remove multiple entities at once.
> - You must have at least one entity configured for Sales agent to function.
> - When you remove a record, the Sales agent will no longer have access to it. If this record is configured in Forms settings, it will still be available in Forms and can be used in other features of the Sales agent.

## Step 2: Set up additional synonyms and glossary terms

Sales reps can use natural language in Sales agent to access CRM information. However, the terms they use may not always match the standard field names in the CRM. Sales agent relies on CRM metadata about entities (tables in Dynamics 365 and objects in Salesforce) to interpret user requests and provide relevant information. Because this metadata is often incomplete, you can supply additional guidance, such as synonyms and glossary terms, to help the AI better understand and map user language to CRM data. Providing this extra information improves the AI's ability to recognize user requests and generate accurate, helpful responses.

### Synonyms

Synonyms are alternative names or phrases that users might use to refer to specific CRM fields. For example, a user might refer to the "Account" field as "Company" or "Client." By adding these synonyms, you help Sales agent understand and respond to user queries more effectively.

#### Dynamics 365

1. Open [Copilot Studio](https://copilotstudio.microsoft.com) and select your Dynamics 365 Sales environment.
1. Select **Agents** > **Copilot in Dynamics 365 Sales**.
1. Select **SalesSpecificQnA** under **Knowledge** section.
1. Select the **Synonyms** section.
1. From the **Select item** list, select the CRM table for which you want to add synonyms.
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

You must add glossary terms in Microsoft Copilot Studio. The glossary terms you add in Copilot Studio work for both the Sales agent and Copilot in Dynamics 365 Sales. Learn more about [adding glossary terms in Copilot Studio](/dynamics365/sales/extend-copilot-chat#add-glossary-to-help-copilot-understand-your-business-terms).

#### Salesforce

Glossary terms are not supported for Salesforce CRM currently.

## Step 3: Configure record summary

Sales reps can get a summary of their accounts and opportunities in Sales agent. To enable this feature, you need to configure the account and opportunity summary settings in the Sales agent admin settings.

Sales agent generates account and opportunity summaries by using commonly used fields from the Account and Opportunity tables and natural language instructions that organize and present the information in a meaningful, useful format. You can [customize the AI instructions](#customize-ai-instructions) to include additional or different fields and tailor how the summary is curated to fit your organization's needs.

### Customize AI instructions

1. Go to the [Sales agent admin settings](administrator-settings-for-viva-sales.md#access-administrator-settings).
1. Under **Environment**, select **Custom AI instructions**.
1. For the **Account summary** or **Opportunity summary** report, select **...** > **Edit**.

    :::image type="content" source="media/sales-chat-custom-ai.png" alt-text="Screenshot showing custom AI instructions for account summary.":::

1. In the **Description** field, customize the default prompt to control how the summary is generated. You can:
   - Describe how to organize and present the information
   - @mention specific field names to specify which fields to include in the summary
   - Use natural language to provide curation instructions to the AI
1. (Optional) Under **Notes summary** and **Interaction summary**, configure the number of weeks of content to include. By default, the summary includes content from the past 4 weeks. The maximum 12 weeks.

    By default, these settings are turned on, and the summary includes notes and interactions from the past 4 weeks. If you want to exclude notes or interactions from the summary, turn off the respective setting.

1. Select **Publish**.

    :::image type="content" source="media/sales-chat-custom-ai-edit.png" alt-text="Screenshot showing edited custom AI instructions for account summary.":::

    The new instructions are applied the next time a user requests a summary in Sales agent. You can test them by requesting a summary in Sales agent.

    If you want to restore the default instructions, select **Restore default**.

> [!NOTE]
> - You can't test the custom instructions before saving them. To validate your changes, connect to a test CRM environment before applying them in your production environment.
> - The effectiveness of a custom instruction depends on the information included in the summary. Whenever you update either the custom instructions or the summary content, review and adjust both to ensure they work well together.

## Step 4: Configure past customer meetings

Meeting insights generated by the Sales agent are accessible in Sales agent. You can [manage access to meeting insights through the Sales agent access settings](access-settings.md#meeting-insights). There are no separate settings for meeting insights specific to Sales agent.

## Step 5 (optional): Enable Microsoft 365 Copilot in model-driven apps

This step is applicable only if you're using Dynamics 365 as your CRM system. Enabling Microsoft 365 Copilot in model-driven apps allows users to access Sales agent directly within the Dynamics 365 apps. Learn how to [enable Microsoft 365 Copilot in model-driven apps](/power-apps/maker/model-driven-apps/add-microsoft-365-copilot).

## Related information

- [Use Sales agent in Microsoft 365 Copilot](use-sales-chat.md)
- [Turn on Sales agent](access-settings.md#sales-agent-in-microsoft-365-copilot-preview)
- [Privileges required to use Sales agent](privileges.md)
