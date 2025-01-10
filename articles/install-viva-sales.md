---
title: Install Microsoft 365 Copilot for Sales
description: Learn what are the various ways to install Copilot for Sales
ms.date: 01/10/2025
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Install Microsoft 365 Copilot for Sales

Copilot for Sales can be installed either by an administrator or by an end user. As an administrator, you can install Copilot for Sales as an integrated app on multiple platforms or as an individual app on a single platform. As an end user, you can install the Outlook add-in and Teams app from within Microsoft AppSource in Outlook or Teams respectively, as long as they aren't explicitly blocked by your administrator. For information about privileges required to use Copilot for Sales, see [Privileges required to use Copilot for Sales](privileges.md).

## Admin-deployed installation

You can install Copilot for Sales as an integrated app on multiple platforms or as an individual app on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft AppSource to install it in Outlook and assign users. If you start from AppSource, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator installs it for best performance and usability.  

Additionally, to install the app within Teams, you need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Copilot for Sales app for Teams from AppSource, you'll install it to your personal scope only, not for your users.

You need to be a Microsoft 365 administrator to deploy and install the Copilot for Sales add-in for Outlook and Microsoft 365 apps. You need to be a Teams administrator to deploy and install Copilot for Sales for Teams.

For steps to install Copilot for Sales in Outlook and Teams, see [Install Copilot for Sales in Outlook](install-viva-sales-as-an-integrated-app.md) and [Install and pin Copilot for Sales in Teams](install-pin-viva-sales-teams.md).

> [!NOTE]
> If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce. If it's blocked, you need to unblock it to use Copilot for Sales and might take up to 24 hours for the add-in to show up for your users.

Watch this video to learn how to install Copilot for Sales in Outlook and Teams:

> [!VIDEO da2701bb-06f0-49e0-b757-80c584af69f7]

## User-deployed installation

As an end user, you can install the Outlook add-in and Teams app from within Microsoft AppSource in Outlook or Teams respectively, as long as they aren't explicitly blocked by your administrator. 

When you install the Outlook add-in, it's considered user-deployed instead of admin-deployed and will not have full feature support. User-deployed add-ins don't support Copilot for Sales banner notifications that appear within the top of new or reply emails. Also, the Copilot for Sales app is not added automatically to meeting invites. However, you can manually add Copilot for Sales to the meeting to get meeting summaries.

Watch this video to learn more about Copilot for Sales:

> [!VIDEO e7eb1248-4d7f-464b-896c-70f47e6e7fdf]

> [!IMPORTANT]
>
> - This article provides instructions for business users without administrator privileges to install Copilot for Sales. If you are a CRM administrator trying to install Copilot for Sales for your sales team, see [Copilot for Sales deployment guide for Dynamics 365 customers](deploy-viva-sales-d365.md) or [Copilot for Sales deployment guide for Salesforce customers](deploy-viva-sales-sf.md) as per your requirement.
> - You may not be able to install Copilot for Sales if downloading add-ins is turned off for your organization. In this case, contact your administrator.
> - If you are using the Dynamics 365 app for Outlook, you can consider switching to Copilot for Sales, as you can do much more with Copilot for Sales. More information: [Difference between Copilot for Sales and Dynamics 365 app for Outlook](#difference-between-copilot-for-sales-and-dynamics-365-app-for-outlook)

### Install Copilot for Sales in Outlook

1. Sign in to [Microsoft AppSource](https://appsource.microsoft.com/home).

1. Enter **Copilot for Sales** in the **Search** box.

1. From the search results, select **Get it now** on the **Copilot for Sales** app's card.

1. In the **Confirm your details to continue** window, select **Get it now**.

    The app is installed, and a confirmation message is displayed.

> [!NOTE]
> You can also get the add-in from Office Store within Outlook. More information: [Get an Office Add-in for Outlook](https://support.microsoft.com/office/get-an-office-add-in-for-outlook-1ee261f9-49bf-4ba6-b3e2-2ba7bcab64c8).

#### Difference between Copilot for Sales and Dynamics 365 app for Outlook

| Capability | Copilot for Sales | Dynamics 365 app for Outlook |
|------------|---------------|------------------------------|
| **Work in Outlook**        |               |              | 
| Intelligent context-aware email content suggestions with copilot  | Supported    | Not supported          |
| Save Outlook emails and calendar events to Dynamics 365   | Supported     | Supported       |
| Connect saved Outlook emails and events to Dynamics 365 accounts and opportunities  | Supported¹    | Supported      |
| Create new CRM contacts from Outlook   | Supported     | Supported    |
| Automatically capture email signature during new contact creation | Supported     | Not supported                |
| Create and edit non-contact records in Dynamics 365     | Supported²    | Supported      |
| Delegate access (allow a user to act on behalf of another user)    | Not supported | Supported    |
| Mobile support | Not supported | Supported |
| **Work in Teams³**   |               |               |
| Collaborate on customer records with colleagues in Teams    | Supported     | Not supported    |
| Post-meeting: Play back and transcript with highlights, topics, executive summary, action items, and sentiment analysis  | Supported     | Not supported    |
| Mobile support | Supported | Supported |
| ¹ Copilot for Sales supports connecting Microsoft Outlook activities to accounts and opportunities. Support for connecting Outlook activities to other entities is coming soon. | | |
| ² Copilot for Sales allows creating contacts and editing contacts, accounts, and opportunities. Support for creating and editing additional entities is coming soon. | | |
|³ Requires Copilot for Sales app to be installed in Microsoft Teams.  |               |                              |      

### Install Copilot for Sales app in Microsoft Teams

1. Sign in to Microsoft Teams.  
1. In the navigation bar on the left, select **Apps**.

    :::image type="content" source="media/store.png" alt-text="Screenshot showing Apps on the navigation bar.":::

1. Search for **Copilot for Sales**, and then select it.  
1. Select **Add** in the **Copilot for Sales** window.

### Welcome message

Once the Copilot for Sales app is deployed, each user is welcomed by an engaging message from the Copilot for Sales bot in Teams. This message outlines the key capabilities in Copilot for Sales and provides direct links to comprehensive feature documentation and other learning resources.

## How to use Copilot for Sales?

After Copilot for Sales is installed, you can start using it in Outlook and Teams. For information on how to use Copilot for Sales, see [Access the Copilot for Sales app](open-app.md).

### Related information

[Install Copilot for Sales in Outlook](install-viva-sales-as-an-integrated-app.md)<br>  
[Install and pin Copilot for Sales in Teams](install-pin-viva-sales-teams.md)<br>
[Privileges required to use Copilot for Sales](privileges.md)
