---
title: Error after connecting and signing in to Salesforce CRM
description: Troubleshoot and resolve error messages in Viva Sales related to error message after connecting and signing in to Salesforce CRM.
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

# Error after connecting and signing in to Salesforce CRM

This article helps you troubleshoot and resolve error messages in Viva Sales related to users connecting and signing into Salesforce. 

## Who is affected?

|  |  |
|---------|---------|
|**Client app**     |  Viva Sales Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Salesforce      |
|**Users**     | All users |

## Symptom

After a user signs in to Salesforce CRM, the following error message is displayed in the Viva Sales Outlook add-in:

:::image type="content" source="media/tsg-api-perm-error.png" alt-text="API permission error":::

## Root cause and resolution

### Issue 1: Viva Sales displays an error stating the REST API isn't enabled for this organization 

#### Root cause

The issue occurs when the user doesn't have API Permissions in Salesforce. You can confirm if this is the root cause of the issue if you see the following error in the logs:

```
Exception thrown in VivaSalesContacts/GetContactsByEmailAddress - 
Microsoft.SalesProductivity.Common.Base.SPServiceException: Salesforce failed to complete task: Message: entity is deleted clientRequestId: 000000000-aaaa-4545-8383-00bf00f10000-self ---> 
System.Exception: { 
    "error": { 
        "code": 502, 
        "source": "xxy-001.azure-apim.net", 
        "message": "BadGateway", 
        "innerError": { 
            "status": 502, 
            "message": "Salesforce failed to complete task: Message: **API is disabled for this User**\r\nclientRequestId: 000000000-aaaa-4545-8383-00bf00f10000-self", 
            "error": null, 
            "source": "Salesforce.Common", 
            "errors": [] 
        } 
    } 
} 
```

#### Resolution

You must be a Salesforce administrator to resolve the issue.

1. In Salesforce **Setup**, open the profile assigned to the Viva Sales user, and then select **Edit**.
2. In the **Administrative Settings** section, select **API Enabled**. 
3. Select **Save**.

## Is your issue still not resolved?

Visit the [Viva Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.
