---
title: Uninstall Sales Copilot add-in for Outlook
description: Uninstall Sales Copilot add-in for Outlook using Microsoft 365 admin center or PowerShell.
ms.date: 10/17/2022
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:10/17/2023
---

# Uninstall Sales Copilot add-in for Outlook

You can uninstall the Sales Copilot add-in for Outlook using the Microsoft 365 admin center or PowerShell.

## Uninstall using Microsoft 365 admin center

If you've installed the Sales Copilot add-in for Outlook from the Microsoft 365 admin center, it is considered as admin-deployed. You can remove the Sales Copilot add-in if your sellers no longer need it.

1.  In the Microsoft 365 admin center, go to **Settings** &gt; **Integrated apps**.

2.  Select **Microsoft Sales Copilot** and then select the **Configuration** tab.

3. Select the app to be removed and then select **Remove**.

4.  Confirm about your choice and then select **Remove**.

5. When the app is successfully removed, select **Done**.

## Uninstall using PowerShell

If the Sales Copilot add-in for Outlook was installed automatically for your organization or sellers have installed it themselves, you can use PowerShell to remove it.

### Uninstall for individual user

```powershell
Install-Module -Name ExchangeOnlineManagement
Import-Module ExchangeOnlineManagement

# Sales copilot app id
$appIdentity = "c3b456a3-a41a-4ed4-8040-354f73574021"

Connect-ExchangeOnline -UserPrincipalName <tenant admin email>

Remove-App -Mailbox <user alias to delete from> -Identity $appIdentity -Confirm:$false
```

### Uninstall for all users


```powershell
Install-Module -Name ExchangeOnlineManagement
Import-Module ExchangeOnlineManagement

# Sales copilot app id
$appIdentity = "c3b456a3-a41a-4ed4-8040-354f73574021"

Connect-ExchangeOnline -UserPrincipalName <tenant admin email>

Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | ForEach-Object { Remove-App -Mailbox $_.Identity -Identity $appIdentity -Confirm:$false }
```

### See also

[Block the Sales Copilot app in Teams](block-viva-sales-app-teams.md)