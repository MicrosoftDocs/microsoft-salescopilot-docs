---
title: Manage consumption-based billing
description: Learn about managing consumption-based billing for agent capabilities in Copilot for Sales.
ms.date: 06/04/2025
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Manage consumption-based billing for agent capabilities

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This article explains how to set up billing for Copilot and agent capabilities in Copilot for Sales.  

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

## Consumption-based billing

Selected Copilot and agent capabilities in Copilot for Sales use consumption-based billing, charging per use. These capabilities use Microsoft Copilot Studio messages for AI interactions and tasks, like retrieving information and responding to prompts. Messages are the billing units that measure usage. The number of messages per event depends on its complexity. Learn more about messages in [Message scenarios](/microsoft-copilot-studio/requirements-messages-management#message-scenarios).  

Learn more about billing and rates in [Power Platform Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130).

### Set up billing model

Copilot and agent capabilities in Copilot for Sales support two billing models: prepaid capacity and pay-as-you-go. The prepaid capacity model uses Copilot Studio message pack subscriptions, which are a licensing option for Microsoft Copilot Studio that you purchase in advance. The pay-as-you-go model charges for the actual number of messages consumed by agents during the month. Learn more in [Copilot licensing](/microsoft-copilot-studio/billing-licensing).

Both models require that you use a production Power Platform environment. [Learn more about converting a trial environment to a production environment](convert-trial-prod.md). 

> [!NOTE]
> Both billing models can be used on the Power Platform environment. Prepaid capacity is consumed first. Message capacity on the Power Platform environment is consumed by Copilot for Sales and other Microsoft services on the tenant.

### Set up prepaid capacity

Complete these tasks to set up the Power Platform environment for prepaid capacity.

1. Purchase a Copilot message pack subscription using the Microsoft 365 admin center or Partner Center.

   Learn more in [Manage self-service purchases and trials (for users)](/microsoft-365/commerce/subscriptions/manage-self-service-purchases-users) or [Manage self-service purchases and trials (for admin)](/microsoft-365/commerce/subscriptions/manage-self-service-purchases-admins).

1. Assign prepaid capacity to the Power Platform environment using the Power Platform admin center.

   Learn more in [Manage Capacity](/power-platform/admin/manage-copilot-studio-messages-capacity?tabs=new#manage-capacity).

    > [!NOTE]
    > If you are using a non-Dynamics 365 CRM, such as Salesforce, you must assign the prepaid capacity to the environment named **msdyn_viva**.

### Set up pay-as-you-go

To set up pay-as-you-go billing, you first need an active Azure subscription. Then, you link the subscription to your Power Platform environment using the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) or within [Power Apps](https://make.powerapps.com/).

Learn more in [Set up pay-as-you-go](/power-platform/admin/pay-as-you-go-set-up).

## Manage capacity and usage

You can view Copilot Studio message capacity and usage for prepaid capacity and pay-as-you-go in the Power Platform admin center. Learn more in [Manage Copilot Studio messages and capacity](/power-platform/admin/manage-copilot-studio-messages-capacity).

If the available capacity (quota) of your organization is low or depleted, it is important to take timely action by reallocating existing capacity or purchasing more capacity.

- For prepaid capacity, use the Power Platform admin center to allocate more capacity to the environment from the total available on the tenant. Learn more in [Manage capacity](/power-platform/admin/manage-copilot-studio-messages-capacity#manage-capacity). If there's no quantity to allocate, purchase more.
- For pay-as-you-go, use Microsoft Cost Management in the Azure portal to view detailed usage and adjust spending limits (budgets) to free up more capacity. Learn more in [View usage and billing information](/power-platform/admin/pay-as-you-go-usage-costs). If there's no quantity to allocate, purchase more.

> [!IMPORTANT]
> When the quota is depleted, the AI capability is unavailable until more capacity is added.

## Related information

- [Assign licenses and manage access to Copilot Studio](/microsoft-copilot-studio/requirements-licensing?tabs=web)  
- [Copilot Studio licensing](/microsoft-copilot-studio/billing-licensing)  
- [Disable or limit sharing of agents](/microsoft-copilot-studio/admin-sharing-controls-limits)  
- [Orchestrate copilot topics and actions with generative AI](/microsoft-copilot-studio/advanced-generative-actions)  