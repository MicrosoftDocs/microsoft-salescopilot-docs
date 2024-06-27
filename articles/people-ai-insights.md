---
title: View People.ai insights (preview)
description: View comprehensive customer insights from People.ai, including engagement levels, connections, and predicted buying power.
ms.date: 05/20/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:03/13/2024
---

# View People.ai insights (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

People.ai insights provide a comprehensive view of your customer interactions and engagement. You can view insights for your accounts, contacts, and opportunities when [viewing details of a record](view-record-details.md) in the Copilot for Sales pane. 

## Prerequisites

- The People.ai integration must be [enabled by your administrator](use-extensions.md#integrate-with-peopleai). 
- You must have a license for People.ai.

## View insights from People.ai

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