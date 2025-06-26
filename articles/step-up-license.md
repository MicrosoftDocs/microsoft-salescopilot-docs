---
title: Understand the Copilot for Sales step-up license
description: Learn how to assign Copilot for Sales step-up licenses and upgrade from the Microsoft 365 Copilot license.
ms.date: 06/26/2025
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/17/2024
---

# Understand the Copilot for Sales step-up license

If you have the Copilot for Sales step-up license, you can upgrade from the Microsoft 365 Copilot license to the Copilot for Sales license that offers sales-related insights and capabilities.  
The step-up license is a fractional license, not a standalone license. Therefore, it requires a Microsoft 365 Copilot license when it's added to the tenant.  
This article guides you through the process of assigning Copilot for Sales step-up licenses to your existing Microsoft 365 Copilot licenses.

> [!IMPORTANT]
> A step-up license automatically upgrades the prerequisite license to the full license. Therefore, the Copilot for Sales step-up license automatically upgrades the Microsoft 365 Copilot license to a Copilot for Sales license. As a result, the number of available Microsoft 365 Copilot licenses in the tenant is reduced.
> For example, Contoso has 1,000 Microsoft 365 Copilot licenses, 200 of which aren't assigned to users. Contoso plans to deploy 300 Copilot for Sales licenses. In this scenario, Contoso can buy 200 Copilot for Sales step-up licenses and 100 standalone Copilot for Sales licenses. The 200 unassigned Microsoft 365 Copilot licenses are converted to Copilot for Sales licenses. A Contoso admin can then assign the 300 Copilot for Sales licenses to selected users.

## Prerequisites

Before you add Copilot for Sales step-up licenses to your tenant, ensure that the following prerequisites are met:

- You have the required number of Copilot for Sales step-up licenses.
- The required number of Microsoft 365 Copilot licenses is available in your tenant. Follow these steps to verify the availability of Microsoft 365 Copilot licenses:  
    1. Open the [Microsoft 365 admin center](https://admin.microsoft.com/).
    1. On the left navigation pane, select **Billing** > **Licenses**.
    1. Confirm that you have enough available Microsoft 365 Copilot licenses for the users who need access to Copilot for Sales.

    > [!NOTE]
    > - The unassigned Microsoft 365 Copilot licenses are the ones that you can upgrade to Copilot for Sales licenses. Therefore, ensure that the number of available Microsoft 365 Copilot licenses matches the number of step-up licenses that you need.
    > - The expiry date of the available and unassigned Microsoft 365 Copilot licenses should be the same as or later than the expiry date of the Copilot for Sales step-up licenses.

If these prerequisites aren't met, and you don't have enough available Microsoft 365 Copilot licenses, you can buy the full [Copilot for Sales licenses](buy-license.md).

> [!IMPORTANT]
> - If you already assigned Microsoft 365 Copilot licenses to users in your tenant, and there aren't enough available and unassigned licenses for the step-up license, the process continues by removing the standalone allocation to complete the upgrade to a full Copilot for Sales license. This action reduces the number of available standalone Microsoft 365 Copilot licenses and might cause a discrepancy between the available licenses and assigned licenses. In this case, you receive a message that indicates over-allocation.
> - No Copilot for Sales license is assigned to a user without intervention from the admin team. An alert message indicates that the number of licenses that are assigned to users exceeds the number of licenses that are available for standalone Microsoft 365 Copilot. The license count for Copilot for Sales increases to the number of step-up licenses that are added. If this situation arises, and you want to reassign those licenses, go to the [Frequently asked questions](#frequently-asked-questions) section.

## Add Copilot for Sales step-up licenses

1. Open the [Microsoft 365 admin center](https://admin.microsoft.com/).
1. [Assign the Copilot for Sales licenses to your sales users](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide&preserve-view=true).

## Frequently asked questions

### What happens if I add the step-up license after I already assigned the Microsoft 365 Copilot licenses that I bought?

If there aren't enough unassigned Microsoft 365 Copilot licenses in your tenant, the step-up license continues to use a Microsoft 365 Copilot license but converts it to a Copilot for Sales license. The result is a reduction in the number of standalone Microsoft 365 Copilot licenses, which are replaced with Copilot for Sales licenses.

### What should I do if the system indicates that the Microsoft 365 Copilot license is allocated more than the available licenses?

To fix this issue, the admin must remove the Microsoft 365 Copilot licenses from a sales user and assign a Copilot for Sales license to that user. For information about how to assign or unassign licenses, go to [Assign or unassign licenses for users in the Microsoft 365 admin center](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide&preserve-view=true).
