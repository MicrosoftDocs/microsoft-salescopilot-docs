---
title: Install Copilot for Sales (user-deployed)
description: Learn how to install Copilot for Sales.
ms.date: 01/09/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Install Copilot for Sales (user-deployed)

Microsoft Copilot for Sales is designed to help sellers work the way they want to without unnecessary context switching and manual data entry. It brings together the applications you work with daily, your CRM, Microsoft 365, and Microsoft Teams, to provide a more streamlined and AI-powered selling experience.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW181Q6]

## Install Copilot for Sales add-in for Outlook

With Copilot for Sales for Microsoft Outlook, you can:

- Reply quickly and confidently with assistance from AI

- Save Outlook emails and events to Dynamics 365

- Connect Outlook emails and events to relevant Dynamics 365 records

- Create new contacts in Dynamics 365 from Outlook

- Update opportunities, accounts and contacts in Dynamics 365 from Outlook

>
> [!IMPORTANT]
> - This article provides instructions for business users without administrator privileges to install Copilot for Sales. If you are a CRM administrator trying to install Copilot for Sales for your sales team, see [Copilot for Sales deployment guide for Dynamics 365 customers](deploy-viva-sales-d365.md) or [Copilot for Sales deployment guide for Salesforce customers](deploy-viva-sales-sf.md) as per your requirement.
> - When you install the Outlook add-in, it's considered user-deployed instead of admin-deployed and will not have full feature support. User-deployed add-ins don't support Copilot for Sales banner notifications that appear within the top of new or reply emails. Also, the Copilot for Sales app is not added automatically to meeting invites. However, you can manually add Copilot for Sales to the meeting to get meeting summaries.
> - You may not be able to install Copilot for Sales if downloading add-ins is turned off for your organization. In this case, contact your administrator.
> - If you are using the Dynamics 365 app for Outlook, you can consider switching to Copilot for Sales, as you can do much more with Copilot for Sales. More information: [Difference between Copilot for Sales and Dynamics 365 app for Outlook](#difference-between-copilot-for-sales-and-dynamics-365-app-for-outlook)

### Install Copilot for Sales Outlook add-in from AppSource

1. Sign in to [Microsoft AppSource](https://appsource.microsoft.com/home).

1. Enter **Copilot for Sales** in the **Search** box.

1. From the search results, select **Get it now** on the **Copilot for Sales for Microsoft Outlook** app's card.

1. In the **Confirm your details to continue** window, select **Get it now**.

    The app is installed, and a confirmation message is displayed.

> [!NOTE]
> You can also get the add-in from Office Store within Outlook. More information: [Get an Office Add-in for Outlook](https://support.microsoft.com/office/get-an-office-add-in-for-outlook-1ee261f9-49bf-4ba6-b3e2-2ba7bcab64c8).

### Start using Copilot for Sales in Outlook

After you've installed Copilot for Sales, you can open Copilot for Sales and sign in to your CRM system to start using Copilot for Sales. More information: [Use Copilot for Sales in Outlook](use-sales-copilot-outlook.md)

### Difference between Copilot for Sales and Dynamics 365 app for Outlook

| Capability | Copilot for Sales | Dynamics 365 app for Outlook |
|------------|---------------|------------------------------|
| **Work in Outlook**        |               |              | 
| Intelligent context-aware email content suggestions with copilot  | Supported    | Not supported          |
| Save Outlook emails and calendar events to Dynamics 365   | Supported     | Supported       |
| Connect saved Outlook emails and events to Dynamics 365 accounts and opportunities  | Supported¹    | Supported      |
| Create new CRM contacts from Outlook   | Supported     | Supported    |
| Automatically capture email signature and suggest updating CRM   | Supported     | Not supported                |
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


### Uninstall Copilot for Sales Outlook add-in

1. Open [https://aka.ms/olksideload](https://aka.ms/olksideload). If required, sign in to your Microsoft Outlook account.

1. In the **Add-Ins for Outlook** window, select **My add-ins** in the left pane.

1. On the **Copilot for Sales for Microsoft Outlook** card, select **Manage Add-In** (**...**) at the bottom-right, and then select **Remove**.

    :::image type="content" source="media/uninstall add-in.png" alt-text="Uninstall Copilot for Sales Outlook add-in.":::

> [!NOTE]
> If there's no option to uninstall the add-in, it's likely that the add-in was installed by your administrator. Contact your administrator to uninstall the add-in. To know if the add-in is admin-deployed or user-deployed, see [How do I know if the Copilot for Sales add-in for Outlook is admin-deployed or user-deployed?](#how-do-i-know-if-the-copilot-for-sales-add-in-for-outlook-is-admin-deployed-or-user-deployed).

## Install Copilot for Sales app for Microsoft Teams

1. Sign in to Microsoft Teams.

1. In the navigation bar on the left, select **Store**.

	:::image type="content" source="media/store.png" alt-text="Screenshot showing select store on the navigation bar.":::

1.  Search for **Copilot for Sales**, and then select it.

1.  Select **Add** in the **Copilot for Sales** window.

	:::image type="content" source="media/add-sales-copilot.png" alt-text="Screenshot showing add Copilot for Sales app.":::

### Start using Copilot for Sales in Teams

After you've installed Copilot for Sales, you can start using Copilot for Sales to stay connected to your customers, minimize data entry, and personalize your engagements. More information: [Use Copilot for Sales in Teams](use-sales-copilot-teams.md)

### Uninstall Copilot for Sales app for Microsoft Teams

1. Sign in to Microsoft Teams.

1. In the navigation bar on the left, select **Store**.

1. At the bottom of the **Apps** sidebar, select **Manage your apps**.

1. Find the Copilot for Sales app and select it to expand its row.

1. Select **Remove** :::image type="content" source="media/trash.png" alt-text="Delete team trash can button."::: for the personal app and confirm you want to remove the app from the selected location.

## FAQ

### How do I know if the Copilot for Sales add-in for Outlook is admin-deployed or user-deployed?

If the Copilot for Sales add-in for Outlook was installed from the Microsoft 365 admin center, it is considered as admin-deployed. If the Copilot for Sales add-in for Outlook was installed automatically for your organization or sellers have installed it themselves, it is considered as user-deployed.

You can check if the Copilot for Sales add-in for Outlook is admin-deployed or user-deployed by following these steps:

1. Open [https://aka.ms/olksideload](https://aka.ms/olksideload). If required, sign in to your Microsoft Outlook account.

2. In the **Add-Ins for Outlook** window, go to **My add-ins** and **Admin-managed** tabs in the left pane, and check if the add-in is available under these tabs.

    If the add-in is available under **Admin-managed** tab, it is admin-deployed. Contact your administrator to [uninstall the add-in](disable-viva-sales.md).

    If the add-in is available under **My add-ins** tab, it is user-deployed. You can [uninstall the add-in](#uninstall-copilot-for-sales-outlook-add-in) by yourself. If you are unable to uninstall the add-in, contact your administrator.