---
title: Unable to update records when connected to Salesforce CRM
description: Troubleshoot and resolve error issues when users are unable to update records in Sales Copilot when connected to Salesforce CRM.
ms.date: 08/22/2023
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

This article helps you troubleshoot and resolve issues when users are unable to update records in Sales Copilot when connected to Salesforce CRM.

## Who is affected?

|  |  |
|---------|---------|
|**Client app**     |  Sales Copilot Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Salesforce      |
|**Users**     | Users trying to update a record in Sales Copilot |

## Symptom

When trying to update a CRM record from the Sales Copilot add-in for Outlook, the following error message is displayed: `Can't update Salesforce because you don't have edit access for this record.`

:::image type="content" source="media/tsg-update-record.png" alt-text="Error about unable to update records in Salesforce.":::

## Root cause and resolution

### Issue 1: User doesn't have Write access to an entity in Salesforce

#### Root cause

When a user tries to edit an entity, Sales Copilot checks if the user has **Write** access to the entity in Salesforce. If the user doesn't have **Write** access to the entity, the error message is displayed.

You can confirm if the user not having **Write** access to the entity is the root cause of issue if you see the following error in the logs:

```
Exception thrown in VivaSalesContacts/UpdateContact - 
Microsoft.SalesProductivity.Common.Base.SPServiceException: Salesforce failed to complete task: Message: entity is deleted clientRequestId: 01665660-aeb5-45fe-83d3-59bf69f1e85e-self ---> 
System.Exception: { 
    "status": 400, 
    "message": "Object type contact is not supported. If you are attempting to use a custom object, be sure to append the '__c' after the entity name. 
                Please reference your WSDL or the describe call for the appropriate names\r\nclientRequestId: <CLIENT REQUEST ID>-self", 
    "error": null, 
    "source": "Salesforce.Common", 
    "errors": [] 
}

```

In the above error message, the `Object type contact is not supported` indicates that the user doesn't have **Write** access to the Contact entity.

#### Resolution

To resolve the issue, ensure that the user has:

- Read/write level permissions to the entity which the user is trying to edit in Salesforce
- Read/write permissions on all of the fields configured for editing
- Access to the specific record that the user is trying to edit

For information about object-level security, field-level security, and record-level security in Salesforce, see [Control Who Sees What](https://help.salesforce.com/s/articleView?id=sf.security_data_access.htm&type=5). You can also contact your Salesforce administrator for help in setting permissions correctly.

## Is your issue still not resolved?

Visit the [Sales Copilot - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.