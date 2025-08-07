---
title: Configure access settings for features in Copilot for Sales
description: Control access to various features in Copilot for Sales, including meeting insights and Sales Agent capabilities.
ms.date: 07/09/2025
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

As an administrator, you can turn features on or off and manage access permissions for sellers across Microsoft products.

## Configure meeting insights storage settings

With this setting, you can specify whether meeting insights are stored in Dataverse. By default, this setting is turned on, meaning that post-meeting insights such as AI-generated notes, questions, and action items for all recorded sales meetings are stored in Dataverse. You can also choose whether to store meeting insights of all users or only of specific security groups.

> [!NOTE]
> If a meeting is marked as Private, the meeting insights won't be stored in Dataverse, regardless of the settings you choose. This ensures that sensitive information remains confidential and isn't accessible to others in the organization.

### Prerequisites

- [Copilot AI features must be turned on](suggested-replies.md) for your organization or environment.

### Turn on or off meeting insights storage 

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).

1. Under **Environment**, select **Access settings**.

1. Select **Allow meeting insights**. 

1. Turn on or off the **Turn on access** toggle.
    
    If you turn off this setting, users will no longer receive any meeting insights, and related features will be hidden.

1. If the toggle is turned on, you can choose to store meeting insights of all users or only of specific security groups. To do this, select one of the following options:
    - **No restrictions**: All users' meeting insights are stored.
    - **Set access restrictions**: Meeting insights are stored only of users in the selected security groups. You can add security groups in **Allow access** and **Restrict access** sections. Leaving the **Allow access** section empty will allow all users to access the feature, except those in the **Restrict access** section.

1. Select **Save** to apply the changes.

## Configure email insights storage settings (preview)

[!INCLUDE [preview-banner-section](~/../shared-content/shared/preview-includes/preview-banner-section.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

With this setting, you can specify whether email insights are stored in Dataverse. By default, this setting is turned off. When you turn it on, AI-generated email insights such as summary, sentiment, objections, and next steps for sales emails with at least one CRM contact are stored in Dataverse. You can also choose whether to store email insights of all users or only of specific security groups.

### Prerequisites

- [Copilot AI features must be turned on](suggested-replies.md) for your organization or environment.
- If you're using Salesforce, you must have [set up a server-to-server connection](connect-agent-datasource.md#set-up-server-to-server-connection-to-salesforce) to allow the agent to access data in Salesforce.

### Turn on or off email insights storage

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).

1. Under **Environment**, select **Access settings**.

1. Select **Email insights (preview)**.

1. Turn on or off the **Turn on access** toggle.

    If you turn off this setting, users will no longer receive any email insights, and related features will be hidden.

1. If the toggle is turned on, you can choose to store email insights of all users or only of specific security groups. To do this, select one of the following options:
    - **No restrictions**: All users' email insights are stored.
    - **Set access restrictions**: Email insights are stored only of users in the selected security groups. You can add security groups in **Allow access** and **Restrict access** sections. Leaving the **Allow access** section empty will allow all users to access the feature, except those in the **Restrict access** section.

1. Select **Save** to apply the changes.

After you turn on this setting, you can configure the [email insights settings](email-insights-settings.md) such as sharing of email insights and including email with sensitivity labels.

## Related information

- [Configure email insights settings (preview)](email-insights-settings.md)