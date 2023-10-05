---
title: Integrate Microsoft Sales Copilot with other applications
description: Learn how to integrate Sales Copilot with other applications
ms.date: 10/09/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Integrate Microsoft Sales Copilot with other applications (preview)

[!INCLUDE [preview-note](includes/preview-note.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

You can use extensions to integrate Sales Copilot with other applications. Integration helps you enhance the functionality of Sales Copilot and adds insights for your salespeople.

## Integrate with Viva Topics

Viva Topics provides information to users when they need it. When sellers are having a conversation with a customer in a Teams meeting and some topics are mentioned that are not familiar to sellers, Viva Topics can help them understand what a topic means, who in the organization is an expert on the topic, and websites and documents that are related to the topic. Learn more about [Viva Topics](/viva/topics/topic-experiences-overview).

Integrate with Viva Topics to give your sellers a quick way to find company information. Viva Topics detects keywords in the Teams transcript. Then, in the summary, sellers can see content that seems to be related to these keywords. 

By default, the integration is disabled. When enabled, identified topics are displayed on the **Mentions** tab when [viewing a meeting summary](view-understand-meeting-summary.md#view-viva-topics-in-meeting-summary-preview).

> [!NOTE]
> Sellers must have a license of Viva Topics to see them in meeting summary.

### Turn on Viva Topics integration

1.	In Sales Copilot admin settings, select **Extensions**.

2.	Turn on **Microsoft Viva Topics (preview)**.

3.	Select **Save**.

    :::image type="content" source="media/enable-viva-topics.png" alt-text="Screenshot setting to enable Viva Topics integration.":::

## Integrate with People.ai

Integrate with People.ai to get insights into your sellers' activities and their engagement with customers. The insights are based on the data that is collected from your sellers' email and meeting. Insights from People.ai are displayed for contacts, opportunities, and accounts.

By default, the integration is disabled. When enabled, the insights are displayed in the [detailed view of a record](view-record-details.md#view-peopleai-insights-preview) as well as in the [opportunity summary card](view-opportunity-summary.md#view-peopleai-insights-in-opportunity-summary-preview) in the **Sales Copilot** pane in Outlook.

### Prerequisites

- You must generate an API key and API secret from admin settings in People.ai. They are used to authenticate and connect you with People.ai. 

> [!NOTE]
> - People.ai is currently available only for Salesforce customers. People.ai settings are displayed only if you are connected to a Salesforce environment.
> - A user license is required to view People.ai insights in the Sales Copilot pane in Outlook.

### Turn on People.ai integration

1.	In Sales Copilot admin settings, select **Extensions**.

2.	Turn on **People.ai (preview)**.

3.	Enter the values for API key and API Secret.

4.	Select **Save**.

    :::image type="content" source="media/enable-people-ai.png" alt-text="Screenshot setting to enable People.ai integration.":::