---
title: What's changed with Sales Copilot to Copilot for Sales
description: Revamped Sales Copilot, now called Microsoft 365 Copilot for Sales, merges features and improves user experience.
ms.date: 09/25/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:01/23/2024
---

# What's changed with Sales Copilot to Microsoft 365 Copilot for Sales

On February 1, 2024, Sales Copilot updated to bring the power of Microsoft 365 Copilot and the role specific insights and actions together under a new offering called Microsoft 365 Copilot for Sales. As part of the effort, we're excited to bring the following updates:

- **New user experience**: The **Highlights** and CRM tabs are merged into one unified view.
- **License changes**: A new Microsoft 365 Copilot for Sales license is introduced, which includes Microsoft 365 Copilot subscription.
- **Enhanced Teams app**: The existing Sales Copilot Teams app and Outlook add-in have been upgraded to a single enhanced Teams app. 
- **Better together experience**: : Copilot for Sales combines the power of your CRM application with Microsoft 365 Copilot. It provides an AI-optimized out of the box experience that has been enriched with role specific insights and recommendations. 

## New user experience

The new user experience brings the **Highlights** and CRM tabs together into one unified view and combines the data to make a single enriched result. The new view is designed to provide a more streamlined experience by bringing the most relevant information to the top of the view. For information about the new user experience, go to [Copilot for Sales license](#copilot-for-sales-license).

## License changes

Customers must purchase Copilot for Sales licenses, as Sales Copilot is no longer available. For information on Copilot for Sales pricing and licensing guidance, view the [licensing and pricing pages](https://www.microsoft.com/en-us/microsoft-365/copilot/copilot-for-sales#Pricing). 

### Existing Sales Copilot license

Existing customers with the Sales Copilot licenses will continue to see a subset of functionality until moving to Copilot for Sales. For information about limited features, see [Copilot for Sales features for Dynamics 365 Sales users](features-d365-users.md).

### Copilot for Sales license

The Copilot for Sales license includes the Microsoft 365 Copilot subscription. In this license, you can expect to see an integrated experience combining the value of Microsoft 365 Copilot and the role-based sales insights with out of the box CRM integration as part of the core package. Email summary and generative replies are integrated into Outlook as part of the Microsoft 365 Copilot experience. If you're using the Outlook on the web or the new Outlook for Windows, you can access Copilot for Sales in the Microsoft 365 Copilot side pane in Outlook. [Learn more about unified side pane](#unified-side-pane-in-outlook-on-the-web-and-outlook-for-windows).

> [!NOTE]
> If you're a Dynamics 365 Sales Premium customer, the ability to activate Copilot for Sales is included with the license. To activate, ensure that the users have a Microsoft 365 Copilot license and Dynamics 365 Sales Premium license associated to their user profile in the Microsoft 365 admin center. This will automatically enable Copilot for Sales.

:::image type="content" source="media/premium-license-small.png" alt-text="Screenshot showing Copilot for Sales license user interface." lightbox="media/premium-license.png":::

Legend:
1. Email summary and generative replies integrated into Outlook as part of the Microsoft 365 Copilot experience.
1. The **Key sales info** card provides an overview about account, contact, and opportunity.
1. Related CRM records are placed after the **Key sales info** card.

In the Outlook calendar view, you can see the opportunity summary and insights from partner apps, if enabled.

In Microsoft Teams, you can use chat capabilities of Copilot in Microsoft Teams enriched with the seller capabilities such as generating opportunity summary using CRM data and getting brand/competitor information during the meeting.

:::image type="content" source="media/teams-copilot-chat.png" alt-text="Screenshot showing Copilot in Teams chat user interface.":::

After a Teams meeting, the meeting summary is enriched with capabilities such as action items, participant statistics, and task creation in CRM from within Teams.

:::image type="content" source="media/teams-recap.png" alt-text="Screenshot showing meeting summary enriched with sales data in Teams recap.":::

### Unified side pane in Outlook on the web and Outlook for Windows

For users using Outlook on the web or the new Outlook for Windows, the Copilot for Sales side pane in Outlook is now unified with the Microsoft 365 Copilot side pane. This allows users to experience a single unified Copilot in Outlook wherein all the Copilot for Sales capabilities can be accessed directly from the Microsoft 365 Copilot side pane. 

Select the hamburger menu (:::image type="icon" source="media/hamburger.png" border="false":::) in the Microsoft 365 Copilot side pane and select **Sales** to access the Copilot for Sales capabilities.

:::image type="content" source="media/unified-m365-sidecar.png" alt-text="Screenshot of the unified side pane for Copilot for Sales":::

> [!NOTE]
> The unified Copilot experience is currently available only in Outlook on the web (Outlook online) and the new Outlook for Windows. For all other Outlook surfaces, users would experience Copilot for Sales capabilities in the dedicated Copilot for Sales side pane in Outlook.

## Enhanced Teams app support

The existing Sales Copilot Teams app and Outlook add-in have been upgraded to a single enhanced Teams app. The enhanced Teams app allows the Teams personal app that includes the **Home** and **Settings** tab to be available in Microsoft 365 applications including Outlook. Additionally, the Teams message extension now allows searching for CRM records and embedding them as rich adaptive cards directly into an email - similar to how it can be used in a Teams chat. The enhanced app also allows the packaging of Microsoft 365 Copilot capabilities thereby opening up the ability to ask questions such as "Summarize account Fabrikam" directly in the Microsoft 365 chat.

### New deployments

Although the new Copilot for Sales enhanced Teams app is packaged as a single app, deployment is still needed in both the Microsoft 365 admin center for Outlook and Microsoft 365 apps and the Teams admin center for Teams deployment. See deployment guides for details: [Dynamics 365 customers](deploy-viva-sales-d365.md) and [Salesforce CRM customers](deploy-viva-sales-sf.md).

### Update existing Sales Copilot deployments

#### Upgrade the app within Teams 

Due to the upgrade of the previous Sales Copilot Teams app to an enhanced Teams app, every Teams user will be presented with an update button within Teams. In this case, no administration is needed in the Teams admin center. [Learn more about updating an app in Microsoft Teams](https://support.microsoft.com/office/update-an-app-in-microsoft-teams-3d53d136-5c5d-4dfa-9602-01e6fdd8015b).

#### Upgrade the app for Outlook 

To get the benefits of the new enhanced Teams app within Outlook, the new app needs to be deployed to the same set of users as the existing Outlook add-in within the Microsoft 365 admin center. [Learn more about installing Copilot for Sales for Outlook](install-viva-sales-as-an-integrated-app.md)

If Copilot for Sales was previously deployed from the Microsoft 365 admin center, the **Merge both versions** button is shown when you [manage the app](install-viva-sales-as-an-integrated-app.md#manage-the-copilot-for-sales-app). You must select **Merge both versions** to upgrade the app to the latest version. 