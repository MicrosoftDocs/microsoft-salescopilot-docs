---
title: Install Sales agent
description: Learn what are the various ways to install the Sales agent.
ms.date: 03/09/2026
ms.topic: install-set-up-deploy
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Install Sales agent

The Sales agent can be installed either by an administrator or by an end user. As an administrator, you can install the Sales agent as an integrated app on multiple platforms or as an individual app on a single platform. As an end user, you can install the Outlook add-in and Teams app from within Microsoft Marketplace in Outlook or Teams respectively, as long as they aren't explicitly blocked by your administrator. For information about privileges required to use the Sales agent, see [Privileges required to use the Sales agent](privileges.md).

## Admin-deployed installation

You can install the Sales agent as an integrated app on multiple platforms or as an individual app on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft Marketplace to install it in Outlook and assign users. If you start from Marketplace, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator installs it for best performance and usability.  

Additionally, to install the app within Teams, you need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Sales agent for Teams from Marketplace, you'll install it to your personal scope only, not for your users.

You need to be a Microsoft 365 administrator to deploy and install the Sales agent for Outlook and Microsoft 365 apps. You need to be a Teams administrator to deploy and install the Sales agent for Teams.

For steps to install the Sales agent in Outlook and Teams, see [Install the Sales agent in Outlook](install-sales-as-an-integrated-app.md) and [Install and pin the Sales agent in Teams](install-pin-sales-teams.md).

> [!NOTE]
> If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce. If it's blocked, you need to unblock it to use the Sales agent and might take up to 24 hours for the add-in to show up for your users.

## User-deployed installation

As an end user, you can install the Outlook add-in and Teams app from within Microsoft Marketplace in Outlook or Teams respectively, as long as they aren't explicitly blocked by your administrator. 

When you install the Outlook add-in, it's considered user-deployed instead of admin-deployed and will not have full feature support. User-deployed add-ins don't support the Sales agent banner notifications that appear within the top of new or reply emails. Also, the Sales agent is not added automatically to meeting invites. However, you can manually add the Sales agent to the meeting to get meeting summaries.

> [!IMPORTANT]
>
> - This article provides instructions for business users without administrator privileges to install the Sales agent. If you are a CRM administrator trying to install the Sales agent for your sales team, see [Sales agent deployment guide for Dynamics 365 customers](deploy-sales-app-d365.md) or [Sales agent deployment guide for Salesforce customers](deploy-sales-app-sf.md) as per your requirement.
> - You may not be able to install the Sales agent if downloading add-ins is turned off for your organization. In this case, contact your administrator.
> - If you are using the Dynamics 365 app for Outlook, you can consider switching to the Sales agent, as you can do much more with the Sales agent. More information: [Difference between the Sales agent and Dynamics 365 app for Outlook](#difference-between-sales-agent-and-dynamics-365-app-for-outlook)

### Install Sales agent in Outlook

1. Sign in to [Microsoft Marketplace](https://marketplace.microsoft.com/home).

1. Enter **Sales** in the **Search** box.

1. From the search results, select **Get it now** on the **Sales** card.

1. In the **Confirm your details to continue** window, select **Get it now**.

    The app is installed, and a confirmation message is displayed.

> [!NOTE]
> You can also get the add-in from Office Store within Outlook. More information: [Get an Office Add-in for Outlook](https://support.microsoft.com/office/get-an-office-add-in-for-outlook-1ee261f9-49bf-4ba6-b3e2-2ba7bcab64c8).

#### Difference between Sales agent and Dynamics 365 app for Outlook

| Capability | Sales agent | Dynamics 365 app for Outlook |
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
| ¹ The Sales agent supports connecting Microsoft Outlook activities to accounts and opportunities. Support for connecting Outlook activities to other entities is coming soon. | | |
| ² The Sales agent allows creating contacts and editing contacts, accounts, and opportunities. Support for creating and editing additional entities is coming soon. | | |
|³ Requires the Sales agent to be installed in Microsoft Teams.  |               |                              |      

### Install Sales agent in Microsoft Teams

1. Sign in to Microsoft Teams.  
1. In the navigation bar on the left, select **Apps**.

    :::image type="content" source="media/store.png" alt-text="Screenshot showing Apps on the navigation bar.":::

1. Search for **Sales**, and then select it.  
1. Select **Add** in the **Sales** window.

### Welcome message

Once the Sales agent is deployed, each user is welcomed by an engaging message from the Sales bot in Teams. This message outlines the key capabilities in the Sales agent and provides direct links to comprehensive feature documentation and other learning resources.

## How to use Sales agent?

After the Sales agent is installed, you can start using it in Outlook and Teams. For information on how to use the Sales agent, see [Access the Sales agent](open-app.md).

### Related information

[Install Sales agent in Outlook](install-sales-as-an-integrated-app.md)<br>
[Install and pin Sales agent in Teams](install-pin-sales-teams.md)<br>
[Privileges required to use Sales agent](privileges.md)
