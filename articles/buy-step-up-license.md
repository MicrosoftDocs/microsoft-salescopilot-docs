---
title: Buy step-up license for Copilot for Sales
description: Learn how to assign Microsoft Copilot for Sales step-up licenses and upgrade from the Copilot for Microsoft 365 license.
ms.date: 05/17/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/17/2024
---

# Buy step-up license for Copilot for Sales

This article guides you through the process of assigning Microsoft Copilot for Sales step-up licenses to your existing Copilot for Microsoft 365 licenses so that you get sales-related insights.

The Copilot for Sales step-up license enables you to upgrade from the Copilot for Microsoft 365 license to the Copilot for Sales license that offers sales related insights and capabilities.

The step-up license is a fractional license, and not a standalone license, hence it requires a Copilot for Microsoft 365 license when added into the tenant.

> [!IMPORTANT]
> A step-up license automatically upgrades the prerequisite license to the full license. This means that the Copilot for Sales step-up license automatically upgrades the Copilot for Microsoft 365 license to a Copilot for Sales license, thereby reducing the number of available Copilot for Microsoft 365 licenses in the tenant.

## Prerequisites

Before you add Copilot for Sales step-up licenses to your tenant, ensure that you have the required number of Copilot for Microsoft 365 licenses by following these steps:

1. Open the [Microsoft 365 admin center](https://admin.microsoft.com/).
1. In the left navigation pane, select **Billing** > **Your products**.
1. Verify whether you have sufficient Copilot for Microsoft 365 licenses available for the users who need access to Copilot for Sales.

> [!NOTE]
> - There must be enough Copilot for Microsoft 365 licenses available in the tenant to allow the conversion to Copilot for Sales licenses.
> - The Copilot for Microsoft 365 licenses should not be assigned to any users.
> - The available and unaasigned Copilot for Microsoft 365 licenses should be the ones you want to upgrade to Copilot for Sales licenses, and thus adequate to assign to youy dedicated sales users.
> - The available and unaasigned Copilot for Microsoft 365 licenses should have the same or later expiry date as the Copilot for Sales step-up licenses.

If you don't meet these prerequisites and don't have enough Copilot for Microsoft 365 licenses available, you must purchase the full [Copilot for Sales licenses](buy-license.md).

> [!IMPORTANT]
> - If you've already assigned Copilot for Microsoft 365 licenses to users within your tenant and there aren't enough available and unassigned licenses for the step-up license, the process will continue by removing the standalone allocation to complete the upgrade to a full Copilot for Sales license. This action will reduce the number of available standalone Copilot for Microsoft 365 licenses, potentially causing a discrepancy between available licenses and those assigned. In such a case, you'll receive a message indicating over-allocation.
> - No Copilot for Sales license is assigned to a user without intervention from the admin team. An alert message will indicate that you have more licenses assigned to users than are available for standalone Copilot for Microsoft 365. The license count for Copilot for Sales should increase. If this situation arises and you wish to reassign these licenses, please refer to the [Frequently asked questions](#frequently-asked-questions) section.

## Add Copilot for Sales step-up licenses

1. Open the [Microsoft 365 admin center](https://admin.microsoft.com/).
2. Add the Copilot for Sales step-up licenses to your tenant.
3. [Assign the Copilot for Sales licenses to your sales users](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide&preserve-view=true).

## Frequently asked questions

### What happens if I've already assigned my purchased Copilot for Microsoft 365 licenses and then I add the step-up license?

If there aren't enough unassigned Copilot for Microsoft 365 licenses in your tenant, the step-up license will continue to use a Copilot for Microsoft 365 license, converting it into Copilot for Sales license. This will result in a reduction of Copilot for Microsoft 365 (standalone) licenses, which will be replaced with Copilot for Sales licenses.

### What should I do if the system indicates that more users are accessing Copilot for Microsoft 365 than there are available licenses in the tenant?

To rectify this, the admin must remove the Copilot for Microsoft 365 licenses from a sales user and instead assign them a Copilot for Sales license. For information on how to assign or unassign licenses, see [Assign or unassign licenses for users in the Microsoft 365 admin center](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide&preserve-view=true).
