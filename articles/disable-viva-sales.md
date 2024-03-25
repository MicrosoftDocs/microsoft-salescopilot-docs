---
title: Uninstall Copilot for Sales add-in for Outlook
description: Uninstall Copilot for Sales add-in for Outlook using Microsoft 365 admin center or PowerShell.
ms.date: 03/23/2024
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

# Uninstall Copilot for Sales add-in for Outlook

You can uninstall the Copilot for Sales add-in for Outlook using the Microsoft 365 admin center or PowerShell.

## Uninstall using Microsoft 365 admin center

If you've installed the Copilot for Sales add-in for Outlook from the Microsoft 365 admin center, it is considered as admin-deployed. You can remove the Copilot for Sales add-in if your sellers no longer need it.

1.  In the Microsoft 365 admin center, go to **Settings** &gt; **Integrated apps**.

2.  Select **Microsoft Copilot for Sales** and then select the **Configuration** tab.

3. Select the app to be removed and then select **Remove**.

4.  Confirm about your choice and then select **Remove**.

5. When the app is successfully removed, select **Done**.

## Uninstall using PowerShell

If the Copilot for Sales add-in for Outlook was installed automatically for your organization or sellers have installed it themselves, you can use PowerShell to remove it.

> [!NOTE]
> - You must be a tenant administrator to run PowerShell scripts.
> - PowerShell scripts must be used only to uninstall user-deployed add-ins. If you run these scripts to uninstall admin-deployed add-ins, an error message is displayed.

### Uninstall for individual user

```powershell
Install-Module -Name ExchangeOnlineManagement
Import-Module ExchangeOnlineManagement

# Copilot for Sales app id
$appIdentity = "c3b456a3-a41a-4ed4-8040-354f73574021"

Connect-ExchangeOnline -UserPrincipalName <tenant admin email>

Remove-App -Mailbox <user alias to delete from> -Identity $appIdentity -Confirm:$false
```

### Uninstall for all users


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