---
title: Allow users to manage environments
description: Troubleshoot and resolve error messages in Viva Sales related to signing in to Salesforce.
ms.date: 04/20/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Allow users to manage environments

This article helps you troubleshoot and resolve error messages in Viva Sales related to signing in to Salesforce.

## Who is affected?

|  |  |
|---------|---------|
|**Client app**     |  Viva Sales Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Salesforce        |
|**Users**     | First user who tries to sign-in to Salesforce from Viva Sales   |

## Symptom

When first user in an organization tries to sign-in to Salesforce from Viva Sales, they see the following error message `To use this app, ask your Power Platform admin to let you use Viva Sales, and include the error details in your request.`

## Root caue and resolution

### Root cause

Tenant's administrators have disabled trial environment creation for non-administrator users. 

### Resolution

As a tenant administrator, allow users to create trial environments.

1. Sign in to [Power Platform admin center](https://admin.powerplatform.microsoft.com/) with your administrator credentials.
2. In the left navigaion pane, select **Settings**.
3. On the **Tenant settings** page, select **Trial environment assignments**.
4. In the **Trial environment assignments** panel, select **Everyone**.
5. Select **Save**.

## Is your issue still not resolved?

Visit the [Viva Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.