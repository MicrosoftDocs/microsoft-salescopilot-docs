---
title: Convert the sales environment from Trial to Production
description: Learn how to convert the sales environment from Trial to Production.
ms.date: 09/24/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Convert the sales environment from Trial to Production

In certain situations, the Power Platform environment used for Sales app is of a Trial type. 

If you are using Dynamics 365 and the environment in Dynamics 365 is of type Trial, the Sales app is connected to the trial environment.

If you are using a non-Dynamics 365 CRM, such as Salesforce, Sales app creates a trial Power Platform environment to store settings and some data for the running of the app. The name of the environment is **msdyn_viva**.

You can find the name and details of your environment in the **Environments** section of the [Power Platform admin center](https://admin.powerplatform.microsoft.com/). The type of the environment is shown in the **Type** column.

:::image type="content" source="media/ppac-admin-center.png" alt-text="Screenshot that shows the default Dataverse instance in Power Platform admin center.":::

> [!WARNING]
> Do not remove or edit the **msdyn_viva** environment because it is holds important data for Sales app. If the environment is removed or edited, Sales app might stop working.

To use Sales Agent, you must convert the trial environment to production in which Sales app is deployed. You can also convert the environment to production for other reasons such as using the features available in production environment.

## Convert the environment from Trial to Production

You must be a Power Platform admin to convert the environment.

### Dynamics 365 environment

If you are using Dynamics 365 and the environment in Dynamics 365 is of type Trial, the Sales app app is connected to the trial environment.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. Go to **Environments** and the select the trial environment.
1. On the command bar at the top, select **Convert to production**.
1. Select **Continue**.

It might take several hours to convert to a production environment. Learn more about [converting a trial environment to production](/power-platform/admin/trial-environments#convert-either-type-of-trial-environment-to-a-production-environment).

### msdyn_viva environment

If you are using a non-Dynamics 365 CRM, such as Salesforce, Sales app creates a trial Power Platform environment named **msdyn_viva**.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. Go to **Environments** and then select the environment named **msdyn_viva**.
1. On the command bar at the top, select **Convert to production**.
1. Select **Continue**.

It might take several hours to convert to a production environment. Learn more about [converting a trial environment to production](/power-platform/admin/trial-environments#convert-either-type-of-trial-environment-to-a-production-environment).

After the environment is converted to production, you must assign the Viva Sales role to the default team in the environment.

To assign the role:

1. In the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), select the **msdyn_viva** environment.
1. On the **Access** card, under **Teams**, select **See all**.
1. Find the default team. Usually the default team is the one with administrator other than SYSTEM.
1. Select **More team actions** (vertical ellipsis) and then select **Manage security roles**.
1. In the **Manage security roles** pane, select **Viva Sales**, and then select **Save**.

## Set up billing options for Sales Agent

If you've converted the environment to use Sales Agent, you must set up billing options. Learn more about [managing consumption-based billing for agent capabilities](manage-consumption-based-billing.md).