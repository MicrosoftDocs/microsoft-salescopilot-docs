---
title: Convert the Dynamics 365 environment from Trial to Production
description: Learn how to convert the Dynamics 365 environment from Trial to Production.
ms.date: 02/24/2026
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Convert the Dynamics 365 environment from Trial to Production

In certain situations, the Power Platform environment used for the Sales app is of a Trial type. 

If you are using Dynamics 365 and the environment in Dynamics 365 is of type Trial, the Sales app is connected to the trial environment.

You can find the name and details of your environment in the **Environments** section of the [Power Platform admin center](https://admin.powerplatform.microsoft.com/). The type of the environment is shown in the **Type** column.

To use Sales Agent - Lead Research, you must convert the trial environment to production in which the Sales app is deployed. You can also convert the environment to production for other reasons such as using the features available in production environment.

> [!NOTE]
> If you're using Salesforce as your CRM and want to convert your **msdyn_viva** trial environment to a production environment to use **Sales Agent - Lead Research**, follow the instructions in [Set up Sales Agent - Lead Research](set-up-sales-agent.md#step-3-set-up-and-activate-the-agent).

## Convert the environment from Trial to Production

You must be a Power Platform admin to convert the environment.

If the Dynamics 365 environment is of type Trial, the Sales app is connected to the trial environment.

1. Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/).
1. Go to **Environments** and the select the trial environment.
1. On the command bar at the top, select **Convert to production**.
1. Select **Continue**.

It might take several hours to convert to a production environment. Learn more about [converting a trial environment to production](/power-platform/admin/trial-environments#convert-either-type-of-trial-environment-to-a-production-environment).

## Set up billing options for Sales Agent - Lead Research

If you've converted the environment to use Sales Agent - Lead Research, you must set up billing options. Learn more about [managing consumption-based billing for agent capabilities](manage-consumption-based-billing.md).