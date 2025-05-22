---
title: Convert the Dynamics 365 environment from Trial to Production
description: Learn how to convert the Dynamics 365 environment from Trial to Production.
ms.date: 05/28/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Convert the Dynamics 365 environment from Trial to Production

In certain situations, the Power Platform environment used for Copilot for Sales is of a Trial type. 

If you are using Dynamics 365 and the environment in Dynamics 365 is of type Trial, the Copilot for Sales app is deployed in the trial environment. You can find the name and details of your environment in the **Environments** section of the [Power Platform admin center](https://admin.powerplatform.microsoft.com/). The type of the environment is shown in the **Type** column.

:::image type="content" source="media/ppac-admin-center.png" alt-text="Screenshot that shows the default Dataverse instance in Power Platform admin center.":::

To use Sales Agent, you must convert the trial environment to production in which Copilot for Sales is deployed. You can also convert the environment to production for other reasons such as using the features available in production environment.

## Convert the environment from Trial to Production

You must be a Power Platform admin to convert the environment.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. Go to **Environments** and the select the trial environment.
1. On the command bar at the top, select **Convert to production**.
1. Select **Continue**.

It might take up to 20 minutes or longer in some cases to convert the environment.

## Set up billing options for Sales Agent

If you've converted the environment to use Sales Agent, you must set up billing options.