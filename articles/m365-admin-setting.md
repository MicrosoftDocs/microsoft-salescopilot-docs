---
title: Turn off actionable banners in Microsoft 365 apps
description: Learn how to turn off actionable banners in Microsoft 365 apps.
ms.date: 06/26/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/28/2023
  - bap-template
---

# Turn off actionable banners in Microsoft 365 apps

Some Copilot for Sales features run in Microsoft 365 app service apart from the Outlook add-in and Teams app. These features are turned on by default. Tenant administrators can turn them off in the Microsoft 365 admin center.

1. Sign in to the Microsoft 365 admin center with your tenant admin credentials.  
1. Select **Settings** > **Org settings**.  
1. On the **Org settings** page, in the **Services** tab, select **Copilot for Sales**.  
1. Clear **Allow users to see Copilot for Sales content in Microsoft 365 apps**.  
1. Select **Save**.

## Effect on the Copilot for Sales email notification banner

To help users find Copilot for Sales when they interact with customer emails, a Microsoft 365 service adds a notification banner at the top of incoming messages when the message is from an external email domain or an external email address is included in the **To** or **Cc** field. Banner notifications are displayed on a limited number of emails per day.  
If you turn off actionable banners in Microsoft 365 apps, banner notifications aren't removed from emails that are already in users' Inboxes. However, no new incoming emails display the banner until you turn the setting on again.
