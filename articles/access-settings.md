---
title: Configure access settings for features in the Sales app
description: Control access to various features in the Sales app, including meeting insights and Sales Agent capabilities.
ms.date: 12/01/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ai-usage: ai-assisted
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-description
  - ai-seo-date:05/06/2025
---

# Configure access settings for features in the Sales app

As an administrator, you can enable or disable features in the Sales app. You can also control who has access to these features by specifying security groups. 

## Meeting insights

You can control whether meeting insights are stored in Dataverse. By default, the feature is turned on, so post-meeting insights—including AI-generated notes, questions, and action items from all recorded sales meetings—are stored in Dataverse. You can choose to store meeting insights for all users or for specific security groups.

> [!NOTE]
> If a meeting is marked as Private, the meeting insights won't be stored in Dataverse, regardless of the settings you choose. This ensures that sensitive information remains confidential and isn't accessible to others in the organization.

### Prerequisites

[Copilot AI features must be turned on](suggested-replies.md) for your organization or environment.

### Configure meeting insights access settings

1. [Open the Sales app administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).

1. Under **Environment**, select **Access settings**.

1. Select **Allow meeting insights**. 

1. In the **Allow meeting insights** pane, turn on or off the toggle.

1. If you turn on the toggle, you can choose to store meeting insights for all users or only for specific security groups. Under **Who can access this feature?**, select one of the following options:
    - **No restrictions**: All users' meeting insights are stored.
    - **Set access restrictions**: Use security groups to decide which users' meeting insights are stored. 
        - **Allow access**: Search and add security groups that can access the feature.
        - **Restrict access**: Search and add security groups that cannot access the feature.

        You must add security groups in either of the sections to save the changes.

1. Select **Save**.

    :::image type="content" source="media/meeting-insights-access-settings.png" alt-text="Screenshot showing meeting insights access settings.":::

You can configure [meeting insights settings](configure-meeting-agent.md) such as auto-recording of sales meetings and pre-and-post meeting notification configurations on the **Meeting insights** settings page.

If you want to turn off meeting insights storage, follow the same steps to access the **Allow meeting insights** pane and turn off the toggle. If you turn off this setting, users will no longer receive any meeting insights, and related features will be hidden.

## Sales Agent - Lead Research (preview)

[!INCLUDE [preview-banner-section](~/../shared-content/shared/preview-includes/preview-banner-section.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Sales Agent allows sellers to automate lead research and get insights about their leads. It helps sellers prepare for meetings by providing relevant information about the lead, such as company details and recent news. 

By default, Sales Agent is turned off. When you turn it on, you can control whether Sales Agent is available to all sellers or only to specific security groups.

To turn on Sales Agent:

1. [Open the Sales app administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Environment**, select **Access settings**.
1. Select **Sales Agent**.
1. In the **Sales Agent** pane, turn on the toggle.   
1. Under **Who can access this feature?**, choose to allow access to all sellers or only to specific security groups. To do this, select one of the following options:
    - **No restrictions**: All sellers in the environment can use the feature.
    - **Set access restrictions**: Use security groups to decide which sellers can use the feature. 
        - **Allow access**: Search and add security groups that can access the feature.
        - **Restrict access**: Search and add security groups that cannot access the feature.

        You must add security groups in either of the sections to save the changes.

1. Select **Save**.

    :::image type="content" source="media/sales-agent-access-settings.png" alt-text="Screenshot showing Sales Agent access settings.":::

After you turn on Sales Agent, you can [set up and activate the Sales Agent feature from the **Sales Agent - Lead Research** settings page](set-up-sales-agent.md).

If you want to turn off Sales Agent, follow the same steps to access the **Sales Agent** pane and turn off the toggle. If you turn off this setting, sellers will no longer see the Sales Agent feature in the Sales app. Turning off the agent will stop the agent from researching leads.

## Sales agent in Microsoft 365 Copilot (preview)

[!INCLUDE [preview-banner-section](~/../shared-content/shared/preview-includes/preview-banner-section.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Sales agent is an AI-powered chat interface that allows sellers to interact with their sales data using natural language. Sellers can ask questions and gain insights from their CRM data and past customer conversations. By default, Sales agent is turned on for all users. You can choose to restrict access to specific security groups or turn off the feature entirely.

To configure Sales agent access settings:

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).
1. Under **Environment**, select **Access settings**.
1. Select **Allow access to Sales Chat**.
1. In the **Allow access to Sales Chat** pane, turn on or off the toggle.
1. If you turn on the toggle, you can choose to allow access for all users or only for specific security groups. Under **Who can access this feature?**, select one of the following options:
    - **No restrictions**: All users can use the feature.
    - **Set access restrictions**: Use security groups to decide which users can use the feature.
        - **Allow access**: Search and add security groups that can access the feature.
        - **Restrict access**: Search and add security groups that cannot access the feature.

        You must add security groups in either of the sections to save the changes.

1. Select **Save**.

    :::image type="content" source="media/sales-chat-access-settings.png" alt-text="Screenshot showing Sales agent access settings.":::

After you turn on Sales agent, you can [set up and configure Sales agent from the **Sales Chat** settings page](set-up-sales-chat.md).

If you want to turn off Sales agent, follow the same steps to access the **Allow access to Sales Chat** pane and turn off the toggle. If you turn off this setting, users who have Copilot for Sales app installed will still see Sales as an agent in Microsoft 365 Copilot chat. They can still ask questions and get responses, but the responses will not include any Sales data.

## Related information

- [Configure meeting insights settings](configure-meeting-agent.md)
- [Set up and activate Sales Agent - Lead Research](set-up-sales-agent.md)
- [Set up Sales agent in Microsoft 365 Copilot](set-up-sales-chat.md)