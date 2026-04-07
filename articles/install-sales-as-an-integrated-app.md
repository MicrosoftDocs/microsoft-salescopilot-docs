---
title: Install Sales agent in Outlook
description: Learn how to install, manage, and update the Sales agent in Microsoft 365 with this comprehensive guide.
ms.date: 04/07/2026
ms.topic: install-set-up-deploy
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:06/19/2024
---

# Install Sales agent in Outlook

As an administrator, you can install the Sales agent as an integrated app from Microsoft 365 admin center. The app is installed in Fixed mode by default. In a Fixed deployment, users receive the app automatically and can't remove it. You can also manage the app's configuration, add and remove users, and view its usage in the Microsoft 365 admin center.

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/).  
1. In the left pane, select **Agents** > **All agents**.  
1. On the **All agents** page, search for **Sales** and select it.
1. In the **Sales** pane, select **Deploy**.

    :::image type="content" source="media/sales-agent-deploy.png" alt-text="Screenshot of the Sales pane in the Microsoft 365 admin center, with the Deploy button highlighted.":::

1. In the **Select users** step, select the users or groups who will have access to the app, and then select **Next**. Learn more about configuring users and groups at [Considerations when assigning an add-in to users and groups](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true#considerations-when-assigning-an-add-in-to-users-and-groups)

    :::image type="content" source="media/sales-agent-deploy-users.png" alt-text="Screenshot of the Select users step in the Sales agent deployment process.":::

1. In the **Accept permissions** step, select **Next**.  
1. In the **Review & finish** step, review the selected settings, and then select **Finish deployment**.  
1. When the deployment is complete, select **Done**.  
    Allow up to six hours for the Sales agent to appear in users' Outlook ribbon.

> [!NOTE]
> The app is installed in Outlook and other Microsoft 365 applications but not in Teams. You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. For information about installing the Sales agent in Teams, go to [Install and pin the Sales agent in Teams](install-pin-sales-teams.md).


> [!IMPORTANT]
> It can take up to 48 hours for the app to appear in Outlook and other Microsoft 365 apps. If users can't see the app after 48 hours, it might be due to the public attachment handling policy. More information: [Why can't users see the Sales agent in Outlook after it's deployed?](sales-m365-copilot-faq.md#why-cant-users-see-the-sales-agent-in-outlook-after-its-deployed)

## Manage the Sales agent

After you've deployed the Sales agent, you can manage its configuration by adding or removing agents, adding custom tools and knowledge, and updating users.

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), select **Agents** > **All agents**.  
1. On the **All agents** page, select **Sales**.  

The **Sales** panel opens with the following tabs:

- **Overview**: Displays basic information about the agent, assigned users, and channel availability.
- **Connected Agents**: Displays any agents that are connected to the Sales agent.
- **Custom tools & knowledge**: Allows you to add custom tools and knowledge to the Sales agent to enhance its capabilities.
- **Users**: Allows you to edit the users who can use the app.  

## Update the Sales agent

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), select **Agents** > **All agents**.  
1. On the **All agents** page, select **Sales**. 
1. In the **Sales** panel, select **Update**.

## User-deployed app installation

End users can install the Outlook add-in and Teams app from within Microsoft Marketplace in Outlook or Teams respectively, as long as they aren't explicitly blocked by the administrator.  

If end users install the Outlook add-in, it's considered user-deployed instead of admin-deployed and will not have full feature support. User-deployed apps don't support the Sales agent banner notifications that appear within the top of new or reply emails. Also, the Sales agent is not added automatically to meeting invites. However, sellers can manually add the Sales agent to the meeting to get meeting summaries.

### Related information

[Install and pin the Sales agent in Teams](install-pin-sales-teams.md)
