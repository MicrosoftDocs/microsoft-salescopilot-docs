---
title: Extend Microsoft Sales Copilot with partner applications (preview)
description: Extend Sales Copilot to integrate with partner applications to provide contextual insights and recommendations in Teams and Outlook.
ms.date: 11/13/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
---

# Extend Microsoft Sales Copilot with partner applications (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

Sales Copilot boosts seller productivity by providing contextual insights and recommendations in the context of the seller's daily workflow in Microsoft Teams and Outlook. Sales Copilot can be connected to Dynamics 365 and Salesforce out of the box.

However, sales is more than just CRM. Sellers use a variety of applications to get their job done. Sales Copilot can be extended to integrate with partner applications to provide contextual insights and recommendations.

If you are a partner application developer, you can integrate your application with Sales Copilot to provide contextual insights and recommendations in the context of the seller's daily workflow in Microsoft Teams and Outlook.

To extend Sales Copilot:

1. Decide which of the following capabilities you want to extend:
    - Latest activities in opportunity summary
    - Records from non-CRM applications related to a CRM record
    
    > [!NOTE]
    > If you want to extend any capability other than the ones listed above, contact us using [this link](https://aka.ms/SalesCopilotPartnerSignUp).

2. Implement the APIs to extend the capabilities you chose in step 1.
    1. Latest activities in opportunity summary - [GetRelatedActivities](api-get-related-activities.md)
    1. Records from non-CRM applications related to CRM records - [GetRelatedRecords](api-get-related-records.md)

3. Create or add above APIs to a [Power Apps connector](/connectors/connectors) and [get your connector certified](/connectors/custom-connectors/submit-certification).

4. [Register your connector as a plug-in](/power-apps/developer/data-platform/register-plug-in).


## Show latest activities from your application in opportunity summary

Sales Copilot displays [opportunity summary](view-opportunity-summary.md) when a seller reads an email or prepares for a meeting with customer. You can extend this capability to show latest activities from your application in opportunity summary by implementing the `GetRelatedActivities` API and surfacing it in a Power Apps connector.

The following image shows an example of how the output of the `GetRelatedActivities` API is mapped to the opportunity summary.

`image`

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

Sales Copilot displays [related records](view-record-details.md) when a seller reads an email or prepares for a meeting with customer. You can extend this capability to show records from your application related to CRM records in Sales Copilot by implementing the `GetRelatedRecords` API and surfacing it in a Power Apps connector.

The following image shows an example of how the output of the `GetRelatedRecords` API is mapped to the related records.

`image`

|Annotation|Description|
|----------|-----------|
|1|Card showing related records from partner application.|
|2|Icon and title of the card. The icon is retrieved from the Power Apps connector metadata. The card title is the name of the Power Apps connector.|
|3|Related record titles from API response. Two additional properties from API response are rendered as key fields of each related record.|
|4|Link to view related record details in the partner application. It is based on the URL of the related record in API response.|
|5|Additional properties of the related record from API response.|

### See also

[Get activities and records from partner applications](api-ref-partner-apps.md)