---
title: Missing privileges in Dynamics 365
description: Troubleshoot and resolve error messages in Copilot for Sales related to missing privileges in Dynamics 365.
ms.date: 01/09/2024
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Missing privileges in Dynamics 365

This article helps you troubleshoot and resolve error messages in Copilot for Sales related to missing privileges in Dynamics 365.

## Who is affected?

| Requirement type |Description  |
|---------|---------|
|**Client app**     |  Copilot for Sales Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Dynamics 365        |
|**Users**     | Users who don't have Copilot for Sales privileges in Dynamics 365   |

## Symptom

When Dynamics 365 users try to sign in to Copilot for Sales, an error message is displayed indicating that they're missing certain privileges.

## Root cause and resolution

### Issue 1: User doesn't have Copilot for Sales privileges in Dynamics 365

#### Root cause

Users are missing privileges granted by the **Copilot for Sales User** role. 

#### Resolution

You must assign the [additional privileges required for Dynamics 365 customers](install-viva-sales.md#additional-privileges-required-for-dynamics-365-customers) to resolve the issue. 

## Is your issue still not resolved?

Visit the [Copilot for Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.
