---
title: Extend Microsoft Copilot for Sales with partner applications (preview)
description: Extend Copilot for Sales to integrate with partner applications to provide contextual insights and recommendations in Teams and Outlook.
ms.date: 12/11/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
---

# Extend Microsoft Copilot for Sales with partner applications (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

Copilot for Sales boosts seller productivity by providing contextual insights and recommendations in the context of the seller's daily workflow in Microsoft Teams and Outlook. Copilot for Sales can be connected to Dynamics 365 and Salesforce out of the box.

However, sales is more than just CRM. Sellers use a variety of applications to get their job done. Copilot for Sales can be extended to integrate with partner applications to provide contextual insights and recommendations.

If you are a partner application developer, you can integrate your application with Copilot for Sales to provide contextual insights and recommendations in the context of the seller's daily workflow in Microsoft Teams and Outlook.

To extend Copilot for Sales:

1. Decide which of the following capabilities you want to extend:
    - Latest activities in opportunity summary
    - Records from non-CRM applications related to a CRM record
    
    > [!NOTE]
    > If you want to extend any capability other than the ones listed above, contact us using [this link](https://aka.ms/SalesCopilotPartnerSignUp).

2. Implement the APIs to extend the capabilities you chose in step 1.
    1. Latest activities in opportunity summary - [GetRelatedActivities](api-get-related-activities.md)
    1. Records from non-CRM applications related to CRM records - [GetRelatedRecords](api-get-related-records.md)

3. Add the above APIs to an existing or a new [Power Apps copilot enabled connector](https://go.microsoft.com/fwlink/?linkid=2251841) and get your connector certified.


## Show latest activities from your application in opportunity summary

Copilot for Sales displays [opportunity summary](view-opportunity-summary.md) when a seller reads an email or prepares for a meeting with customer. You can extend this capability to show latest activities from your application in opportunity summary by implementing the `GetRelatedActivities` API and surfacing it in a Power Apps connector.

The following image shows an example of how the [output of the GetRelatedActivities API](api-get-related-activities.md#example) is mapped to the opportunity summary.

:::image type="content" source="media/extend-oppty-summ.png" alt-text="Screenshot showing anatomy of latest activities from a partner application.":::

|Annotation|Description|
|----------|-----------|
|1|Section showing latest activities from partner application in opportunity summary. The section title is the name of the Power Apps connector.|
|2|Activity descriptions from API response.|
|3|Citation number to see details about the activity.|
|4|Citation card showing details about the activity.|
|5|Icon and title of the activity. The icon is retrieved from the Power Apps connector metadata. The title text is the title of the activity.|
|6|Additional properties of the activity from API response.|
|7|Name of the partner application. The name displayed is the name of the Power Apps connector.|
|8|Link to view activity details in the partner application. It is based on the URL of the activity in API response.|


## Show records from your application related to CRM records

Copilot for Sales displays [related records](view-record-details.md) when a seller reads an email or prepares for a meeting with customer. You can extend this capability to show records from your application related to CRM records in Copilot for Sales by implementing the `GetRelatedRecords` API and surfacing it in a Power Apps connector.

> [!NOTE]
> Currently, related records from partner applications are shown only for opportunities and accounts.

The following image shows an example of how the [output of the GetRelatedRecords API](api-get-related-records.md#example) is mapped to the related records.

:::image type="content" source="media/extend-record-details.png" alt-text="Screenshot showing anatomy of related records from a partner application.":::

|Annotation|Description|
|----------|-----------|
|1|Card showing related records from partner application.|
|2|Icon and title of the card. The icon is retrieved from the Power Apps connector metadata. The card title is the name of the Power Apps connector.|
|3|Related record titles from API response. Two additional properties from API response are rendered as key fields of each related record.|
|4|More actions icon to either copy a link to the record or view record details in the partner application. The link is based on the URL of the related record in API response.|
|5|Additional properties of the related record from API response.|

### See also

[Get activities and records from partner applications](api-ref-partner-apps.md)