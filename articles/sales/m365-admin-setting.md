---
title: Configure Viva Sales for Microsoft 365 apps
description: Learn how to configure Viva Sales for Microsoft 365 apps.
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

# Configure Viva Sales for Microsoft 365 apps

A few Viva Sales features run within a Microsoft 365 app service apart from the standard Outlook add-in and Teams app. Feature mentioned in the following sections can be disabled or enabled by a tenant administrator from Microsoft 365 admin center. By default, the feature is enabled.

**To disable the feature**

1.	Sign in to Microsoft 365 admin center with tenant admin credentials.
2.	Select **Settings** > **Org settings**.
3.	On the **Org settings** page, under the **Services** tab, select **Viva Sales**.
4.	In the **Viva Sales** panel, select **Allow users to see Viva Sales content in Microsoft 365 apps**.

> [!NOTE] 
> If you disable the feature, notifications are not removed from the existing emails that are in the inbox, but no further incoming emails will be processed to display the banner.

## Viva Sales email notification banner

To help users in finding Viva Sales when interacting with external customer emails, a Microsoft 365 service is used to process incoming emails and provide a notification banner at the top of incoming emails. Banner notifications are displayed only twice in a day. The incoming email must be from an external email domain, or an external email address is included in the **To** or **Cc** field. 
