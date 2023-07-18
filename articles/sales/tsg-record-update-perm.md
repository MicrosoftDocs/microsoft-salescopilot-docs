---
title: Unable to update records when connected to Salesforce CRM
description: Troubleshoot and resolve error messages in Sales Copilot related to users who are unable to update records in Sales Copilot when connected to Salesforce CRM.
ms.date: 06/18/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Unable to update records in Sales Copilot when connected to Salesforce CRM

[!INCLUDE[vs-rebrand-note](../includes/vs-rebrand-note.md)]

This article helps you troubleshoot and resolve error messages in Sales Copilot related to users unable to update records in Sales Copilot when connected to Salesforce CRM.

## Who is affected?

|  |  |
|---------|---------|
|**Client app**     |  Sales Copilot Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Salesforce      |
|**Users**     | All users |

## Symptom

When trying to update a CRM record from the Sales Copilot add-in for Outlook, an error message is displayed saying that Salesforce can't be updated due to lack of edit access for this record.

:::image type="content" source="media/tsg-update-record.png" alt-text="Error about updating records in Salesforce.":::

## Root cause and resolution

### Issue 1: User cannot update a record in Salesforce CRM due to missing edit access for a given record

#### Root cause

User is missing the **Edit** access to the object in Salesforce.

#### Resolution

You must provide the **Edit** access to the object in Salesforce. More information: [Edit Object Permissions in Profiles](https://help.salesforce.com/s/articleView?id=sf.perm_sets_object_perms_edit.htm&type=5)

## Is your issue still not resolved?

Visit the [Sales Copilot - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.