---
title: 
description:
ms.date: 11/13/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Integrate Microsoft Sales Copilot with partner applications (preview)

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

2. Implment the APIs to extend the capabilities you chose in step 1.
    1. Latest activities in opportunity summary - GetRelatedActivities
    1. Records from non-CRM applications related to CRM records - GetRelatedRecords

3. Create or add above APIs to a [Power Apps connector](/connectors/connectors) and [get your connector certified](/connectors/custom-connectors/submit-certification).

4. [Register your connector as a plug-in](/power-apps/developer/data-platform/register-plug-in).


## Show latest activities from your application in opportunity summary

Sales Copilot displays opportunity summary when a seller reads an email or prepares for a meeting wih customer. You can extend this capability to show latest activities from your application in opportunity summary by implementing the `GetRelatedActivities` API and surfacing it in a Power Apps connector.

The following image shows an example of how the output of the `GetRelatedActivities` API is mapped to the opportunity summary.

`image`

|Annotation|Description|
|----------|-----------|


## Show records from your application related to CRM records