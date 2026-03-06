---
title: Data handling in Sales agent 
description: Know how data is handled in Sales agent 
ms.date: 01/20/2026
ms.topic: concept-article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Data handling in Sales agent

This article gives you an overview of how data is handled in Sales agent.

The Sales agent is built on the [Microsoft Power Platform](https://powerplatform.microsoft.com/) and data is stored in [Microsoft Dataverse](/powerapps/maker/common-data-service/data-platform-intro) in addition to the connected CRM.

## Data retention

Since the Sales agent data is stored in [Dataverse](/powerapps/maker/common-data-service/data-platform-intro), data retention policies differ from other Microsoft 365 applications and non-Dynamics 365 CRM solutions. For example, when your Microsoft 365 subscription ends, your data is retained for 90 days before it's automatically deleted (in accordance to [Microsoft 365 data retention policies](/microsoft-365/compliance/retention-policies)). However, if you use the Sales agent, that data isn't automatically deleted 90 days after your subscription ends.

## Sales agent, Dataverse, and your CRM

When the Sales agent is connected to Dynamics 365, the Sales agent data is stored with the Dynamics 365 Sales Dataverse instance.

When the Sales agent is connected to a non-Dynamics 365 CRM, a default Dataverse instance specific to the Sales agent is provided to your tenant. The Sales agent data is stored in the default instance in addition to your CRM.

You can find the name and details of your default Dataverse instance named **msdyn_viva** in the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

> [!IMPORTANT]
> - The **msdyn_viva** environment is of type **Trial**. If you need to convert the environment to **Production**, follow the steps in the [Convert the sales environment from Trial to Production](convert-trial-prod.md) article.
> - Don't remove or edit the **msdyn_viva** environment because it holds important data for the Sales agent. If the environment is removed or edited, the Sales agent might stop working.

:::image type="content" source="media/ppac-admin-center.png" alt-text="Screenshot that shows the default Dataverse instance in Power Platform admin center.":::

### Where is the data stored?

The Sales agent data is stored in several tables in Dataverse. You shouldn't modify or use these tables directly. They're used by the Sales agent features and agents to store and retrieve the insights and data needed to provide the Sales agent experience. The tables used for storing insights are:

|Table name|Description|
|---|---|
|**msdyn_rawinsight**|This table contains insights from communications with customers such as emails and meetings, if the corresponding features are enabled. This includes information such as meeting summaries, objections raised, and questions asked.|
|**msdyn_rawinsightentitylink**|This table contains links between insights and relevant CRM records.|
|**Lead Intelligence Insight**|This table contains insights by the Sales Agent about the leads found in the CRM.|

Insights related to emails and meetings have a retention policy of 90 days, and will be deleted afterwards. If a customer requires custom retention policy, scripts can be created to delete the data from the table.

## Additional Dataverse capacity

Dataverse environments used to store Sales agent data receive additional capacity entitlements: 3 MB of Database capacity and 3 MB of Log capacity per license.

## Delete the Sales agent data

If you need to delete the Sales agent data (for example, delete data for a specific user), you can choose to [manually delete it](/power-platform/admin/remove-user-personal-data).

### Related information

[Introduction to Sales agent](introduction.md)<br>
[Install the Sales agent](install-sales-app.md)
