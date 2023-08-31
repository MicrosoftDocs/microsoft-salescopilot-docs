---
title: Configure Sales Copilot for Microsoft 365 apps
description: Learn how to configure Sales Copilot for Microsoft 365 apps.
ms.date: 07/12/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Configure Sales Copilot for Microsoft 365 apps

[!INCLUDE[vs-rebrand-note](includes/vs-rebrand-note.md)]

A few Sales Copilot features run within a Microsoft 365 app service apart from the standard Outlook add-in and Teams app. Feature mentioned in the following sections can be disabled or enabled by a tenant administrator from Microsoft 365 admin center. By default, the feature is enabled.

**To disable the feature**

1.	Sign in to Microsoft 365 admin center with tenant admin credentials.
2.	Select **Settings** > **Org settings**.
3.	On the **Org settings** page, under the **Services** tab, select **Sales Copilot**.
4.	In the **Sales Copilot** panel, select **Allow users to see Sales Copilot content in Microsoft 365 apps**.

> [!NOTE] 
> If you disable the feature, notifications are not removed from the existing emails that are in the inbox, but no further incoming emails will be processed to display the banner.

## Sales Copilot email notification banner

To help users in finding Sales Copilot when interacting with external customer emails, a Microsoft 365 service is used to process incoming emails and provide a notification banner at the top of incoming emails. Banner notifications are displayed on a limited number of emails per day when either the incoming email is from an external email domain or an external email address is included in the **To** or **Cc** field. 
