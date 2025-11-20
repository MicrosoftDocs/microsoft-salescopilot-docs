---
title: Mobile support for Sales in Microsoft 365 Copilot (preview)
description: Learn about the mobile support for Sales in Microsoft 365 Copilot on iOS and Android versions of Outlook and Teams, including supported and unsupported features.
ms.date: 07/29/2025
ms.topic: concept-article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom: CXT
---

# Mobile support for Sales in Microsoft 365 Copilot (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Sales in Microsoft 365 Copilot is supported on mobile (iOS and Android) versions of Outlook and Teams. All the features available in the desktop version of Sales in Microsoft 365 Copilot aren't available in the mobile version. This article outlines what is and isn't supported on mobile.

> [!NOTE]
> During the preview, if Sales app was deployed to your organization before mobile support, you must redeploy the app from the Microsoft 365 admin center. In the admin center, find the existing Sales integrated app and remove it. Then redeploy the app by following the instructions in the [Install Sales app](install-sales-app.md) article.

## Outlook experience

You can access the Sales app only when reading emails. It's not available when composing or replying to emails or when viewing or creating a meeting or appointment.

To open Sales app, select an email on your mobile device, and then select **...**  next to the email from and to fields. Select **Sales** from the top app list or find it under **More Add-Ins**. When the app is launched, it takes over the full screen due to the smaller mobile screen.

:::image type="content" source="media/open-mobile-app-outlook.png" alt-text="Screenshot of Sales app opened in Outlook mobile app.":::

### Supported features

All features available in the desktop version of Sales app work on mobile (unless called out in the known issues section) including the following features:

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
- The **Saved to Salesforce** tag isn't displayed in iOS. When an email is saved to CRM using Sales app, two different tags are generated based on the CRM you're signed in to. The **Tracked to Dynamics 365** tag is displayed when signed in to Dynamics 365 and the **Saved to Salesforce** tag is displayed when signed in to Salesforce. Both the tags are displayed in the desktop and web versions of Outlook. However, only the **Tracked to Dynamics 365** tag is displayed in iOS. 
- The Sales app doesn't appear when signed in to multiple accounts in Outlook. Ensure your primary account is used with Copilot.

## Teams experience

Sales app in Teams has mixed support on Teams mobile version.

### Supported features

- Message extension to share CRM records within chats and Team conversations.
- Share Sales app CRM record links in conversations. The records links unfurl into rich adaptive cards.
- Bot notifications including reading preparation cards.

### Unsupported features

- The Sales tab with meeting recap, mentions, and details is only available on larger screens.
- The Sales pill within the Teams recap isn't available on Teams mobile for post-meeting information.

## Shared Microsoft 365 experience

The Sales personal app can be accessed from both Outlook and Teams mobile apps via **Apps** button in the bottom navigation bar.

The personal app includes **Home** and **Settings** tabs. The **Settings** tab is only available to CRM or system administrators. Learn more at [Sales personal app](personal-app.md).

:::image type="content" source="media/open-personal-app-mobile.png" alt-text="Screenshot for Sales personal app opened in Outlook mobile app.":::

### Related information

- [Buy Sales](buy-license.md)<br>
- [Install Sales app](install-sales-app.md)
