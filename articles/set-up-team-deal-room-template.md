---
title: Set up a team using deal room template 
description: Learn how to set up a team using deal room template.
ms.date: 08/23/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais 
---

# Set up a team using deal room template

When working with a deal room template, you can [set up an existing team from Outlook](#set-up-an-existing-deal-room-team-from-outlook) or [create a new team from Outlook](#create-a-new-deal-room-team-from-outlook).

> [!NOTE]
> You can set up teams and channels by applying sales templates in Sales Copilot from Outlook only. In the Sales app, you can use [existing enhanced collaboration](/dynamics365/sales/teams-integration/teams-collaboration-enhanced-experience) functionality to set up basic teams and channels linked to your CRM opportunity. These teams and channels linked from Sales app do not come with pre-defined channels and pre pinned apps that Sales templates provide. Linked teams and channels can be accessed both from Outlook and Sales app regardless of how they have been set up.

## Set up an existing deal room team from Outlook

1. Open the email communication with your customer, and then open Sales Copilot.

1. On the **Highlights** tab, go to the **Collaborate in Teams** card, hover over the opportunity name, and then select **Set up deal room**.

    :::image type="content" source="media/deal-room.png" alt-text="Screenshot showing set up deal room button.":::

1. In the **Set up a deal room** step, select **Use an existing team**.

    :::image type="content" source="media/deal-room-type.png" alt-text="Screenshot showing select deal room type.":::

1. In the **Select a team** step, select the team you want to set up, and then select **Next**.

    If the parent account for the opportunity is already linked in the Teams app, it's displayed as the recommended team to create a deal room channel.

    If you want to create a deal room channel under a different team, you can pick from the list of other teams displayed.

    :::image type="content" source="media/select-team-existing-deal-room.png" alt-text="Screenshot showing select team for existing deal room.":::

1. In the **Set up your channels** step:

    1. Update the channel name, if necessary, and select a privacy option.

    1. You can set up a shared channel for collaborating with customers. By default, **Include shared channel** is selected. Customers and your colleagues aren't added to the shared channel. Owners of the team can add members to this channel from Microsoft Teams after it's created.

        Shared channels can only be created by the owners of the team. If you pick an existing team that you're a member of, the option to create a shared channel is disabled.

        :::image type="content" source="media/set-channel-deal-room.png" alt-text="Screenshot showing setting up channel for deal room.":::

1. Select **Set up team**.

    Once the team is set up, a confirmation message is displayed. Select **Open in Teams** to access the team. Two new channels are created in existing team in Microsoft Teams as follows:

    :::image type="content" source="media/existing-deal-room.png" alt-text="Screenshot showing existing deal room in Teams.":::

    For more information about working with the newly created channel, see [Collaborate in Teams using the newly created or existing team](collaborate-teams-newly-created-existing-team.md).

    Once the team is completely set up with pre pinned apps and shared channel, it's shown in the **Collaborate in Teams** card in the **Highlights** tab of Sales Copilot app. Select the team to open it in Microsoft Teams.

    :::image type="content" source="media/created-deal-room-viva-sales.png" alt-text="Screenshot showing created existing deal room in Sales Copilot.":::

## Create a new deal room team from Outlook

1. Open the email communication with your customer, and then open Sales Copilot.

1. On the **Highlights** tab, go to the **Collaborate in Teams** card, hover over the opportunity name, and then select **Set up deal room**.

    :::image type="content" source="media/deal-room.png" alt-text="Screenshot of set up deal room button.":::

1. In the **Set up a deal room** step, select **Create a new team**.

    :::image type="content" source="media/deal-room-type.png" alt-text="Screenshot of select deal room type.":::

1. In the **Set up your team** step, update the team name, if necessary, and select the sensitivity and privacy of your team. Select **Next**.

    By default, the team's name is set to the opportunity's name. Sensitivity options are displayed if they have been set up by your tenant administrator. More information: [Sensitivity labels for Microsoft Teams](/microsoftteams/sensitivity-labels)

    If sensitivity options are set up by your administrator, the privacy of the team (Private/Public) defaults to the tenant admin settings.

    :::image type="content" source="media/set-deal-room.png" alt-text="Screenshot showing set up deal room.":::

1. In the **Add team members** step, select your colleagues to add to the team that is being set up, and then select **Next**.

    > [!NOTE]
    > Selected team members are not added to the shared channel. Team owners must add them explicitly from Microsoft Teams.

    The recommended team members are suggested based on the following logic:

    - **Dynamics 365**: CRM opportunity owner, members with whom opportunity is shared, and members of the access team. If the opportunity owner is a group, the list of users from this group is displayed.

    - **Salesforce CRM**: CRM opportunity owner and members who are part of the opportunity team. For information about enabling opportunity teams in Salesforce, see [Facilitate Team Selling by Enabling Opportunity Teams](https://help.salesforce.com/s/articleView?id=sf.teamselling_enabling.htm&type=5).

        :::image type="content" source="media/add-members-deal-room.png" alt-text="Screenshot showing add members to deal room.":::

1. In the **Set up your channels** step:

    1. Update the channel name, if necessary, and select a privacy option.

    1. You can set up a shared channel for collaborating with customers. By default, **Include shared channel** is selected. Customers and your colleagues aren't added to the shared channel. Owners of the team can add members to this channel from Microsoft Teams after it's created.

        :::image type="content" source="media/set-channel-deal-room.png" alt-text="Screenshot of set up channel for deal room.":::

1. Select **Set up team**.

1. Once the basic General channel is set up, a confirmation message is displayed. Select **Open in Teams** to access the team. A new team is created in Microsoft Teams as follows:

    :::image type="content" source="media/new-teams-deal-room.png" alt-text="Screenshot showing new deal room in Teams.":::

    For more information about working with the newly created team, see [Collaborate in Teams using the newly created or existing team](collaborate-teams-newly-created-existing-team.md).

1. Once the team is completely set up with pre pinned apps and shared channel, it's shown in the **Collaborate in Teams** card in the **Highlights** tab of Sales Copilot app. Select the team to open it in Microsoft Teams.

    :::image type="content" source="media/created-new-deal-room-viva-sales.png" alt-text="Screenshot showing created new deal room in Sales Copilot.":::