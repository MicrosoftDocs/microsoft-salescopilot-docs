---
title: Integrate Microsoft 365 Copilot for Sales with other applications (preview) 
description: Learn how to integrate Copilot for Sales with People.ai to enhance the functionality of Copilot for Sales and add insights for your sellers.
ms.date: 03/10/2025
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

If your organization uses Salesforce for customer relationship management, integrate Copilot for Sales with People.ai to get insights into your sellers' activities and their engagement with customers. People.ai insights are based on your sellers' emails and meetings and are displayed for contacts, opportunities, and accounts.

People.ai integration is turned off by default. When it's turned on, insights are displayed in the **Copilot for Sales** pane in Outlook. More information: [View People.ai insights (preview)](people-ai-insights.md)

### Prerequisites

- You must generate an API key and API secret from admin settings in People.ai. They are used to authenticate and connect you with People.ai. 

> [!NOTE]
> - People.ai is currently available only for Salesforce customers. People.ai settings are displayed only if you are connected to a Salesforce environment.
> - A user license is required to view People.ai insights in the Copilot for Sales pane in Outlook.

### Turn on People.ai integration

1. [Open Copilot for Sales administrator settings](administrator-settings-for-viva-sales.md#access-administrator-settings).

1. Under **Environment**, select **Extensions**.

1. Turn on **People.ai (preview)**.

1. Enter the API key and API secret you generated in the People.ai administrative settings.

1. Select **Save**.