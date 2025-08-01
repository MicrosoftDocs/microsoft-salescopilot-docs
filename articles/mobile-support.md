---
title: Mobile support for Copilot for Sales (preview)
description: Learn about the mobile support for Copilot for Sales on iOS and Android versions of Outlook and Teams, including supported and unsupported features.
ms.date: 07/29/2025
ms.topic: concept-article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom: CXT
---

# Mobile support for Copilot for Sales (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Copilot for Sales is supported on mobile (iOS and Android) versions of Outlook and Teams. All the features available in the desktop version of Copilot for Sales aren't available in the mobile version. This article outlines what is and isn't supported on mobile.

> [!NOTE]
> During the preview, if Copilot for Sales was deployed to your organization before mobile support, you must redeploy the app from the Microsoft 365 admin center. In the admin center, find the existing Copilot for Sales integrated app and remove it. Then redeploy the app by following the instructions in the [Install Copilot for Sales](install-viva-sales.md) article.

Here's a video that provides an overview of Copilot for Sales on mobile devices:

> [!VIDEO d4240ff0-fcfa-47b7-8bd5-61ab0f2d714f]

## Outlook experience

You can access the Copilot for Sales app only when reading emails. It's not available when composing or replying to emails or when viewing or creating a meeting or appointment.

To open Copilot for Sales, select an email on your mobile device, and then select **...**  next to the email from and to fields. Select Copilot for Sales from the top app list or find it under **More Add-Ins**. When the app is launched, it takes over the full screen due to the smaller mobile screen.

:::image type="content" source="media/open-mobile-app-outlook.png" alt-text="Screenshot of Copilot for Sales opened in Outlook mobile app.":::

### Supported features

All features available in the desktop version of Copilot for Sales work on mobile (unless called out in the known issues section) including the following features:

- Add or edit CRM records such as contacts, accounts, and opportunities.
- Search for and view CRM records.
- Save emails to CRM.
- View AI-generated email summaries.
- Generate email drafts that can be copied into an email reply.
- View AI-generated opportunity summaries.

### Unsupported features

- Salesforce sign-in isn't supported in iOS. As a workaround, sign in from the desktop or web version of Outlook and then use the mobile version.
- Selecting **Open in Salesforce** opens the home page in a browser instead of the record page. Salesforce links don't work on mobile browsers. However, if you have the Salesforce mobile app installed, the record page opens in the Salesforce app in iOS and Android.
- The **Saved to CRM** tag isn't displayed in Android for emails already saved to CRM due to platform limitations with email categorization.
- The **Saved to Salesforce** tag isn't displayed in iOS. When an email is saved to CRM using Copilot for Sales, two different tags are generated based on the CRM you're signed in to. The **Tracked to Dynamics 365** tag is displayed when signed in to Dynamics 365 and the **Saved to Salesforce** tag is displayed when signed in to Salesforce. Both the tags are displayed in the desktop and web versions of Outlook. However, only the **Tracked to Dynamics 365** tag is displayed in iOS. 
- The Copilot for Sales app doesn't appear when signed in to multiple accounts in Outlook. Ensure your primary account is used with Copilot.

## Teams experience

Copilot for Sales Teams app has mixed support on Teams mobile version.

### Supported features

- Message extension to share CRM records within chats and Team conversations.
- Share Copilot for Sales CRM record links in conversations. The records links unfurl into rich adaptive cards.
- Bot notifications including reading preparation cards.

### Unsupported features

- The Sales tab with meeting recap, mentions, and details is only available on larger screens.
- The Sales pill within the Teams recap isn't available on Teams mobile for post-meeting information.

## Shared Microsoft 365 experience

The Copilot for Sales personal app can be accessed from both Outlook and Teams mobile apps via **Apps** button in the bottom navigation bar.

The personal app includes **Home** and **Settings** tabs. The **Settings** tab is only available to CRM or system administrators. Learn more at [Microsoft 365 Copilot for Sales personal app](personal-app.md).

:::image type="content" source="media/open-personal-app-mobile.png" alt-text="Screenshot for Copilot for Sales personal app opened in Outlook mobile app.":::

### Related information

- [Buy Microsoft 365 Copilot for Sales](buy-license.md)<br>
- [Install Copilot for Sales](install-viva-sales.md)
