---
title: Configure access settings for meeting insights
description: Control how AI-generated meeting insights are stored in Copilot for Sales with customizable access settings for better data governance.
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

# Configure access settings for meeting insights

As an administrator, you can configure which AI-generated meeting insights are stored in Copilot for Sales. This feature provides governance options to address storage costs and data management concerns.

> [!NOTE]
> If a meeting is marked as Private, the meeting insights won't be stored in Dataverse, regardless of the settings you choose. This ensures that sensitive information remains confidential and isn't accessible to others in the organization.

## Prerequisites

[Copilot AI features must be turned on](suggested-replies.md) for your organization or environment.

## Configure meeting insights storage settings

With this setting, you can specify whether meeting insights are stored in Dataverse. By default, this setting is turned on, meaning that post-meeting insights such as AI-generated notes, questions, and action items for all recorded sales meetings are stored in Dataverse. You can also choose whether to store meeting insights of all users or only of specific security groups.

To configure meeting insights storage settings:

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).

2. Under **Environment**, select **Access settings**.

3. Select **Allow meeting insights**. 

4. Turn on or off the **Turn on access** toggle.
    
    If you turn off this setting, users will no longer receive any meeting insights, and related features will be hidden.

1. If the toggle is turned on, you can choose to store meeting insights of all users or only of specific security groups. To do this, select one of the following options:
    - **No restrictions**: All users' meeting insights are stored.
    - **Set access restrictions**: Meeting insights are stored only of users in the selected security groups. You can add security groups in **Allow access** and **Restrict access** sections. Leaving the **Allow access** section empty will allow all users to access the feature. 

1. Select **Save** to apply the changes.
