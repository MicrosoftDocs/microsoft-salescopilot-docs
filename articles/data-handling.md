---
title: Data handling in Copilot for Sales 
description: Know how data is handled in Copilot for Sales 
ms.date: 01/09/2024
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---


# Data handling in Copilot for Sales 



This article gives you an overview of how data is handled in Copilot for Sales.

Copilot for Sales is built on the [Microsoft Power Platform](https://powerplatform.microsoft.com/). Copilot for Sales data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) in addition to the connected CRM.

## Data retention 

Since Copilot for Sales data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro), data retention policies differ from other Microsoft 365 applications and non-Dynamics 365 CRM solutions. For example, when your Microsoft 365 subscription ends, your data is retained for 90 days before it's automatically deleted (in accordance to [Microsoft 365 data retention policies](/microsoft-365/compliance/retention-policies)). However, if you use Copilot for Sales, that data isn't automatically deleted 90 days after your subscription ends.  

## Copilot for Sales, Dataverse, and your CRM

When Copilot for Sales is connected to Dynamics 365, Copilot for Sales data is stored with the Dynamics 365 Sales Dataverse instance.

When Copilot for Sales is connected to a non-Dynamics 365 CRM, a default Dataverse instance specific to Copilot for Sales is provided to your tenant. Copilot for Sales data is stored in the default instance in addition to your CRM. 

You can find the name and details of your default Dataverse instance named **msdyn_viva** in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

> [!NOTE]
> The msdyn_viva environment is of type **Trial**. Do not convert the environment to **Production**.

:::image type="content" source="media/ppac-admin-center.png" alt-text="Screenshot that shows the default Dataverse instance in Power Platform admin center.":::

## Delete Copilot for Sales data 

If you need to delete Copilot for Sales data (for example, delete data for a specific user), you can choose to [manually delete it](/power-platform/admin/remove-user-personal-data). 

### See also

[Introduction to Microsoft Copilot for Sales](introduction.md)<br>
[Install Copilot for Sales](install-viva-sales.md)
