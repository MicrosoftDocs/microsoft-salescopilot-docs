---
title: What's new in Sales Copilot changing to Copilot for Sales
description: Revamped Sales Copilot, now called Microsoft Copilot for Sales, merges features and improves user experience.
ms.date: 05/30/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:01/23/2024
---

# What's new in Sales Copilot changing to Copilot for Sales

On February 1, 2024, Sales Copilot will be changing to bring the power of Copilot for Microsoft 365 and the role specific insights and actions together under a new offering called Microsoft Copilot for Sales. As part of the effort, we are excited to bring the following updates:

- **New user experience**: The **Highlights** and CRM tabs are merged into one unified view.
- **License changes**: A new Copilot for Sales license is introduced, which includes Copilot for Microsoft 365 subscription.
- **Enhanced Teams app**: The existing Sales Copilot Teams app and Outlook add-in have been upgraded to a single enhanced Teams app. 

## New user experience

The new user experience brings the **Highlights** and CRM tabs together into one unified view. The new view is designed to provide a more streamlined experience by bringing the most relevant information to the top of the view.

:::image type="content" source="media/comparison.png" alt-text="Screenshot showing old and new user interface." lightbox="media/comparison.png":::

Legend:
1. Generate email content using Copilot capabilities
1. Related CRM records
1. Contact, account, and opportunity summaries
1. Extend Copilot for Sales with partner apps

## License changes

A new Copilot for Sales license is introduced, which includes Copilot for Microsoft 365 subscription. 

### Existing Sales Copilot license

The existing Sales Copilot license is referred to as Copilot for Sales standard license. The Copilot for Sales standard license will continue to provide the same capabilities as the Sales Copilot license, but with the new order of the cards in the Outlook mailbox view.

:::image type="content" source="media/standard-license-small.png" alt-text="Screenshot showing standard license user interface." lightbox="media/standard-license.png":::

Legend:
1. Email summary and generative replies
1. Save email to CRM is moved to the top and related CRM records are placed after the **Key email info** card.
1. Opportunity summary
1. Create and access collaboration spaces in Teams

In the Outlook calendar view, the cards order will remain the same as in the mailbox view, but there will be no email summary.

In Microsoft Teams, the Copilot for Sales Standard license will continue to provide the same capabilities as the Sales Copilot license. 

### New Copilot for Sales license

The new Copilot for Sales license is referred to as Copilot for Sales premium license. In this license, email summary and generative replies are integrated into Outlook as part of the Copilot for Microsoft 365 experience.

> [!NOTE]
> If you're a Dynamics 365 Premium customer, you can get the same capabilities as the Copilot for Sales premium license by purchasing the Copilot for Microsoft 365 license. 

:::image type="content" source="media/premium-license-small.png" alt-text="Screenshot showing premium license user interface." lightbox="media/premium-license.png":::

Legend:
1. Email summary and generative replies integrated into Outlook as part of the Copilot for Microsoft 365 experience.
1. Save to CRM is moved to the top and related CRM records are placed after the **Key sales info** card.
1. The **Key sales info** card provides an overview about account, contact, and opportunity.

In the Outlook calendar view, you can see the opportunity summary and insights from partner apps, if enabled.

In Microsoft Teams, you can use chat capabilities of Copilot in Microsoft Teams enriched with the seller capabilities such as generating opportunity summary using CRM data and getting brand/competitor information during the meeting.

:::image type="content" source="media/teams-copilot-chat.png" alt-text="Screenshot showing Copilot in Teams chat user interface.":::

After a Teams meeting, the meeting summary is enriched with capabilities such as action items, participant statistics, and task creation in CRM from within Teams.

:::image type="content" source="media/teams-recap.png" alt-text="Screenshot showing meeting summary enriched wih sales data in Teams recap.":::

## Enhanced Teams app support

The existing Sales Copilot Teams app and Outlook add-in have been upgraded to a single enhanced Teams app. The enhanced Teams app allows the Teams personal app which includes the **Home** and **Settings** tab to be available in Microsoft 365 applications including Outlook. Additionally, the Teams message extension now allows searching for CRM records and embedding them as rich adaptive cards directly into an email - similar to how it can be used in a Teams chat. The enhanced app also allows the packaging of Copilot for Microsoft 365 capabilities thereby opening up the ability to ask questions such as "Summarize account Fabrikam" directly in the Microsoft 365 chat.

The enhanced Teams app is initially supported in the desktop and web version of Outlook, but support for other Outlook clients such as Mac and mobile are not currently available. If your sellers use an unsupported version of the Outlook client, you should deploy both the new enhanced Teams app and the Outlook add-in. 

### New deployments

Although the new Copilot for Sales enhanced Teams app is packaged as a single app, deployment is still needed in both the Microsoft 365 admin center for Outlook and Microsoft 365 apps and the Teams admin center for Teams deployment. See deployment guides for details: [Dynamics 365 customers](deploy-viva-sales-d365.md) and [Salesforce CRM customers](deploy-viva-sales-sf.md).

### Update existing Sales Copilot deployments

#### Upgrading the app within Teams 

Due to the upgrade of the previous Sales Copilot Teams app to an enhanced Teams app, every Teams user will be presented with an update button within Teams. In this case, no administration is needed in the Teams admin center. [Learn more about updating an app in Microsoft Teams](https://support.microsoft.com/office/update-an-app-in-microsoft-teams-3d53d136-5c5d-4dfa-9602-01e6fdd8015b).

#### Upgrading the app for Outlook 

To get the benefits of the new enhanced Teams app within Outlook, the new app will need to be deployed to the same set of users as the existing Outlook add-in within the Microsoft 365 admin center. [Learn more about installing Copilot for Sales for Outlook](install-viva-sales-as-an-integrated-app.md)

The existing Sales Copilot add-in will be automatically updated to Copilot for Sales to support Outlook clients that do not yet support the enhanced Teams app such as Mac and mobile, thus no need to remove the existing deployment for the add-in.