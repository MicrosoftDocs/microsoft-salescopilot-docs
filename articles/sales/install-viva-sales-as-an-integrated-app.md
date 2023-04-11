---
title: Install Viva Sales add-in for Outlook
description: Learn how to install Viva Sales add-in for Outlook from Microsoft 365 admin center.
ms.date: 04/05/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Install Viva Sales add-in for Outlook

The add-in is installed in Fixed mode by default. In a Fixed deployment, users receive the add-in automatically and can't remove it.

1.  Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/).

2.  In the left pane, select **Settings** &gt; **Integrated apps**.

3.  On the **Integrated apps** page, select **Get apps**.

    Microsoft AppSource opens in an embedded window.

4.  In the **AppSource** window, search for **Viva Sales**.

5.  In the search results, select either **Viva Sales for Microsoft Outlook** or **Viva Sales for Microsoft Teams**, and then select **Get it now**. 

    The AppSource window closes. You'll complete the remaining steps in the Microsoft 365 admin center.

6.  In the **Configuration** step, select the apps to deploy, and then select **Next**.

7.  In the **Users** step, select the users or groups who will have access to the add-in, and then select **Next**.

8.  In the **Deployment** (**Permissions**) step, read the app permissions and capabilities for each of the apps to be deployed, select **Accept permissions** for each app, and then select **Next**.

9.  In the **Deployment** (**Finish**) step, review the selected settings, and then select **Finish deployment**.

10. When the deployment is complete, select **Done**.

> [!NOTE]
> The app is enabled in Teams but not installed. You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. For information about installing Viva Sales in Teams, go to [Install and pin Viva Sales in Teams](install-pin-viva-sales-teams.md).

Allow up to six hours for Viva Sales to appear in users' Outlook ribbon.

Sellers will receive a pop-up notification that their administrator has installed a new app.

## Manage the Viva Sales app

After you've installed Viva Sales as an integrated app, you can manage its configuration, add and remove users, and view its usage in the Microsoft 365 admin center.

1.  In the [Microsoft 365 admin center](https://admin.microsoft.com/), select **Settings** &gt; **Integrated apps**.

2.  On the **Integrated apps** page, select the Viva Sales app.

The **Microsoft Viva Sales** panel opens with the following tabs:

- **Overview**: Displays basic information about the add-in, deployed apps, and assigned users.

- **Configuration**: Allows you to remove the app from a selected product. To remove the app, select it, and then select **Remove**.

- **Users**: Allows you to edit the users who can use the app.

- **Usage**: Displays the number of active users of the app based on the selected platform and date range.

## Update the Viva Sales add-in

1.  In the [Microsoft 365 admin center](https://admin.microsoft.com/), select **Settings** &gt; **Integrated apps**.

2.  On the **Integrated apps** page, select the Viva Sales app.

    The **Microsoft Viva Sales** panel opens. If there's an update available for the add-in, a message is displayed in the **Overview** tab.

3. Select **Know more and update**.

    :::image type="content" source="media/update-add-in.png" alt-text="Update the Viva Sales add-in.":::

4. In the **Updates** panel, select **Accept and update**.

## User-deployed app installation

End users can install the Outlook add-in and Teams app from within Microsoft AppSource in Outlook or Teams respectively, as long as they aren't explicitly blocked by the administrator.  

If end users install the Outlook add-in, it's considered user-deployed instead of admin-deployed and will not have full feature support. User-deployed apps don't support Viva Sales banner notifications that appear within the top of new or reply emails. Also, the Viva Sales is not added automatically to meeting invites. However, sellers can manually add Viva Sales to the meeting to get meeting summaries.


