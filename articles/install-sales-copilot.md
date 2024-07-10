---
title: Install Copilot for Sales (user-deployed)
description: Discover how to install Microsoft Copilot for Sales as a user-deployed app that streamlines and enhances your selling experience.
ms.date: 07/10/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:06/19/2024
---

# Install Copilot for Sales (user-deployed)

Microsoft Copilot for Sales is designed to help sellers work the way they want to without unnecessary context switching and manual data entry. It brings together the applications you work with daily, your CRM, Microsoft 365, and Microsoft Teams, to provide a more streamlined and AI-powered selling experience.


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW181Q6]

## Install Copilot for Sales in Outlook

With Copilot for Sales, you can:

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

**To install Copilot for Sales in Outlook**

1. Sign in to [Microsoft AppSource](https://appsource.microsoft.com/home).

1. Enter **Copilot for Sales** in the **Search** box.

1. From the search results, select **Get it now** on the **Copilot for Sales** app's card.

1. In the **Confirm your details to continue** window, select **Get it now**.

    The app is installed, and a confirmation message is displayed.

> [!NOTE]
> - You can also get the add-in from Office Store within Outlook. More information: [Get an Office Add-in for Outlook](https://support.microsoft.com/office/get-an-office-add-in-for-outlook-1ee261f9-49bf-4ba6-b3e2-2ba7bcab64c8).

### Start using Copilot for Sales in Outlook

After you've installed Copilot for Sales, you can open Copilot for Sales and sign in to your CRM system to start using Copilot for Sales. More information: [Access the Copilot for Sales app](open-app.md)

### Difference between Copilot for Sales and Dynamics 365 app for Outlook

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


## Install Copilot for Sales app in Microsoft Teams

1. Sign in to Microsoft Teams.

1. In the navigation bar on the left, select **Apps**.

	:::image type="content" source="media/store.png" alt-text="Screenshot showing Apps on the navigation bar.":::

1.  Search for **Copilot for Sales**, and then select it.

1.  Select **Add** in the **Copilot for Sales** window.

### Start using Copilot for Sales in Teams

After you've installed Copilot for Sales, you can start using Copilot for Sales to stay connected to your customers, minimize data entry, and personalize your engagements. More information: [Access the Copilot for Sales app](open-app.md)

### Welcome message

Once the Copilot for Sales app is deployed, each user is welcomed by an engaging message from the Copilot for Sales bot in Teams. This message outlines the key capabilities in Copilot for Sales and provides direct links to comprehensive feature documentation and other learning resources.

## FAQ

### How do I know if the Copilot for Sales add-in for Outlook is admin-deployed or user-deployed?

If the Copilot for Sales add-in for Outlook was installed from the Microsoft 365 admin center, it is considered as admin-deployed. If the Copilot for Sales add-in for Outlook was installed automatically for your organization or sellers have installed it themselves, it is considered as user-deployed.

You can check if the Copilot for Sales add-in for Outlook is admin-deployed or user-deployed by following these steps:

1. Open [https://aka.ms/olksideload](https://aka.ms/olksideload). If required, sign in to your Microsoft Outlook account.

2. In the **Add-Ins for Outlook** window, go to **My add-ins** and **Admin-managed** tabs in the left pane, and check if the add-in is available under these tabs.

    If the add-in is available under **Admin-managed** tab, it is admin-deployed. Contact your administrator to [uninstall the add-in](disable-viva-sales.md).

    If the add-in is available under **My add-ins** tab, it is user-deployed. You can [uninstall the add-in](disable-viva-sales.md#uninstall-copilot-for-sales-outlook-add-in) by yourself. If you are unable to uninstall the add-in, contact your administrator.

### See also

[Uninstall Copilot for Sales app](disable-viva-sales.md)