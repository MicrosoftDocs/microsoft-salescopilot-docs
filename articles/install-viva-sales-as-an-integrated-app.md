---
title: Install Copilot for Sales in Outlook
description: Learn how to install, manage, and update the Copilot for Sales app in Microsoft 365 with this comprehensive guide.
ms.date: 08/09/2024
ms.topic: article
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

# Install Copilot for Sales in Outlook

As an administrator, you can install Copilot for Sales as an integrated app from Microsoft 365 admin center. The app is installed in Fixed mode by default. In a Fixed deployment, users receive the app automatically and can't remove it. You can also manage the app's configuration, add and remove users, and view its usage in the Microsoft 365 admin center.

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/).

2. In the left pane, select **Settings** > **Integrated apps**.

3. On the **Integrated apps** page, select **Get apps**.

    :::image type="content" source="media/get-apps-admin-center.svg" alt-text="Screenshot showing Get apps button in Microsoft 365 admin center.":::

    Microsoft AppSource opens in an embedded window.

4. In the **AppSource** window, search for **Copilot for Sales**.

5. In the search results, on the **Copilot for Sales** card, select **Get it now**. 

    :::image type="content" source="media/get-enhanced-app.png" alt-text="Screenshot showing Copilot for Sales enhanced app in Microsoft 365 admin center.":::

    The AppSource window closes. You'll complete the remaining steps in the Microsoft 365 admin center.

6. In the **Configuration** step, select **Next**.

    :::image type="content" source="media/apps-to-deploy.png" alt-text="Screenshot showing apps to deploy.":::

8. In the **Users** step, select the users or groups who will have access to the app, and then select **Next**. Learn more about configuring users and groups at [Considerations when assigning an add-in to users and groups](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true#considerations-when-assigning-an-add-in-to-users-and-groups)

9. In the **Deployment** (**Permissions**) step, read the app permissions and capabilities, select **Accept permissions** for the app, and then select **Next**.

10. In the **Deployment** (**Finish**) step, review the selected settings, and then select **Finish deployment**.

11. When the deployment is complete, select **Done**.

    Allow up to six hours for Copilot for Sales to appear in users' Outlook ribbon.

> [!NOTE]
> The app is installed in Outlook and other Microsoft 365 applications but not in Teams. You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. For information about installing Copilot for Sales in Teams, go to [Install and pin Copilot for Sales in Teams](install-pin-viva-sales-teams.md).


> [!IMPORTANT]
> It can take up to 48 hours for the app to appear in Outlook and other Microsoft 365 apps. If users can't see the app after 48 hours, it might be due to the public attachment handling policy. More information: [Why can't users see the Copilot for Sales app in Outlook after it's deployed?](sales-copilot-faq.md#why-cant-users-see-the-copilot-for-sales-app-in-outlook-after-its-deployed)

## Manage the Copilot for Sales app

After you've installed Copilot for Sales as an integrated app, you can manage its configuration, add and remove users, and view its usage in the Microsoft 365 admin center.

1.  In the [Microsoft 365 admin center](https://admin.microsoft.com/), select **Settings** &gt; **Integrated apps**.

2.  On the **Integrated apps** page, select the **Microsoft 365 Copilot for Sales** app.

The **Microsoft 365 Copilot for Sales** panel opens with the following tabs:

- **Overview**: Displays basic information about the add-in, deployed apps, and assigned users. If Copilot for Sales was previously deployed from the Microsoft 365 admin center, the **Merge both versions** button is shown. Select **Merge both versions** to upgrade the app to the latest version.

- **Configuration**: Allows you to remove the app from a selected product. To remove the app, select it, and then select **Remove**.

- **Users**: Allows you to edit the users who can use the app.

- **Usage**: Displays the number of active users of the app based on the selected platform and date range.

## Update the Copilot for Sales app

1.  In the [Microsoft 365 admin center](https://admin.microsoft.com/), select **Settings** &gt; **Integrated apps**.

2.  On the **Integrated apps** page, select the **Microsoft 365 Copilot for Sales** app.

    The **Microsoft 365 Copilot for Sales** panel opens. If there's an update available for the add-in, a message is displayed in the **Overview** tab.

3. Select **Know more and update**.

4. In the **Updates** panel, select **Accept and update**.

## User-deployed app installation

End users can install the Outlook add-in and Teams app from within Microsoft AppSource in Outlook or Teams respectively, as long as they aren't explicitly blocked by the administrator.  

If end users install the Outlook add-in, it's considered user-deployed instead of admin-deployed and will not have full feature support. User-deployed apps don't support Copilot for Sales banner notifications that appear within the top of new or reply emails. Also, the Copilot for Sales is not added automatically to meeting invites. However, sellers can manually add Copilot for Sales to the meeting to get meeting summaries.

### See also

[Install and pin Copilot for Sales in Teams](install-pin-viva-sales-teams.md)
