---
title: Uninstall the Microsoft 365 Copilot for Sales app
description: Uninstall the Microsoft 365 Copilot for Sales app using Microsoft 365 admin center or PowerShell.
ms.date: 09/29/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:10/17/2023
---

# Uninstall the Microsoft 365 Copilot for Sales app

You can uninstall the Copilot for Sales app from your organization or for individual users. The steps to uninstall the app depend on whether you are an admin or a user.

## Uninstall as a user

You can uninstall the Copilot for Sales app from either Microsoft Outlook or Microsoft Teams. Uninstalling the app from one location uninstalls it from all locations.

1. Sign in to Microsoft Outlook or Microsoft Teams.  

1. In the navigation bar on the left, right-click the Copilot for Sales app, and then select **Uninstall**.  

    > [!NOTE]
    > If there's no option to uninstall the app, it's likely that the app was installed by your administrator.

## Uninstall as an admin

As as admin, you can uninstall the Copilot for Sales add-in for Outlook using the Microsoft 365 admin center or PowerShell. 

For the Copilot for Sales app in Teams, you can either remove the remove the group policy assignment or block the app if your sellers no longer need it.

### Uninstall Copilot for Sales Outlook add-in using Microsoft 365 admin center

If you've installed the Copilot for Sales add-in for Outlook from the Microsoft 365 admin center, it is considered as admin-deployed. You can remove the Copilot for Sales add-in if your sellers no longer need it.

1. In the Microsoft 365 admin center, go to **Settings** &gt; **Integrated apps**.  
1. Select **Copilot for Sales** and then select the **Configuration** tab.  
1. Select the app to be removed and then select **Remove**.  
1. Confirm about your choice and then select **Remove**.  
1. When the app is successfully removed, select **Done**.

### Uninstall Copilot for Sales Outlook add-in using PowerShell

If the Copilot for Sales add-in for Outlook was installed automatically for your organization or sellers have installed it themselves, you can use PowerShell to remove it.

> [!NOTE]
>
> - You must be a tenant administrator to run PowerShell scripts.  
> - PowerShell scripts can only be used to uninstall user-deployed add-ins. If you run these scripts to uninstall admin-deployed add-ins, an error message is displayed.
> - To remove the older Sales Copilot add-in, use the app ID `c3b456a3-a41a-4ed4-8040-354f73574021`. If the older add-in is not found, it might have been updated to the enhanced Teams app. In that case, use the app ID `c92c289e-ceb4-4755-819d-0d1dffdab6fa`.

#### Uninstall for individual user

```powershell
Install-Module -Name ExchangeOnlineManagement
Import-Module ExchangeOnlineManagement

# Copilot for Sales app id
$appIdentity = "c3b456a3-a41a-4ed4-8040-354f73574021"

Connect-ExchangeOnline -UserPrincipalName <tenant admin email>

Remove-App -Mailbox <user alias to delete from> -Identity $appIdentity -Confirm:$false
```

#### Uninstall for all users


```powershell
Install-Module -Name ExchangeOnlineManagement
Import-Module ExchangeOnlineManagement

# Copilot for Sales app id
$appIdentity = "c3b456a3-a41a-4ed4-8040-354f73574021"

Connect-ExchangeOnline -UserPrincipalName <tenant admin email>

Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | ForEach-Object { Remove-App -Mailbox $_.Identity -Identity $appIdentity -Confirm:$false }
```

### Uninstall Copilot for Sales app from Microsoft Teams

You can't delete or uninstall the Copilot for Sales app in Teams. You can either remove the group policy assignment, block the app, or change the app's availability if your sellers no longer need it.

#### Remove the group policy assignment

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard).
1. In the left pane, select **Teams apps** &gt; **Setup policies**.
1. On the **Group policy assignment** tab, select the group policy assignment that includes the Copilot for Sales app.
1. Select **Remove**.
1. Select **Confirm**.

#### Block the app

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard).
1. In the left pane, go to **Teams apps** &gt; **Manage apps**.
1. Select the app to open its details.
1. Select Actions at the top-right, and then select **Block app**.

#### Change the app's availability

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard).
1. In the left pane, go to **Teams apps** &gt; **Manage apps**.  
1. Select the check mark to the left of Copilot for Sales in the app list, and then select **Edit availability**. 
1. In the **Edit availability** pane, select **No one** from the **Available to** list.

