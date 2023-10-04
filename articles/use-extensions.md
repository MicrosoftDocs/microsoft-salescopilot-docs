---
title: Use extensions to integrate with third-party applications
description: Learn how to use extensions to integrate with third-party applications
ms.date: 10/09/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Use extensions (preview)

[!INCLUDE [preview-note](includes/preview-note.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

You can use extensions to integrate with third-party applications. Integration helps you enhance the functionality of Sales Copilot and adds insights for your salespeople.

## Integrate with Viva Topics

Integrate with Viva Topics give your sellers a quick way of finding files related to sales meetings. Viva Topics detects keywords in the Teams transcript. Then, in the summary, sellers can see content that seems to be related to these keywords. 

By default, the integration is disabled. When enabled, identified topics are displayed on the **Mentions** tab when [viewing a meeting summary](view-understand-meeting-summary.md#view-viva-topics-in-meeting-summary-preview).

> [!NOTE]
> Sellers must have a license of Viva Topics to see them in meeting summary.

### Turn on Viva Topics integration

1.	In Sales Copilot admin settings, select **Extensions**.

2.	Turn on Microsoft **Viva Topics (preview)**.

3.	Select **Save**.

    :::image type="content" source="media/enable-viva-topics.png" alt-text="Screenshot setting to enable Viva Topics integration.":::

## Integrate with People.ai

Integrate with People.ai to get insights into your sellers' activities and their engagement with customers. The insights are based on the data that is collected from your sellers' email and meeting. People.ai displays insights for contacts, opportunities, and accounts. By default, the integration is disabled. When enabled, the insights are displayed in the [detailed view of a record](view-record-details.md#view-peopleai-insights-preview) as well as in the [opportunity summary card](view-opportunity-summary.md#view-peopleai-insights-in-opportunity-summary-preview) in the **Sales Copilot** pane in Outlook.

### Prerequisites

- You must generate an API key and API secret from admin settings in People.ai. They are used to authenticate and connect you with People.ai. 
- Connect Sales Copilot to Salesforce CRM. Currently, insights from People.ai are displayed only for Salesforce CRM users.

### Turn on People.ai integration

1.	In Sales Copilot admin settings, select **Extensions**.

2.	Turn on **People.ai (preview)**.

3.	Enter the values for API key and API Secret.

4.	Select **Save**.

    :::image type="content" source="media/enable-people-ai.png" alt-text="Screenshot setting to enable People.ai integration.":::