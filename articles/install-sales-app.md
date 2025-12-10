---
title: Install Sales app
description: Learn what are the various ways to install the Sales app.
ms.date: 11/20/2025
ms.topic: install-set-up-deploy
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Install Sales app

The Sales app can be installed either by an administrator or by an end user. As an administrator, you can install the Sales app as an integrated app on multiple platforms or as an individual app on a single platform. As an end user, you can install the Outlook add-in and Teams app from within Microsoft AppSource in Outlook or Teams respectively, as long as they aren't explicitly blocked by your administrator. For information about privileges required to use the Sales app, see [Privileges required to use the Sales app](privileges.md).

## Admin-deployed installation

You can install the Sales app as an integrated app on multiple platforms or as an individual app on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft AppSource to install it in Outlook and assign users. If you start from AppSource, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator installs it for best performance and usability.  

Additionally, to install the app within Teams, you need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Sales app for Teams from AppSource, you'll install it to your personal scope only, not for your users.

You need to be a Microsoft 365 administrator to deploy and install the Sales app for Outlook and Microsoft 365 apps. You need to be a Teams administrator to deploy and install the Sales app for Teams.

For steps to install the Sales app in Outlook and Teams, see [Install the Sales app in Outlook](install-sales-as-an-integrated-app.md) and [Install and pin the Sales app in Teams](install-pin-sales-teams.md).

> [!NOTE]
> If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce. If it's blocked, you need to unblock it to use the Sales app and might take up to 24 hours for the add-in to show up for your users.

## User-deployed installation

As an end user, you can install the Outlook add-in and Teams app from within Microsoft AppSource in Outlook or Teams respectively, as long as they aren't explicitly blocked by your administrator. 

When you install the Outlook add-in, it's considered user-deployed instead of admin-deployed and will not have full feature support. User-deployed add-ins don't support the Sales app banner notifications that appear within the top of new or reply emails. Also, the Sales app is not added automatically to meeting invites. However, you can manually add the Sales app to the meeting to get meeting summaries.

> [!IMPORTANT]
>
> - This article provides instructions for business users without administrator privileges to install the Sales app. If you are a CRM administrator trying to install the Sales app for your sales team, see [Sales app deployment guide for Dynamics 365 customers](deploy-sales-app-d365.md) or [Sales app deployment guide for Salesforce customers](deploy-sales-app-sf.md) as per your requirement.
> - You may not be able to install the Sales app if downloading add-ins is turned off for your organization. In this case, contact your administrator.
> - If you are using the Dynamics 365 app for Outlook, you can consider switching to the Sales app, as you can do much more with the Sales app. More information: [Difference between the Sales app and Dynamics 365 app for Outlook](#difference-between-sales-app-and-dynamics-365-app-for-outlook)

### Install Sales app in Outlook

1. Sign in to [Microsoft AppSource](https://appsource.microsoft.com/home).

1. Enter **Sales** in the **Search** box.

1. From the search results, select **Get it now** on the **Sales** app's card.

1. In the **Confirm your details to continue** window, select **Get it now**.

    The app is installed, and a confirmation message is displayed.

> [!NOTE]
> You can also get the add-in from Office Store within Outlook. More information: [Get an Office Add-in for Outlook](https://support.microsoft.com/office/get-an-office-add-in-for-outlook-1ee261f9-49bf-4ba6-b3e2-2ba7bcab64c8).

#### Difference between Sales app and Dynamics 365 app for Outlook

| Capability | the Sales app | Dynamics 365 app for Outlook |
|------------|---------------|------------------------------|
| **Work in Outlook**        |               |              | 
| Intelligent context-aware email content suggestions with Copilot  | Supported    | Not supported          |
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
| ¹ the Sales app supports connecting Microsoft Outlook activities to accounts and opportunities. Support for connecting Outlook activities to other entities is coming soon. | | |
| ² the Sales app allows creating contacts and editing contacts, accounts, and opportunities. Support for creating and editing additional entities is coming soon. | | |
|³ Requires the Sales app to be installed in Microsoft Teams.  |               |                              |      

### Install Sales app in Microsoft Teams

1. Sign in to Microsoft Teams.  
1. In the navigation bar on the left, select **Apps**.

    :::image type="content" source="media/store.png" alt-text="Screenshot showing Apps on the navigation bar.":::

1. Search for **Sales**, and then select it.  
1. Select **Add** in the **Sales** window.

### Welcome message

Once the Sales app is deployed, each user is welcomed by an engaging message from the Sales bot in Teams. This message outlines the key capabilities in the Sales app and provides direct links to comprehensive feature documentation and other learning resources.

## How to use Sales app?

After the Sales app is installed, you can start using it in Outlook and Teams. For information on how to use the Sales app, see [Access the Sales app](open-app.md).

### Related information

[Install Sales app in Outlook](install-sales-as-an-integrated-app.md)<br>
[Install and pin Sales app in Teams](install-pin-sales-teams.md)<br>
[Privileges required to use Sales app](privileges.md)
