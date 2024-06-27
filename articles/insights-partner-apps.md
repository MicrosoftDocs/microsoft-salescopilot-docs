---
title: View insights from partner applications (preview)
description: View insights from partner applications within Copilot for Sales.
ms.date: 05/20/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:03/13/2024
---

# View insights from partner applications (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

You can view records that are related to CRM records and activities that are related to CRM opportunities from partner applications within Copilot for Sales. To view related records and latest activities from partner applications, you must:

1. Get the feature enabled, as it is not enabled by default.
1. Create a connection using Power Platform connectors.
1. View related records from partner applications.
1. View latest activities from partner applications.

## Get the feature enabled

This feature is not enabled by default. To enable this feature, ask your administrator to [sign up for the preview feature](https://aka.ms/CopilotForSalesExtensibilityPreview). The Microsoft team will get in touch to validate the request and enable the feature for your organization.

## Create a connection

After the feature is enabled, you see an action card in the Copilot for Sales pane in Outlook to create a connection with the partner application. For example, in the following image, the action card to sign in to the connector for the partner application **DocuSign** is displayed. Select **Sign in** to connect to the partner application. 

:::image type="content" source="media/action-card-connector.svg" alt-text="Screenshot showing action card to sign in to connector.":::

In the pop-up message in Outlook, select **Create** to create a connector for the partner application. 

:::image type="content" source="media/create-connector.svg" alt-text="Screenshot showing pop-up to create a connector.":::

> [!NOTE]
> - All Power Platform connectors are not certified to work with Copilot for Sales. Copilot for Sales displays activities from partner applications that have implemented specific APIs and made them available through their Power Platform connectors.
> - If you are a partner application maker and would like to integrate with Copilot for Sales, see Extend Copilot for Sales. Currently, DocuSign can be integrated with Copilot for Sales. 

## View related records

Related records from partner applications are displayed in a new card under record details. For example, in the following image, the contract documents related to a CRM opportunity are displayed from the partner application **DocuSign**.

:::image type="content" source="media/record-details-partner-apps.png" alt-text="Sceenshot showing related records from DocuSign":::

> [!NOTE]
> Currently, related records from partner applications are shown only for opportunities and accounts.

All the information about related records comes from the partner applications. Copilot for Sales renders the related record information retrieved from the partner application through the Power Platform connector. Copilot for Sales does not edit or filter the information.

You can perform the following actions on the related records:
- To see record details, select the record. 
- To copy link to a record or open it in the partner application, hover over the record, select **More actions** (**…**), and then select **Copy link** or **Open in (partner app)** respectively.

## View latest activities

Latest activities from partner applications are displayed under the **Latest activities from (partner app)** section. For example, in the following image, the activities from the partner application **DocuSign** are displayed in the opportunity summary.

:::image type="content" source="media/latest-activities-partner-app.png" alt-text="Sceenshot showing latest activities from DocuSign.":::

All the information about activities comes from the partner applications. Copilot for Sales renders the activity information retrieved from the partner application through the Power Platform connector. Copilot for Sales does not edit or filter the information.

Activities are displayed with citation numbers. Select the citation number to drill down and see detailed information. To view more details in the partner application, select :::image type="icon" source="media/open-record.png" border="false"::: at the bottom-right of the card. 