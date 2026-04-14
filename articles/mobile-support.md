---
title: Mobile support for Sales agent
description: Learn about the mobile support for Sales agent on iOS and Android versions of Outlook and Teams, including supported and unsupported features.
ms.date: 03/09/2026
ms.topic: concept-article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom: CXT
---

# Mobile support for Sales agent

Sales agent is supported on mobile (iOS and Android) versions of Outlook and Teams. All the features available in the desktop version of Sales agent aren't available in the mobile version. This article outlines what is and isn't supported on mobile.

## Sales agent chat on mobile

You can use Sales agent chat on mobile in either of these ways:

- Launch from **Outlook mobile** by tapping the **Copilot** icon, and then selecting **Sales** from the hamburger menu.
- Launch from the standalone **Microsoft 365 Copilot** app by selecting **Sales** from the hamburger menu.

### Chat capabilities

When launched from either entry point, Sales agent chat helps you:

- Search for and view CRM records.
- Add or update CRM records such as contacts, accounts, and opportunities.
- Summarize email context and generate draft responses.
- Capture notes and save them to CRM.

Learn more about using [Sales agent chat capabilities](use-sales-chat.md).

## Capture voice notes and save to CRM

You can capture voice notes in Sales agent using the Microsoft 365 Copilot app and save them directly to your CRM records. You can launch the app from within Outlook mobile or use the Microsoft 365 Copilot app as a standalone app.

This is useful when you want to log call notes, meeting takeaways, or account updates while on the go without typing.

You can capture voice notes in either of these ways:

- **From Outlook mobile**: Launch the Microsoft 365 Copilot app and use your device's keyboard dictation to speak your notes in the Sales agent chat.
- **From the Microsoft 365 Copilot app**: Use the built-in mic icon in the Sales agent chat to record your note.

> [!NOTE]
> This feature is available on both iOS and Android.

### Capture voice notes in Outlook mobile

When you launch Sales agent from Outlook mobile, use your device's keyboard dictation to capture voice notes. The dictated text appears in the Sales agent chat and can then be saved to a CRM record.

1. Open Outlook on your mobile device and tap the **Copilot** icon.
1. Select the hamburger menu on the top left, and then select **Sales**.
1. In the Sales agent chat, tap the message input box to bring up the keyboard.
1. On your keyboard, select the microphone key and speak your note.
   The dictated text appears in the message input box as you speak.
1. Review the transcribed text and make any edits if needed.
1. Send the message to the Sales agent.
1. When prompted, select the CRM record where you want to save the note, and then confirm.


### Capture voice notes in the Microsoft 365 Copilot app

In the Microsoft 365 Copilot app, use the built-in **Mic** icon in the Sales agent chat to capture voice notes directly.

1. Open the Microsoft 365 Copilot app on your mobile device.
1. Select the hamburger menu on the top left, and then select **Sales**.
1. In the chat input area, tap the **Mic** icon and speak your note.
   The transcribed text appears in the message input box.
1. Review the transcribed text and make any edits if needed.
1. Send the message to the Sales agent.
1. When prompted, select the CRM record where you want to save the note, and then confirm.

## Sales agent app on mobile

### Outlook experience

You can access the Sales agent only when reading emails. It's not available when composing or replying to emails or when viewing or creating a meeting or appointment.

To open the Sales agent, select an email on your mobile device, and then select **...**  next to the email from and to fields. Select **Sales** from the top app list or find it under **More Add-Ins**. When the app is launched, it takes over the full screen due to the smaller mobile screen.

:::image type="content" source="media/open-mobile-app-outlook.png" alt-text="Screenshot of the Sales agent opened in Outlook mobile app.":::

#### Supported features

All features available in the desktop version of the Sales agent work on mobile (unless called out in the known issues section) including the following features:

- Add or edit CRM records such as contacts, accounts, and opportunities.
- Search for and view CRM records.
- Save emails to CRM.
- View AI-generated email summaries.
- Generate email drafts that can be copied into an email reply.
- View AI-generated opportunity summaries.

#### Unsupported features

- Salesforce sign-in isn't supported in iOS. As a workaround, sign in from the desktop or web version of Outlook and then use the mobile version.
- Selecting **Open in Salesforce** opens the home page in a browser instead of the record page. Salesforce links don't work on mobile browsers. However, if you have the Salesforce mobile app installed, the record page opens in the Salesforce app in iOS and Android.
- The **Saved to CRM** tag isn't displayed in Android for emails already saved to CRM due to platform limitations with email categorization.
- The **Saved to Salesforce** tag isn't displayed in iOS. When an email is saved to CRM using the Sales agent, two different tags are generated based on the CRM you're signed in to. The **Tracked to Dynamics 365** tag is displayed when signed in to Dynamics 365 and the **Saved to Salesforce** tag is displayed when signed in to Salesforce. Both the tags are displayed in the desktop and web versions of Outlook. However, only the **Tracked to Dynamics 365** tag is displayed in iOS. 
- The Sales agent doesn't appear when signed in to multiple accounts in Outlook. Ensure your primary account is used with Copilot.

### Teams experience

The Sales agent in Teams has mixed support on Teams mobile version.

#### Supported features

- Message extension to share CRM records within chats and Team conversations.
- Share the Sales agent CRM record links in conversations. The records links unfurl into rich adaptive cards.
- Bot notifications including reading preparation cards.

#### Unsupported features

- The Sales tab with meeting recap, mentions, and details is only available on larger screens.
- The Sales pill within the Teams recap isn't available on Teams mobile for post-meeting information.

### Shared Microsoft 365 experience

The Sales personal app can be accessed from both Outlook and Teams mobile apps via **Apps** button in the bottom navigation bar.

The personal app includes **Home** and **Settings** tabs. The **Settings** tab is only available to CRM or system administrators. Learn more at [Sales personal app](personal-app.md).

:::image type="content" source="media/open-personal-app-mobile.png" alt-text="Screenshot for Sales personal app opened in Outlook mobile app.":::


### Related information

- [Buy Sales](buy-license.md)<br>
- [Install the Sales agent](install-sales-app.md)
