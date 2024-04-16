---
title: Collaborate in account and deal room teams
description: Learn how sellers can use account teams and deal room teams to collaborate with colleagues and customers in Microsoft Teams.
ms.date: 04/15/2024
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/14/2023
  - bap-template
---

# Collaborate in account and deal room teams

You can open a collaboration space&mdash;an account team or a deal room channel in Microsoft Teams&mdash;in a variety of ways.

- In Outlook, open Copilot for Sales, and then follow one of these steps:
    
  - Scroll down to the **Collaborate in Teams** card, and then select the account team name or, for opportunities, the opportunity channel name.

    :::image type="content" source="media/created-deal-room-viva-sales.png" alt-text="Screenshot of the Collaborate in Teams card in Copilot for Sales for Outlook, with the deal room channel highlighted.":::

  - In the **Accounts** or **Opportunities** card, hover over a record, select **More actions (...)** > **Teams**, and then select the account team name or, for opportunities, the opportunity channel name.
    
    :::image type="content" source="media/deal-room-record-card.png" alt-text="Screenshot showing deal rooms from record card.":::
    
  - Open account or opportunity details. Scroll down to the **Collaborate in Teams** card, and then select the account team name or, for opportunities, the opportunity channel name.

     :::image type="content" source="media/deal-room-record-details-view.png" alt-text="Screenshot showing deal rooms in record details view.":::

- In Teams, select the account team or deal room channel.

- In Dynamics 365 Sales, open an account or opportunity. Select **Collaborate**, and then select the team that's linked to the account or opportunity. [Learn how to access linked teams and channels](access-linked-teams-channels.md).

## Anatomy of a collaboration space

A team that was created using the account team template or the deal room template always has a **General** channel. Other channels depend on how the team was created and whether more channels were created later.

- The **General** channel is where you can work with members of the sales team or other colleagues on account-related activities. If the team was created using the account team template, the **General** channel is linked to the account in your CRM.

- A channel named for an opportunity, like **Coffee Machine**, is where you can work with the sales team or other colleagues on activities that are related to a specific opportunity. If the team was created using the deal room template, the channel is linked to the opportunity in your CRM.

- Shared channels, named **Customer - *AccountName*** or **Customer - *OpportunityName***, are where you can work with people outside your organization, like customers, on account and opportunity activities.

  Before you can add customers to shared channels using their federated identity, your tenant administrator needs to turn on shared channels in Teams. [Learn more about collaborating with external participants in a shared channel](/microsoft-365/solutions/collaborate-teams-direct-connect?view=o365-worldwide&preserve-view=true).

Internal channels like **General** and **Coffee Machine** have the following apps pinned as tabs:

- **Files** comes with three starter folders for organizing documents that are related to the account or the opportunity, and one CRM folder for organizing CRM-related files. Your administrator might have linked the CRM folder to the CRM storage location that's associated with the account or opportunity.

- **CRM** displays the linked CRM account or opportunity record. You can view and update the CRM information in this tab.

  > [!NOTE]
  > - If you're using Salesforce as your CRM, you need to use the Teams desktop application to view account or opportunity details. The **CRM** tab doesn't load in the Teams web application.
  > - The CRM tab doesn't load in the new version of Teams. To see a CRM record in the new version of Teams, [use the Copilot for Sales app to share a customer's record as an adaptive card](share-crm-record-teams-conversation.md). Alternatively, you can use the classic version of Teams to view account or opportunity details in the CRM tab.

- **Notes** is a OneNote notebook you can use to share notes with all the members of the channel. It is provided by Teams.

- **CRM OneNote** is a OneNote notebook you can use to share notes with all the members of the channel. It is available only in the existing collaboration spaces that were created before April 15, 2024.

    > [!NOTE]
    > If the **CRM OneNote** tab shows an error message when you open it, you must delete the tab by right-clicking it and selecting **Remove**. You must use the **Notes** tab provided by Teams to share notes in the channel.

Shared channels like **Customer - Fourth Coffee** or **Customer - Coffee Machine** have the following apps pinned as tabs:

- **Files** comes with three starter folders for organizing documents that are related to the account or the opportunity.

- **OneNote** is a OneNote notebook you can use to share notes with your customers. This notebook is different from the one that's created in the internal collaboration channels. Team members who aren't part of the shared channel can't access this notebook.

The following screenshot shows an example of an account team for the Fourth Coffee account:

:::image type="content" source="media/anatomy-account-team.png" alt-text="Screenshot of an account team in Microsoft Teams.":::

The following screenshot shows an example of a deal room team for the Fourth Coffee account:

:::image type="content" source="media/anatomy-deal-room-team.png" alt-text="Screenshot of a deal room team in Microsoft Teams.":::

| Annotation | Description |
|------------|-------------|
| 1          | New account team created with two default channels    |
| 2          | General channel to collaborate on account-related activities with people in your organization; linked to the CRM account |
| 3          | Shared account team channel to collaborate with people outside your organization  |
| 4          | Prepinned apps  |
| 5          | New deal room channel created in an existing account team, used to collaborate with people in your organization; linked to the CRM opportunity |
| 6          | Shared deal room channel to collaborate with people outside your organization |

## View an AI-generated opportunity summary in the deal room channel

When you [set up a deal room](set-up-team-deal-room-template.md), the Copilot for Sales Teams app and bot are automatically installed for the selected team. The first time you open the deal room channel, an AI-generated [opportunity summary](view-opportunity-summary.md) is included in the standard channel welcome post.

> [!NOTE]
> - If you're using Dynamics 365 as your CRM system, you can view opportunity summary even if you are not signed in to the Copilot for Sales app in Outlook or if you are signed in to a different Dynamics environment, as long as you have read access for the record and Copilot for Sales privileges. This applies only to the auto posted opportunity summary.
> - If you're using Salesforce as your CRM system, you must be signed in to Salesforce in the Copilot for Sales app in Outlook to view opportunity summary while also having read access for the record and Copilot for Sales privileges.
> - Opportunity summary is not displayed in a private channel, as bots are not supported by Microsoft Teams in private channels. Also, shared channels have customers added, therefore, CRM information is not shared here as well.

:::image type="content" source="media/oppty-summary-deal-room.png" alt-text="Screenshot of an AI-generated opportunity summary in a deal room channel in Teams.":::

To view the opportunity summary again later, use either of the following methods:

- Enter `@Copilot for Sales show opportunity summary` in the message box.
- Enter `@Copilot for Sales help` in the message box, and then select **Generate Opportunity Summary** from the list of options.

The summary uses the following columns in the opportunity record in your CRM:

- Opportunity name
- Opportunity ID
- Created on
- Estimated close date
- Sales stage
- Budget amount
- Description
- Parent account name
- Primary contact name

The **Latest activity** content is generated from the last three notes in the opportunity record.

The AI-generated opportunity summary is available only when your administrator has [turned on copilot AI features](suggested-replies.md#turn-on-copilot-ai-features). If your administrator hasn't turned on those features, the opportunity summary is displayed in the form of field-value pairs. The fields that are included in the summary depend on what your administrator has set.

:::image type="content" source="media/oppty-summary-deal-room-non-ai.png" alt-text="Screenshot of an opportunity summary in a deal room channel when copilot AI features are turned off.":::

If your administrator has turned off the Copilot for Sales app in Teams, the opportunity summary isn't available at all.

### See also

- [Set up a team using the account team template](set-up-team-account-team-template.md)
- [Set up a team using the deal room template](set-up-team-deal-room-template.md)
