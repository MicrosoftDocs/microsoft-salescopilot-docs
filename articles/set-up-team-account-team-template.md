---
title: Set up a team using account team template
description: Learn how to set up a team using account team template.
ms.date: 08/23/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais 
---

# Set up a team using account team template

When working with an account team template, you can [create a new team from Outlook](#create-a-new-account-team-from-outlook) or [set up an existing team from Outlook](#set-up-an-existing-account-team-from-outlook).

> [!NOTE]
> You can set up teams and channels by applying sales templates in Sales Copilot from Outlook only. In the Sales app, you can use the existing [enhanced collaboration](/dynamics365/sales/teams-integration/teams-collaboration-enhanced-experience) functionality to set up basic teams and channels linked to your CRM account. These teams and channels linked from Sales app do not come with pre-defined channels and pre pinned apps that sales templates provide. Linked teams and channels can be accessed both from Outlook and Sales app regardless of how they have been set up.

## Create a new account team from Outlook

1. Open the email communication with your customer, and then open Sales Copilot.

1. On the **Highlights** tab, go to the **Collaborate in Teams** card, hover over the account name, and then select **Set up account team**.

    :::image type="content" source="media/team-button.png" alt-text="Screenshot showing set up account team button.":::

1. In the **Set up an account team** step, select **Create a new team**.

    :::image type="content" source="media/team-type.png" alt-text="Screenshot showing select account team type.":::

1. In the **Set up your team** step, update the team name, if required, and select the sensitivity and privacy of your team. Select **Next**.

    By default, the team's name is set to the account's name. Sensitivity options will show up if it has been set up by your tenant administrator. More information: [Sensitivity labels for Microsoft Teams](/microsoftteams/sensitivity-labels)

    If sensitivity options are set up by your administrator, privacy of the team (Private/Public) defaults to the tenant admin settings.

    :::image type="content" source="media/account-team.png" alt-text="Screenshot showing set up account team.":::

1. In the **Add team members** step, select your colleagues to add to the General channel (for internal collaboration). You can select from the recommended team members that are shared with you.

    :::image type="content" source="media/add-members.png" alt-text="Screenshot showing add members to account team.":::

    A shared channel is automatically created for collaborating with customers. Customers and your colleagues are not added to the shared channel. Owners of the team can add members to this channel from Microsoft Teams after it is created.

    The recommended team members are suggested based on the following logic:

    - **Dynamics 365**: CRM account owner, members with whom the account is shared, and members of the access team. If the account owner is a group, the list of users from this group is displayed.

    - **Salesforce CRM**: CRM account owner and members who are part of the account team. For information about enabling account teams in Salesforce, see [Facilitate Collaboration by Enabling Account Teams](https://help.salesforce.com/s/articleView?id=sf.accountteam_enable.htm&type=5).

1. Select **Create team**.

    Once the basic General channel is set up, a confirmation message is displayed. Select **Open in Teams** to access the team. A new team is created in Microsoft Teams as follows:

    :::image type="content" source="media/new-account.png" alt-text="Screenshot showing new account team in Teams.":::

    For more information about working with the newly created team, see [Collaborate in Teams using the newly created or existing team](collaborate-teams-newly-created-existing-team.md).

    Once the team is completely set up with pre pinned apps and shared channel, it can also be accessed from the **Collaborate in Teams** card in the **Highlights** tab of Sales Copilot app. Select the team to open it in Microsoft Teams.

    :::image type="content" source="media/new-account-viva-sales.png" alt-text="Screenshot showing created new account team in Sales Copilot.":::

## Set up an existing account team from Outlook

1. Open the email communication with your customer, and then open Sales Copilot.

2. On the **Highlights** tab, go to the **Collaborate in Teams card**, hover over the account name, and then select **Set up account team**.

    :::image type="content" source="media/team-button.png" alt-text="Screenshot of set up account team button.":::

3. In the **Set up an account team** step, select **Use an existing team**.

    :::image type="content" source="media/team-type.png" alt-text="Screenshot of select account team type.":::

4. In the **Select a team** step, select the team you want to set up, and then select **Next**.

    The list of teams shown are the ones of which you are an owner or a member of in Teams app.

    :::image type="content" source="media/select-team.png" alt-text="Screenshot showing select team for existing account team.":::

    > [!NOTE]
    > When you set up an account team for an existing team, a new channel is created and linked to the CRM account.

5. In the **Set up your channels** step, update the channel name, if required, and select a privacy option.

    A shared channel is automatically created for collaborating with customers if you are the owner of the existing team. Only owners can create shared channels. Customers and your colleagues are not added to the shared channel. Owners of the team can add members to this channel from Microsoft Teams after it is created.

    :::image type="content" source="media/set-channel.png" alt-text="Screenshot showing set up channel for account team.":::

6. Select **Set up team**.

    Once the team is set up, a confirmation message is displayed. Select **Open in Teams** to access the team. Two new channels are created in existing team in Microsoft Teams as follows:

    :::image type="content" source="media/two-channels.png" alt-text="Screenshot showing existing account team in Teams.":::

    For more information about working with the newly created channel, see [Collaborate in Teams using the newly created or existing team](collaborate-teams-newly-created-existing-team.md).

    This team can also be accessed from the **Collaborate in Teams** card in the **Highlights** tab of Sales Copilot app. Select the team to open it in Microsoft Teams.

    :::image type="content" source="media/existing-team.png" alt-text="Screenshot showing created existing account team in Sales Copilot.":::