---
title: Missing privileges in Dynamics 365
description: Troubleshoot and resolve error messages in Viva Sales related to related to missing privileges in Dynamics 365.
ms.date: 07/18/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Missing privileges in Dynamics 365

This article helps you troubleshoot and resolve error messages in Viva Sales related to missing privileges in Dynamics 365.

## Who is affected?

|  |  |
|---------|---------|
|**Client app**     |  Viva Sales Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Dynamics 365        |
|**Users**     | Users who do not have Viva Sales privileges in Dynamics 365   |

## Symptom

When Dynamics 365 users try to sign in to Viva Sales, an error message is displayed indicating that they are missing certain privileges.

## Root cause and resolution

### Issue 1: User doesn't have Viva Sales privileges in Dynamics 365

#### Root cause

Users are missing privileges granted by the **Viva Sales User** role. 

#### Resolution

You must assing the [additional privileges required for Dynamics 365 customers](install-viva-sales.md#additional-privileges-required-for-dynamics-365-customers) to resolve the issue. 

## Is your issue still not resolved?

Visit the [Viva Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.
