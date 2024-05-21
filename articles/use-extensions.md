---
title: Integrate Microsoft Copilot for Sales with other applications
description: Learn how to integrate Copilot for Sales with other applications
ms.date: 04/12/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Integrate Microsoft Copilot for Sales with other applications (preview)

[!INCLUDE [preview-note](includes/preview-note.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

You can integrate Copilot for Sales with other applications such as Microsoft Viva Topics and People.ai to enhance the functionality of Copilot for Sales and add insights for your sellers.

## Integrate with Viva Topics

> [!IMPORTANT]
> Copilot for Sales integration with Viva Topics in conversation intelligence will be deprecated on February 22, 2025 due to the deprecation of Viva Topics. If you already have an integration with Viva Topics, you can continue to use this feature until the deprecation date. New integrations between Copilot for Sales and Viva Topics will be blocked from May 10, 2024.


Viva Topics provides information to users when they need it. When sellers are having a conversation with a customer in a Teams meeting and some topics are mentioned that are not familiar to sellers, Viva Topics can help them understand what a topic means, who in the organization is an expert on the topic, and websites and documents that are related to the topic. Learn more about [Viva Topics](/viva/topics/topic-experiences-overview).

Integrate with Viva Topics to give your sellers a quick way to find company information. Viva Topics detects keywords in the Teams transcript. Then, in the summary, sellers can see content that seems to be related to these keywords. 

By default, the integration is disabled. When enabled, identified topics are displayed on the **Mentions** tab when [viewing a meeting summary](view-understand-meeting-summary.md#view-viva-topics-in-meeting-summary-preview).

> [!NOTE]
> Sellers must have a license of Viva Topics to see them in meeting summary.

### Turn on Viva Topics integration

1.	In Copilot for Sales admin settings, select **Extensions**.

2.	Turn on **Microsoft Viva Topics (preview)**.

3.	Select **Save**.

    :::image type="content" source="media/enable-viva-topics.png" alt-text="Screenshot setting to enable Viva Topics integration.":::

## Integrate with People.ai

Integrate with People.ai to get insights into your sellers' activities and their engagement with customers. The insights are based on the data that is collected from your sellers' email and meeting. Insights from People.ai are displayed for contacts, opportunities, and accounts.

By default, the integration is disabled. When enabled, the insights are displayed in the [detailed view of a record](view-record-details.md) as well as in the [opportunity summary card](view-opportunity-summary.md) in the **Copilot for Sales** pane in Outlook. More information: [View People.ai insights (preview)](people-ai-insights.md)

### Prerequisites

- You must generate an API key and API secret from admin settings in People.ai. They are used to authenticate and connect you with People.ai. 

> [!NOTE]
> - People.ai is currently available only for Salesforce customers. People.ai settings are displayed only if you are connected to a Salesforce environment.
> - A user license is required to view People.ai insights in the Copilot for Sales pane in Outlook.

### Turn on People.ai integration

1.	In Copilot for Sales admin settings, select **Extensions**.

2.	Turn on **People.ai (preview)**.

3.	Enter the values for API key and API Secret.

4.	Select **Save**.

    :::image type="content" source="media/enable-people-ai.png" alt-text="Screenshot setting to enable People.ai integration.":::
