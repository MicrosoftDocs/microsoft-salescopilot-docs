---
title: View record details
description: Learn how to view record details.
ms.date: 10/09/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# View record details

You can view details about your saved contact and its related records such as account and opportunities.

> [!NOTE]
> All record types that are added by your administrator are displayed, if related to contact, when viewing saved contact details.

1. Open the **Sales Copilot** pane and select the **Dynamics 365** or **Salesforce** tab.

1. In the **(record type)** card, select the record to see the details. For example, if you want to see details of an opportunity, select the opportunity in the **Opportunities** card.

   :::image type="content" source="media/opportunities.png" alt-text="Screenshot showing how to select a record to see its details.":::

If you have a license for People.ai and the capability to display insights from People.ai is [enabled by your administrator](use-extensions.md#integrate-with-peopleai), insights from People.ai are displayed for contacts, opportunities, and accounts. More information: [View People.ai insights](#view-peopleai-insights-preview)

## Open a record in CRM

You can also open a record in CRM to view its complete details. In record details, select **More actions** (**...**), and then select **Open in Dynamics 365** or **Open in Salesforce**. The record details will open in a new tab.

:::image type="content" source="media/open-dynamics.png" alt-text="Screenshot showing the open in CRM icon.":::

Alternately, you can also open a record in CRM from the **Dynamics 365** or **Salesforce** tab. Hover over a record, select **More actions** (**...**), and then select **Open in Dynamics 365** or **Open in Salesforce**.

:::image type="content" source="media/more-actions.png" alt-text="Screenshot showing how to open a record in CRM.":::

## View People.ai insights (preview)

[!INCLUDE [preview-banner-section](includes/preview-banner-section.md)]

**Prerequisites**: 

- The People.ai integration must be enabled by your administrator. 
- You must have a license for People.ai.

Insights from People.ai are displayed in a new card for contacts and accounts, and under the **Insights from People.ai** section for opportunities. Insights are displayed with citation numbers. Select the citation number to drill down and see detailed information. For contact and account records, data from the past 90 days is considered to generate insights.

:::image type="content" source="media/people-ai-contact-insights.png" alt-text="Screenshot showing People.ai insights in contact details.":::

The following insights are displayed:

- **Engagement level**: This is the overall engagement level. The engagement level is calculated based on  interactions (emails and meetings) that have happened with the customer. The engagement level is displayed as low, medium, or high. When you drill down into the engagement level and trend, you can see the total number of activities, along with the breakdown of the number of meetings and emails that have been exchanged with the customer. To open metrics in People.ai, select :::image type="icon" source="media/open-record.png" border="false"::: at the bottom-right of the card.

- **Connections**: This insight suggests the names of your colleagues who have interacted with the customer through emails or meetings. It helps you quickly email your colleagues to request an introduction. When you drill down, you can see the names of the people. By default, the top three connections are displayed. 

    To quickly start an email with one of the top connections, hover over the name, and then select :::image type="icon" source="media/mail-icon.png" border="false":::.

    To see all connections or more metrics, you must go to People.ai. Select :::image type="icon" source="media/open-record.png" border="false"::: at the bottom-right of the card to open People.ai.

- **Predicted buying power**: This insight is displayed only for a contact. It shows the likely range of buying power of the contact. The buying power is calculated based on the number of deals that the contact has closed in the past 90 days. The closed deals are compared with similar won opportunities involving stakeholders who are similar to the contact in terms of their title, department, and industry. When you drill down, you can see detailed information. To open metrics in People.ai, select   at the bottom-right of the card.