---
title: Set up a team using the deal room template 
description: Learn how to set up a team using a deal room team template in the Copilot for Sales add-in for Outlook.
ms.date: 09/29/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/13/2023
  - bap-template
---

# Set up a team using the deal room template

You can create a [collaboration space from a sales template](./collaboration-space.md) only in the Copilot for Sales add-in for Outlook. You can use the [enhanced collaboration](/dynamics365/sales/teams-integration/teams-collaboration-enhanced-experience) feature in Dynamics 365 Sales to set up basic teams and channels that are linked to your customer relationship management (CRM) accounts. However, they don't come with the predefined channels and pinned apps that the sales templates provide.

Regardless of how you set them up, you can access linked teams and channels from both Outlook and the Sales app.

When you create a collaboration space with the deal room team template, you can [create a deal room team](#create-a-deal-room-team) or [set up an existing team as a deal room team](#set-up-an-existing-team-as-a-deal-room-team).

## Set up an existing team as a deal room team

1. In Outlook, open an email to or from your customer, and then open Copilot for Sales.

1. Go to the **Collaborate in Teams** card, hover over the opportunity name, and then select **Set up deal room**.

    :::image type="content" source="media/deal-room.png" alt-text="Screenshot of the Collaborate in Teams card in Copilot for Sales for Outlook, with the Set up deal room button highlighted.":::

1. In the **Set up a deal room** step, select **Use an existing team**.

1. In the **Select a team** step, select a team from the list of teams that you own or are a member of, and then select **Next**.

    If the opportunity's parent account is already linked to a team, the linked team is shown as the recommended one to create the deal room channel in. You can create the channel in any of the other teams listed, however.

    :::image type="content" source="media/select-team-existing-deal-room.png" alt-text="Screenshot of the Select a team step in Copilot for Sales for Outlook.":::

1. In the **Set up your channels** step, change the channel name, if necessary, and select a privacy option. To add a shared channel for collaborating with customers, leave **Include shared channel** selected.

    Only team owners can create shared channels. If you select a team that you don't own, the option to include a shared channel is disabled.

    Customers and colleagues aren't added to the shared channel automatically. Owners of the team can add members to the channel later directly in Teams.

    :::image type="content" source="media/set-channel-deal-room.png" alt-text="Screenshot of the Set up your channels step in Copilot for Sales for Outlook.":::

1. Select **Set up team**.

    After the team is set up, a confirmation message is displayed. Select **Open in Teams** to view the new team.

[Learn how to collaborate in Teams using the new team](collaborate-teams-newly-created-existing-team.md).

## Create a deal room team

1. In Outlook, open an email to or from your customer, and then open Copilot for Sales.

1. Go to the **Collaborate in Teams** card, hover over the opportunity name, and then select **Set up deal room**.

    :::image type="content" source="media/deal-room.png" alt-text="Screenshot of the Collaborate in Teams card in Copilot for Sales for Outlook, with the Set up deal room button highlighted.":::

1. In the **Set up a deal room** step, select **Create a new team**.

1. In the **Set up your team** step, change the team name, if necessary, select its sensitivity and privacy, and then select **Next**.

    By default, the team name is set to the opportunity name. Your tenant administrator might have set the [sensitivity label](/microsoftteams/sensitivity-labels) and privacy option in the tenant settings.

    If sensitivity options are set up by your administrator, the privacy of the team (Private/Public) defaults to the tenant admin settings.

1. In the **Add team members** step, select recommended colleagues to add to the team's General channel for internal collaboration. You can add more later directly in Teams.

    :::image type="content" source="media/add-members-deal-room.png" alt-text="Screenshot of the Add team members step in Copilot for Sales for Outlook.":::

    > [!NOTE]
    > Selected team members are not added to the shared channel. Team owners must add them explicitly from Microsoft Teams.

    Team members are recommended based on the following criteria:

    - **Dynamics 365**: The CRM opportunity owner, members of the opportunity team, and members the opportunity is shared with. If the opportunity owner is a group, the members of the group are listed.

    - **Salesforce CRM**: The CRM opportunity owner and members of the opportunity team. [Learn more about using opportunity teams in Salesforce](https://help.salesforce.com/s/articleView?id=sf.teamselling_enabling.htm&type=5).

1. In the **Set up your channels** step, change the channel name, if necessary, and select a privacy option. To add a shared channel for collaborating with customers, leave **Include shared channel** selected.

    Customers and colleagues aren't added to the shared channel automatically. Owners of the team can add members to the channel later directly in Teams.

    :::image type="content" source="media/set-channel-deal-room.png" alt-text="Screenshot of the Set up your channels step in Copilot for Sales for Outlook.":::

1. Select **Set up team**.

    After the basic General channel is set up, a confirmation message is displayed. Select **Open in Teams** to view the new team.

[Learn how to collaborate in Teams using the new team](collaborate-teams-newly-created-existing-team.md).

## Alternative ways to set up a deal room team

You can also set up a team using the deal room template in the following ways:

- In the **Opportunities** card in the Copilot for Sales pane, hover over the opportunity name, and then select **More actions (...)** > **Teams** > **Set up deal room**. [Set up a new team](#create-a-deal-room-team) or [use an existing team as a deal room team](#set-up-an-existing-team-as-a-deal-room-team).

    :::image type="content" source="media/deal-room-record-card.png" alt-text="Screenshot showing creating deal room team from record card.":::

- When viewing opportunity details in the Copilot for Sales pane, go to the **Collaborate in Teams** card, and then select **Set up deal room**. If deal room teams already exist, the button name displayed is **Set up another deal room**. [Set up a new team](#create-a-deal-room-team) or [use an existing team as a deal room team](#set-up-an-existing-team-as-a-deal-room-team).

    :::image type="content" source="media/deal-room-record-details-view.png" alt-text="Screenshot showing creating deal room team from record details view.":::

After you set up a team, you can [collaborate in Teams using the new team](collaborate-teams-newly-created-existing-team.md).
