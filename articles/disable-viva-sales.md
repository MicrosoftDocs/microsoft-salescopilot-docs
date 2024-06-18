---
title: Uninstall Copilot for Sales app
description: Uninstall Copilot for Sales app using Microsoft 365 admin center or PowerShell.
ms.date: 05/08/2024
ms.topic: article
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

# Uninstall Copilot for Sales app

You can uninstall the Copilot for Sales app from your organization or for individual users. The steps to uninstall the app depend on whether you are an admin or a user.

## Uninstall as a user

You can uninstall the Copilot for Sales add-in for Outlook and the Copilot for Sales personal app from Microsoft Teams.

### Uninstall Copilot for Sales Outlook add-in

1. Open [https://aka.ms/olksideload](https://aka.ms/olksideload). If required, sign in to your Microsoft Outlook account.

1. In the **Add-Ins for Outlook** window, select **My add-ins** in the left pane.

1. On the **Copilot for Sales for Microsoft Outlook** card, select **Manage Add-In** (**...**) at the bottom-right, and then select **Remove**.

> [!NOTE]
> If there's no option to uninstall the add-in, it's likely that the add-in was installed by your administrator. Contact your administrator to uninstall the add-in. To know if the add-in is admin-deployed or user-deployed, see [How do I know if the Copilot for Sales add-in for Outlook is admin-deployed or user-deployed?](install-sales-copilot.md#how-do-i-know-if-the-copilot-for-sales-add-in-for-outlook-is-admin-deployed-or-user-deployed).

### Uninstall Copilot for Sales app from Microsoft Teams

1. Sign in to Microsoft Teams.

1. In the navigation bar on the left, select **Store**.

1. At the bottom of the **Apps** sidebar, select **Manage your apps**.

1. Find the Copilot for Sales app and select it to expand its row.

1. Select **Remove** :::image type="content" source="media/trash.png" alt-text="Delete team trash can button."::: for the personal app and confirm you want to remove the app from the selected location.

## Uninstall as an admin

As as admin, you can uninstall the Copilot for Sales add-in for Outlook using the Microsoft 365 admin center or PowerShell.

### Uninstall using Microsoft 365 admin center

If you've installed the Copilot for Sales add-in for Outlook from the Microsoft 365 admin center, it is considered as admin-deployed. You can remove the Copilot for Sales add-in if your sellers no longer need it.

1.  In the Microsoft 365 admin center, go to **Settings** &gt; **Integrated apps**.

2.  Select **Microsoft Copilot for Sales** and then select the **Configuration** tab.

3. Select the app to be removed and then select **Remove**.

4.  Confirm about your choice and then select **Remove**.

5. When the app is successfully removed, select **Done**.

### Uninstall using PowerShell

If the Copilot for Sales add-in for Outlook was installed automatically for your organization or sellers have installed it themselves, you can use PowerShell to remove it.

> [!NOTE]
> - You must be a tenant administrator to run PowerShell scripts.
> - PowerShell scripts can only be used to uninstall user-deployed add-ins. If you run these scripts to uninstall admin-deployed add-ins, an error message is displayed.
> - To remove the older Sales Copilot add-in, use the app ID `c92c289e-ceb4-4755-819d-0d1dffdab6fa`. If the older add-in is not found, it might have been updated to the enhanced Teams app. In that case, use the app ID `c92c289e-ceb4-4755-819d-0d1dffdab6fa`.

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

### See also

[Block the Copilot for Sales app in Teams](block-viva-sales-app-teams.md)<br>
[Check if the Copilot for Sales add-in for Outlook is admin-deployed or user-deployed](install-sales-copilot.md#how-do-i-know-if-the-copilot-for-sales-add-in-for-outlook-is-admin-deployed-or-user-deployed)