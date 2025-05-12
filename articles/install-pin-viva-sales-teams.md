---
title: Install and pin Microsoft 365 Copilot for Sales in Teams
description: Learn how to install and pin Copilot for Sales in Teams
ms.date: 11/29/2024
ms.topic: install-set-up-deploy
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Install and pin the Microsoft 365 Copilot for Sales app in Teams

To install the Copilot for Sales app in Teams, go to the Teams admin center and create setup policies to install the app and assign users. We recommend you to pin the app to increase discoverability and encourage your sellers to use it.

To install and pin the app in Teams, you'll [create a custom Teams app setup policy](#create-a-custom-teams-app-setup-policy) and [assign the policy to a user group](#assign-the-custom-teams-app-setup-policy-to-a-user-group) (security group, organizational unit, or distribution list).

> [!NOTE]
> - The Teams meeting must be transcribed for Copilot for Sales to generate insights. For information about enabling recording transcription for your organization, go to [Turn on or turn off recording transcription](/microsoftteams/cloud-recording#turn-on-or-turn-off-recording-transcription).
> - The connection between Copilot for Sales and your CRM is controlled through Copilot for Sales add-in in Outlook. More information: [Use Copilot for Sales in Outlook](use-sales-copilot-outlook.md)

## Create a custom Teams app setup policy

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard).  
1. In the left pane, select **Teams apps** &gt; **Setup policies**.  
1. On the **Manage policies** tab, select **Add**.  
1. Enter a name and description for the policy.  
1. Turn on **User pinning**.  
1. Under **Installed apps**, select **Add apps**.  
1. In the **Add installed apps** panel, search for the **Copilot for Sales** app. You can also filter apps by app permission policy.  
1. Select **Add** to add Copilot for Sales to the list of apps to install.  
1. Select **Add** again to install the listed apps.  
1. Under **Pinned apps**, select **Add apps**.  
1. In the **Add pinned apps** panel, search for the **Copilot for Sales** app. You can also filter apps by app permission policy.  
1. Select **Add** to add Copilot for Sales to the list of apps to pin.  
1. Select **Add** again to pin the listed apps.  
1. Under **App bar** or **Messaging extensions**, arrange the apps in the order that you want them to appear in Teams.  
1. Select **Save**.

For more information about managing Teams app setup policies, go to [Manage app setup policies in Microsoft Teams](/microsoftteams/teams-app-setup-policies).

## Assign the custom Teams app setup policy to a user group

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard).  
1. In the left pane, select **Teams apps** &gt; **Setup policies**.  
1. On the **Group policy assignment** tab, select **Add**.  
1. Search for and add the group you want to assign the policy to.  
    Ideally, this is the group that sellers belong to. If your sellers are spread across multiple groups, you'll need to create multiple group policy assignments.  
1. Set the ranking for the group assignment.  
1. Select the policy you created earlier.  
1. Select **Apply**.

For more information about assigning user and group policies, go to [Assign policies to users and groups](/microsoftteams/assign-policies-users-and-groups).

## Welcome message

Once the Copilot for Sales app is deployed, each user is welcomed by an engaging message from the Copilot for Sales bot in Teams. This message outlines the key capabilities in Copilot for Sales and provides direct links to comprehensive feature documentation and other learning resources.

### Related information

[Install Copilot for Sales add-in for Outlook](install-viva-sales-as-an-integrated-app.md)
