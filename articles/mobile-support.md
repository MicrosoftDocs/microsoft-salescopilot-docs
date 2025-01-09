---
title: Mobile support for Copilot for Sales (preview)
description: Copilot for Sales is supported on mobile (iOS and Android) versions of Outlook and Teams. This article outlines what is and is not supported on mobile.
ms.date: 01/10/2025
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Mobile support for Copilot for Sales (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Copilot for Sales is supported on mobile (iOS and Android) versions of Outlook and Teams. All the features available in the desktop version of Copilot for Sales are not available in the mobile version. This article outlines what is and is not supported on mobile.

> [!NOTE]
> During the preview, if Copilot for Sales was deployed to your organization prior to the mobile support, you must redeploy the app from the Microsoft 365 admin center. In the Microsoft 365 admin center, find the existing Copilot for Sales integrated app and remove it. You can then redeploy the app by following the instructions in the [Install Copilot for Sales](install-viva-sales.md) article.

## Outlook experience

You can access the Copilot for Sales app only when reading emails. It's not available when composing or replying to emails. It's also not available when viewing or creating a meeting or appointment.

To open Copilot for Sales, select an email on your mobile device, and then select **...**  next to the email from and to fields. Select Copilot for Sales from the top app list or find it under **More Add-Ins**. When the app is launched, it takes over the full screen due to the smaller mobile screen.

### Supported features

All features available in the desktop version of Copilot for Sales will work on mobile (unless called out in the known issues section) including the following:

- Add or edit CRM records such as contacts, accounts, and opportunities.
- Search for and view CRM records.
- Save emails to CRM.
- View AI-generated email summaries.
- Generate email drafts that can be copied into an email reply.
- View AI-generated opportunity summaries.

### Unsupported features

- Salesforce login is not supported in iOS. As a workaround, you can sign in from the desktop or web version of Outlook and then the mobile version will work.
- Copilot for Sales Outlook app does not load with RTL languages. This is a known issue and no workaround is available at this time.
- When selecting the **Open in Salesforce** link, the home page opens in the browser and not the record page. Salesforce links do not work on mobile browsers. However, if you have the Salesforce mobile app installed, the record page will open in the Salesforce app in iOS and Android.
- The **Saved to CRM** tag is not displayed in Android for emails already saved to CRM. This is a known Android platform limitation that email categorization feature does not work.
- The **Saved to Salesforce** tag is not displayed in iOS. When an email is saved to CRM using Copilot for Sales, two different tags are generated based on the CRM you are signed in to. The **Tracked to Dynamics 365** tag is displayed when signed in to Dynamics 365 and the **Saved to Salesforce** tag is displayed when signed in to Salesforce. Both the tags are displayed in the desktop and web versions of Outlook. However, only the **Tracked to Dynamics 365** tag is displayed in iOS. 
- The Copilot for Sales app does not appear when signed in to multiple accounts in Outlook. Ensure that the account you are using with Copilot for Sales app is the primary account in Outlook.

## Teams experience

Copilot for Sales Teams app has mixed support on Teams mobile version.

### Supported features

- Message extension to share CRM records within chats and Team conversations.
- Share Copilot for Sales CRM record links in conversations. The records links will unfurl into rich adaptive cards.
- Bot notifications including reading preparation cards.

### Unsupported features

- The Sales tab with meeting recap, mentions, and details is only available on larger screens.
- The Sales pill within the Teams recap is not available on Teams mobile to see post meeting information.

## Shared Microsoft 365 experience

The Copilot for Sales personal app can be accessed from both Outlook and Teams mobile apps. You can access the app from the Apps button in the bottom navigation bar in Outlook and Teams mobile apps.

The Copilot for Sales personal app includes **Home** and **Settings** tabs. Settings are available only for CRM or system administrators. For more information about the personal app, see [Microsoft 365 Copilot for Sales personal app](personal-app.md).

### Related information

[Buy Microsoft 365 Copilot for Sales](buy-license.md)<br>
[Install Copilot for Sales](install-viva-sales.md)