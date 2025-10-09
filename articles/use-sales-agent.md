---
title: Use Sales Agent (preview)
description: Learn how to view the research conducted on your leads by Sales Agent.
ms.date: 06/13/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Use Sales Agent (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Sales Agent provides you with a comprehensive overview of the research conducted on your leads. This includes insights into the lead's company, recent news, and other relevant information that can help you tailor your outreach strategy. You can view this research in your CRM and in the Sales personal app.

## View leads researched in Sales personal app

When your administrator has enabled the Sales Agent, you can view the leads that are researched by the Sales Agent in the Sales personal app. 

1. Open the Sales personal app in Teams or Outlook.
1. Navigate to the **Home** tab of the app.
1. On the **Automated lead research with Sales Agent** card, select **View leads**.

    :::image type="content" source="./media/sales-agent-home.png" alt-text="Screenshot showing home page of Sales personal app with card for the Sales Agent.":::

    The **Leads researched by Sales Agent** page opens with a list of leads that are researched by Sales Agent. 

    :::image type="content" source="./media/sales-agent-lead-list.png" alt-text="Screenshot showing leads researched by Sales Agent in Sales personal app.":::

    > [!NOTE]
    > - Only leads that your admin has configured to be researched are displayed in this list.
    > - Only leads you have access to view in the CRM are shown.
    > - Sales Agent automatically performs research on leads when they're created or modified in your CRM. You can see the status of the research progress on this list.

1. To view the research details for a lead, select the lead from the list. The lead research details page provides a summary of the research conducted by Sales Agent, including key insights and information about the lead's company. Learn more about the [lead research details](#view-lead-research-details-in-copilot-for-sales-personal-app).

## View lead research details in Sales personal app

The Sales Agent shows the key insights it has gathered, such as if the lead is a decision maker or even a real person or company, so you can make quick decisions to disqualify or pursue each lead. The company's key information, such as their industry, finances, strategic priorities, and business challenges are summarized to help you learn what you need to know about every lead.

:::image type="content" source="./media/sales-agent-lead-research-details.png" alt-text="Screenshot showing the Sales Agent research details for a lead.":::

## View lead research in your CRM

A summary of the lead research will be available in your CRM if your admin has configured this capability. The summary provides a short summary of the information gathered about the lead, along with a link to view the full research details in the Sales personal app.

1. Open your CRM (Microsoft Dynamics 365 Sales or Salesforce Sales Cloud).
1. Navigate to the lead record you want to view.
1. Look for the **Sales Agent** section on the lead record page. This section contains the summary of the research conducted by Sales Agent.
1. Select **View research details** to see the full research report in the Sales personal app.

    :::image type="content" source="./media/sales-agent-crm-summary.png" alt-text="Screenshot showing a CRM with the lead research summary card.":::

## Related information

- [Sales Agent overview](sales-agent-overview.md)
- [Send outreach email to leads](send-outreach-emails.md)