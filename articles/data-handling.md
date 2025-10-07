---
title: Data handling in Sales solution in Microsoft 365 Copilot 
description: Know how data is handled in Copilot for Sales 
ms.date: 09/24/2025
ms.topic: concept-article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Data handling in Sales solution in Microsoft 365 Copilot

This article gives you an overview of how data is handled in Sales solution.

Sales solution is built on the [Microsoft Power Platform](https://powerplatform.microsoft.com/) and data is stored in [Microsoft Dataverse](/powerapps/maker/common-data-service/data-platform-intro) in addition to the connected CRM.

## Data retention

Since Sales solution data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro), data retention policies differ from other Microsoft 365 applications and non-Dynamics 365 CRM solutions. For example, when your Microsoft 365 subscription ends, your data is retained for 90 days before it's automatically deleted (in accordance to [Microsoft 365 data retention policies](/microsoft-365/compliance/retention-policies)). However, if you use Sales solution, that data isn't automatically deleted 90 days after your subscription ends.

## Copilot for Sales, Dataverse, and your CRM

When Copilot for Sales is connected to Dynamics 365, Copilot for Sales data is stored with the Dynamics 365 Sales Dataverse instance.

When Copilot for Sales is connected to a non-Dynamics 365 CRM, a default Dataverse instance specific to Copilot for Sales is provided to your tenant. Copilot for Sales data is stored in the default instance in addition to your CRM.

You can find the name and details of your default Dataverse instance named **msdyn_viva** in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

> [!IMPORTANT]
> - The **msdyn_viva** environment is of type **Trial**. If you need to convert the environment to **Production**, follow the steps in the [Convert the Copilot for Sales environment from Trial to Production](convert-trial-prod.md) article.
> - Do not remove or edit the **msdyn_viva** environment because it is holds important data for Copilot for Sales. If the environment is removed or edited, Copilot for Sales might stop working.

:::image type="content" source="media/ppac-admin-center.png" alt-text="Screenshot that shows the default Dataverse instance in Power Platform admin center.":::

### Where is the data stored?

Copilot for Sales data is stored in several tables in Dataverse. You should not modify or use these tables directly. They are used by Copilot for Sales features and agents to store and retrieve the insights and data needed to provide the Copilot for Sales experience. The tables used for storing insights are:

|Table name|Description|
|---|---|
|**msdyn_rawinsight**|This table contains insights from communications with customers such as emails and meetings, if the corresponding features are enabled. This includes information such as meeting summaries, objections raised, and questions asked.|
|**msdyn_rawinsightentitylink**|This table contains links between insights and relevant CRM records.|
|**Lead Intelligence Insight**|This table contains insights by the Sales Agent about the leads found in the CRM.|

Insights related to emails and meetings have a retention policy of 90 days, and will be deleted afterwards. If a customer requires custom retention policy, scripts can be created to delete the data from the table.

## Delete Copilot for Sales data

If you need to delete Copilot for Sales data (for example, delete data for a specific user), you can choose to [manually delete it](/power-platform/admin/remove-user-personal-data).

### Related information

[Introduction to Sales solution in Microsoft 365 Copilot](introduction.md)<br>
[Install Sales app](install-viva-sales.md)
