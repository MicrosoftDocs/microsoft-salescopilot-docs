---
title: Power BI dashboard hierarchy settings for Salesforce organizations
description: Learn how to import your org chart to Dataverse and keep it synced with Copilot for Sales administrator settings in Power BI.
ms.date: 02/06/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:01/30/2024
---

# Power BI dashboard hierarchy settings for Salesforce organizations (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

You can use a template from Sales Copilot to create a dashboard in Microsoft Power BI. Sellers and managers can use this to get aggregated views over conversation made by themselves or their teams.

As a Salesforce system administrator, you can control the source of the hierarchy information that's used to show the right data to the right people.

To ensure managers and sellers have the right level of access to the dashboard, Sales Copilot uses organizational information saved in the [SystemUser table in Dataverse](/power-apps/developer/data-platform/reference/entities/systemuser). If your org chart isn't saved to Dataverse, you can import it.

> [!NOTE]
>
> - Hierarchy settings are available only for Salesforce customers and are displayed only if you are connected to a Salesforce environment.

## Import your org chart

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).

1. Under **Environment**, select **Reports**.

1. Under **Copilot for Sales dashboard**, select **Import your org chart to Dataverse and keep it synced**.

1. Select **Microsoft Entra ID** or **Salesforce**, and then select **Save**.

    :::image type="content" source="media/hierarchy-settings.png" alt-text="Screenshot showing hierarchy settings.":::

> [!NOTE]
> The organizational hierarchy is not copied at once, but it gets updated every time a user signs in to the **Copilot for Sales** pane in Outlook. If a user does not appear in the Power BI dashboard, ensure they are signed-in to Copilot for Sales, and then try again.
