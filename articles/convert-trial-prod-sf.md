---
title: Convert the msdyn_viva environment from Trial to Production
description: Learn how to convert the msdyn_viva environment from Trial to Production.
ms.date: 05/28/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Convert the msdyn_viva environment from Trial to Production

In certain situations, the Power Platform environment used for Copilot for Sales is of a Trial type.

If you are using a non-Dynamics 365 CRM, such as Salesforce, Copilot for Sales creates a trial Power Platform environment to store settings and some data for the running of the app. The name of the environment is **msdyn_viva**. You can find the name and details of your environment in the **Environments** section of the [Power Platform admin center](https://admin.powerplatform.microsoft.com/). The type of the environment is shown in the **Type** column.

:::image type="content" source="media/ppac-admin-center.png" alt-text="Screenshot that shows the default Dataverse instance in Power Platform admin center.":::

To use Sales Agent, you must convert the trial environment to production in which Copilot for Sales is deployed.  You can also convert the environment to production for other reasons such as using the features available in production environment.

## Convert the environment from Trial to Production

You must be a Power Platform admin to convert the environment.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. Go to **Environments** and then select the environment named **msdyn_viva**.
1. On the command bar at the top, select **Convert to production**.
1. Select **Continue**.

It might take up to 20 minutes or longer in some cases to convert the environment. 

After the environment is converted to production, you must assign the Viva Sales role to the default team in the environment.

## Assign the Viva Sales role to the default team

You must assign the Viva Sales role to the default team in the environment. The default team is usually the one with administrator other than SYSTEM.

1. In the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), select the **msdyn_viva** environment.
1. On the **Access** card, under **Teams**, select **See all**.
1. Find the default team. Usually the default team is the one with administrator other than SYSTEM.
1. Select **More team actions** (vertical ellipsis) and then select **Manage security roles**.
1. In the **Manage security roles** pane, select **Viva Sales**, and then select **Save**.

## Set up billing options for Sales Agent

If you've converted the environment to use Sales Agent, you must set up billing options.