---
title: Integrate Microsoft 365 Copilot for Sales with other applications
description: Learn how to integrate Copilot for Sales with other applications
ms.date: 01/24/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Integrate Microsoft 365 Copilot for Sales with other applications (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

You can integrate Copilot for Sales with other applications such as People.ai to enhance the functionality of Copilot for Sales and add insights for your sellers.

## Integrate with People.ai

Integrate with People.ai to get insights into your sellers' activities and their engagement with customers. The insights are based on the data that is collected from your sellers' email and meeting. Insights from People.ai are displayed for contacts, opportunities, and accounts.  
By default, the integration is disabled. When enabled, the insights are displayed in the [detailed view of a record](view-record-details.md) as well as in the [opportunity summary card](view-opportunity-summary.md) in the **Copilot for Sales** pane in Outlook. More information: [View People.ai insights (preview)](people-ai-insights.md)

### Prerequisites

- You must generate an API key and API secret from admin settings in People.ai. They are used to authenticate and connect you with People.ai. 

> [!NOTE]
> - People.ai is currently available only for Salesforce customers. People.ai settings are displayed only if you are connected to a Salesforce environment.
> - A user license is required to view People.ai insights in the Copilot for Sales pane in Outlook.

### Turn on People.ai integration

1. In Copilot for Sales admin settings, select **Extensions**.  
1. Turn on **People.ai (preview)**.  
1. Enter the values for API key and API Secret.  
1. Select **Save**.
