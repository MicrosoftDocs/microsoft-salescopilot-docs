---
title: View record details
description: View details about saved contacts and related records such as accounts and opportunities in CRM.
ms.date: 02/02/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:10/12/2023
---

# View record details

You can view details about your saved contact and its related records such as account and opportunities.

> [!NOTE]
> All record types that are added by your administrator are displayed, if related to contact, when viewing saved contact details.

1. Open the **Copilot for Sales** pane.

1. In the **(record type)** card, select the record to see the details. For example, if you want to see details of an opportunity, select the opportunity in the **Opportunities** card.

If you have a license for People.ai and the capability to display insights from People.ai is [enabled by your administrator](use-extensions.md#integrate-with-peopleai), insights from People.ai are displayed for contacts, opportunities, and accounts. More information: [View People.ai insights](#view-peopleai-insights-preview)

## Open a record in CRM

You can also open a record in CRM to view its complete details. In record details, select **More actions** (**...**), and then select **Open in (CRM)**. The record details open in a new tab.

:::image type="content" source="media/open-dynamics.png" alt-text="Screenshot showing the open in CRM icon.":::

Alternately, you can also open a record in CRM from the **Copilot for Sales** pane. Hover over a record, select **More actions** (**...**), and then select **Open in (CRM)**.

:::image type="content" source="media/more-actions.png" alt-text="Screenshot showing how to open a record in CRM.":::

> [!NOTE]
> If you're using Salesforce as your CRM, this feature works only if you're using the Lightning Experience.

## View People.ai insights (preview)

[!INCLUDE [preview-banner-section](includes/preview-banner-section.md)]

**Prerequisites**: 

- The People.ai integration must be [enabled by your administrator](use-extensions.md#integrate-with-peopleai). 
- You must have a license for People.ai.

Insights from People.ai are displayed in a new card for contacts and accounts, and under the **Insights from People.ai** section for opportunities. Insights are displayed with citation numbers. Select the citation number to drill down and see detailed information. For contact and account records, data from the past 90 days is considered to generate insights. To open metrics in People.ai, select :::image type="icon" source="media/open-record.png" border="false"::: at the bottom-right of the card.

:::image type="content" source="media/people-ai-contact-insights.png" alt-text="Screenshot showing People.ai insights in contact details.":::

The following insights are displayed:

- **Engagement level and trend**: This is the overall engagement level and trend. The engagement level number is calculated by People.ai based on interactions (emails and meetings) that have happened with the customer. The engagement level is displayed as follows:
   
    |Engagement level number  |Engagement level  |
    |---------|---------|
    |0 to 30     | Low        |
    |31 to 70     | Medium        |
    |71 to 100     | High        |
    
    The engagement trend is calculated by comparing the current week’s engagement level number with that of the previous week. The engagement trend is displayed as trending up or down based on the increase or decrease of the engagement level respectively. 

    When you drill down into the engagement level and trend, you can see the total number of activities, along with the breakdown of the number of meetings and emails that have been exchanged with the customer.

- **Connections**: This insight suggests the names of your colleagues who have interacted with the customer through emails or meetings. It helps you quickly email your colleagues to request an introduction. When you drill down, you can see the names of the people. By default, the top three connections are displayed. 

    To quickly start an email with one of the top connections, hover over the name, and then select :::image type="icon" source="media/mail-icon.png" border="false":::.

    To see all connections or more metrics, you must open People.ai.

- **Predicted buying power**: This insight is displayed only for a contact. It shows the likely range of buying power of the contact. The buying power is calculated based on the number of deals that the contact has closed in the past 90 days. The closed deals are compared with similar won opportunities involving stakeholders who are similar to the contact in terms of their title, department, and industry. When you drill down, you can see detailed information.

## View related records from partner applications (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner-section](includes/preview-banner-section.md)]

You can view records that are related to CRM records from partner applications within Copilot for Sales. To view related records from partner applications, you must:

1. Get the feature enabled, as it is not enabled by default.
2. Create a connection using Power Platform connectors.
3. View related records from partner applications.

### Get the feature enabled

This feature is not enabled by default. To enable this feature, ask your administrator to [sign up for the preview feature](https://aka.ms/SalesCopilotExtensibilityPreview). The Microsoft team will get in touch to validate the request and enable the feature for your organization.

### Create a connection

After the feature is enabled, you must create a connection between Copilot for Sales and the partner application using the partner's certified Power Platform connector. For information about how to create a connection, see [Create a new connection](/power-apps/maker/canvas-apps/add-manage-connections#create-a-new-connection).

> [!NOTE]
> - All Power Platform connectors are not certified to work with Copilot for Sales. Copilot for Sales displays activities from partner applications that have implemented specific APIs and made them available through their Power Platform connectors.
> - If you are a partner application maker and would like to integrate with Copilot for Sales, see Extend Copilot for Sales. Currently, DocuSign can be integrated with Copilot for Sales. 

### View related records

Related records from partner applications are displayed in a new card under record details. For example, in the following image, the contract documents related to a CRM opportunity are displayed from the partner application **DocuSign**.

:::image type="content" source="media/record-details-partner-apps.png" alt-text="Sceenshot showing related records from DocuSign":::

> [!NOTE]
> Currently, related records from partner applications are shown only for opportunities and accounts.

All the information about related records comes from the partner applications. Copilot for Sales renders the related record information retrieved from the partner application through the Power Platform connector. Copilot for Sales does not edit or filter the information.

You can perform the following actions on the related records:
- To see record details, select the record. 
- To copy link to a record or open it in the partner application, hover over the record, select **More actions** (**…**), and then select **Copy link** or **Open in (partner app)** respectively.
