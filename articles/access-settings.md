---
title: Configure access settings for features in Copilot for Sales
description: Control access to various features in Copilot for Sales, including meeting insights and Sales Agent capabilities.
ms.date: 08/13/2025
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

# Configure access settings for features in Copilot for Sales

As an administrator, you can enable or disable features in Copilot for Sales. You can also control who has access to these features by specifying security groups. 

## Meeting insights

You can control whether meeting insights are stored in Dataverse. By default, the feature is turned on, so post-meeting insights—including AI-generated notes, questions, and action items from all recorded sales meetings—are stored in Dataverse. You can choose to store meeting insights for all users or for specific security groups.

> [!NOTE]
> If a meeting is marked as Private, the meeting insights won't be stored in Dataverse, regardless of the settings you choose. This ensures that sensitive information remains confidential and isn't accessible to others in the organization.

### Prerequisites

[Copilot AI features must be turned on](suggested-replies.md) for your organization or environment.

### Configure meeting insights access settings

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).

1. Under **Environment**, select **Access settings**.

1. Select **Allow meeting insights**. 

1. In the **Allow meeting insights** pane, turn on or off the toggle.

1. If you turn on the toggle, you can choose to store meeting insights for all users or only for specific security groups. To do this, select one of the following options:
    - **No restrictions**: All users' meeting insights are stored.
    - **Set access restrictions**: Use security groups to decide which users' meeting insights are stored. 
        - **Allow access**: Search and add security groups that can access the feature.
        - **Restrict access**: Search and add security groups that cannot access the feature.
        
        Ensure you add security groups in either of the sections. Leaving them empty is not allowed.

1. Select **Save**.

After you turn on meeting insights storage, you can configure [meeting insights settings](configure-meeting-agent.md) such as auto-recording of sales meetings and pre-and-post meeting notification configurations.

If you want to turn off meeting insights storage, follow the same steps to access the **Allow meeting insights** pane and turn off the toggle. If you turn off this setting, users will no longer receive any meeting insights, and related features will be hidden.

## Sales Agent (preview)

[!INCLUDE [preview-banner-section](~/../shared-content/shared/preview-includes/preview-banner-section.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Sales Agent allows sellers to automate lead research and get insights about their leads. It helps sellers prepare for meetings by providing relevant information about the lead, such as company details and recent news. 

By default, Sales Agent is turned off. When you turn it on, you can control whether Sales Agent is available to all sellers or only to specific security groups.

To turn on Sales Agent:

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).
1. Under **Environment**, select **Access settings**.
1. Select **Sales Agent**.
1. In the **Sales Agent** pane, turn on the toggle.   
1. Under **Who can access this feature?**, choose to allow access to all sellers or only to specific security groups. To do this, select one of the following options:
    - **No restrictions**: All sellers in the environment can use the feature.
    - **Set access restrictions**: Use security groups to decide which sellers can use the feature. 
        - **Allow access**: Search and add security groups that can access the feature.
        - **Restrict access**: Search and add security groups that cannot access the feature.
        
        Ensure you add security groups in either of the sections. Leaving them empty is not allowed.

1. Select **Save**.

After you turn on Sales Agent, you can [set up and activate the Sales Agent feature from the **Sales Agent - Lead Research** settings page](set-up-sales-agent.md).

If you want to turn off Sales Agent, follow the same steps to access the **Sales Agent** pane and turn off the toggle. If you turn off this setting, sellers will no longer see the Sales Agent feature in Copilot for Sales. Turning off the agent will stop the agent from researching leads.

## Related information

- [Configure meeting insights settings](configure-meeting-agent.md)
- [Set up and activate Sales Agent](set-up-sales-agent.md)