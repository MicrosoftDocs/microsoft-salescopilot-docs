---
title: Set up a team using the account team template
description: Learn how to set up a team using an account team template in the Copilot for Sales add-in for Outlook.
ms.date: 02/19/2024
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

# Set up a team using the account team template

You can create a [collaboration space from a sales template](./collaboration-space.md) only in the Copilot for Sales add-in for Outlook. You can use the [enhanced collaboration](/dynamics365/sales/teams-integration/teams-collaboration-enhanced-experience) feature in Dynamics 365 Sales to set up basic teams and channels that are linked to your customer relationship management (CRM) accounts. However, they don't come with the predefined channels and pinned apps that the sales templates provide.

Regardless of how you set them up, you can access linked teams and channels from both Outlook and the Sales app.

When you create a collaboration space with the account team template, you can [create an account team](#create-an-account-team) or [set up an existing team as an account team](#set-up-an-existing-team-as-an-account-team).

## Create an account team

1. In Outlook, open an email to or from your customer, and then open Copilot for Sales.

1. Go to the **Collaborate in Teams** card, hover over the account name, and then select **Set up account team**.

    :::image type="content" source="media/team-button.png" alt-text="Screenshot of the Collaborate in Teams card in Copilot for Sales for Outlook, with the Set up account team button highlighted.":::

1. In the **Set up an account team** step, select **Create a new team**.

1. In the **Set up your team** step, change the team name, if necessary, select its sensitivity label and privacy option, and then select **Next**.

    By default, the team name is set to the account name. Your tenant administrator might have set the [sensitivity label](/microsoftteams/sensitivity-labels) and privacy option in the tenant settings.

    If sensitivity options are set up by your administrator, privacy of the team (Private/Public) defaults to the tenant admin settings.

1. In the **Add team members** step, select recommended colleagues to add to the team's General channel for internal collaboration. You can add more later directly in Teams.

    :::image type="content" source="media/add-members.png" alt-text="Screenshot of the Add team members step in Copilot for Sales for Outlook.":::

    Team members are recommended based on the following criteria:

    - **Dynamics 365**: The CRM account owner, members of the account team, and members the account is shared with. If the account owner is a group, the members of the group are listed.

    - **Salesforce CRM**: The CRM account owner and members of the account team. [Learn more about using account teams in Salesforce](https://help.salesforce.com/s/articleView?id=sf.accountteam_enable.htm&type=5).

    A shared channel is created for collaborating with customers, but the team members you select aren't added to it automatically. Add customers and colleagues later directly in Teams.

1. Select **Create team**.

    After the basic General channel is set up, a confirmation message is displayed. Select **Open in Teams** to view the new team.

[Learn how to collaborate in Teams using the new team](collaborate-teams-newly-created-existing-team.md).

## Set up an existing team as an account team

When you set up an account team for an existing team, a new channel is created in the team and linked to the CRM account.

1. In Outlook, open an email to or from your customer, and then open Copilot for Sales.

1. Go to the **Collaborate in Teams card**, hover over the account name, and then select **Set up account team**.

    :::image type="content" source="media/team-button.png" alt-text="Screenshot of the Collaborate in Teams card in Copilot for Sales for Outlook, with the Set up account team button highlighted.":::

1. In the **Set up an account team** step, select **Use an existing team**.

1. In the **Select a team** step, select a team from the list of teams that you own or are a member of, and then select **Next**.

1. In the **Set up your channels** step, change the channel name, if necessary, select a privacy option, and then select **Next**.

    By default, the channel name is set to the account name.

    If you're the owner of the team, a shared channel is created for collaborating with customers, but no members are added automatically. Add customers and colleagues later directly in Teams.

    If you're not the owner, ask the team owner to create a shared channel and add customers and colleagues later directly in Teams.

1. Select **Set up team**.

    After the team is set up, a confirmation message is displayed. Select **Open in Teams** to view the new team.

[Learn how to collaborate in Teams using the new team](collaborate-teams-newly-created-existing-team.md).


## Alternate ways to set up an account team

You can also set up a team using the account team template in the following ways:

- In the **Accounts** card in the Copilot for Sales pane, hover over the account name, and then select **More actions (...)** > **Set up account team**. [Set up a new team](#create-an-account-team) or [use an existing team as an account team](#set-up-an-existing-team-as-an-account-team).
- When viewing account details in the Copilot for Sales pane, go to the **Collaborate in Teams** card, and then select **Set up account team**. [Set up a new team](#create-an-account-team) or [use an existing team as an account team](#set-up-an-existing-team-as-an-account-team).

After you set up a team, you can [collaborate in Teams using the new team](collaborate-teams-newly-created-existing-team.md).