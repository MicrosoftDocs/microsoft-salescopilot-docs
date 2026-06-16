---
title: Feature matrix for Sales agent in Outlook
description: Learn which Sales agent capabilities are available in New Outlook, Outlook on the web, and Classic Outlook for each license type.
ms.date: 06/16/2026
ms.topic: overview
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Feature matrix for Sales agent in Outlook

Sales agent capabilities vary by Outlook client and license. Use this matrix to see where each feature appears and which settings change what users see.

> [!NOTE]
> The [email insights](access-settings.md#email-insights-preview) and [meeting insights](access-settings.md#meeting-insights) settings control whether **Opportunity insights** and **Customer communication** cards appear. If you're using Salesforce as your CRM, also [turn on the server-to-server connection](connect-agent-datasource.md#set-up-server-to-server-connection-to-salesforce).

## How to read the matrix

- If both email insights and meeting insights are disabled, the **Key Sales info** card appears in New Outlook and Outlook on the web.
- If either setting is enabled, the **Opportunity insights** and **Customer communication** cards replace **Key Sales info** when the email or meeting is linked to an opportunity.
- In Classic Outlook, the **Key email info** card remains available, and the opportunity-related cards follow the same settings-based behavior.

> [!NOTE]
> The **Opportunity insights** and **Customer communication** cards appear only when an email or a meeting is connected to an opportunity.

## New Outlook and Outlook on the web

| Feature | Access to Dynamics 365 Sales | Access to Microsoft 365 Copilot (with Salesforce or Dynamics 365) |
|---|---|---|
| [Key email info](view-save-email-summary-crm.md) card | Available in the **Sales** pane. | Not available in the **Sales** pane. |
| Draft an email | Available in the **Sales** pane. | Available on canvas. |
| Email summary | Available in the **Key email info** card in the **Sales** pane. | Available on canvas (same location as the **Summary by Copilot** section). |
| [Opportunity insights](view-opportunity-insights.md) and [Customer communication](view-customer-communication.md) cards | Available in the **Sales** pane when email insights or meeting insights are turned on; hidden otherwise. | Available in the **Sales** pane when email insights or meeting insights are turned on; otherwise, the **Key Sales info** card is shown. |


## Classic Outlook

| Feature | Access to Dynamics 365 Sales | Access to Microsoft 365 Copilot (with Salesforce or Dynamics 365) |
|---|---|---|
| [Key email info](view-save-email-summary-crm.md) card | Available in the **Sales** pane. | Available in the **Sales** pane. |
| Draft an email | Available in the **Sales** pane. | Available in the **Sales** pane. |
| [Opportunity insights](view-opportunity-insights.md) and [Customer communication](view-customer-communication.md) cards | Available in the **Sales** pane when email insights or meeting insights are turned on; hidden otherwise. | Available in the **Sales** pane when email insights or meeting insights are turned on; hidden otherwise. |
