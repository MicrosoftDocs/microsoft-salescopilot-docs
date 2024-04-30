---
title: Extend Microsoft Copilot for Sales with partner applications (preview)
description: Extend Copilot for Sales to integrate with partner applications to provide contextual insights and recommendations in Teams and Outlook.
ms.date: 05/15/2024
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

Microsoft Copilot for Sales is an AI assistant designed for sales teams to maximize productivity and close more deals, bringing sales insights and next-generation AI into the tools you use daily like Microsoft Outlook, Microsoft Teams, and other Microsoft 365 apps.

Copilot for Sales connects to CRMs such as Salesforce Sales Cloud and Microsoft Dynamics 365 Sales out-of-box. However, sales is more than CRM. Sales teams often use specialized applications for account planning, prospecting, revenue intelligence, quoting, eSignature, and more. Customers and makers of sales applications can now bring data and insights from any of their applications into the copilot experience. 

If you are a partner application developer, you can integrate your application with Copilot for Sales to provide contextual insights and recommendations in the context of the seller's daily workflow in Microsoft Teams and Outlook.

This article provides guidance on how to extend Copilot for Sales with your application APIs. It provides the following information:
- Capabilities you can extend in Copilot for Sales.
- Input and output parameters for the APIs you need to build.
- Specific descriptions searched by Copilot for Sales within your plugin to determine the intended API for a particular capability. It also guides you on how to manage the input and output for these APIs. 

## How does extensibility work in Copilot for Sales?

Copilot for Sales in Microsoft 365 is composed of multiple individual capabilitys that are made available contextually to users. Each of these features is backed by a skill service owned by Copilot for Sales. When an end user interacts with a capability, the skill service for the capability generates the insights to deliver as part of that capability. Out-of-the-box, the skill service uses data in Graph and CRMs to get insights. With extensibility, the skill service will call into your application APIs made available in your copilot plugin in real-time to get additional insights to enrich the capability. When the skill service calls into your application APIs, it will pass all available context that your application APIs accept; and expects to get back insights in a format that aligns with how the insights are presented to users of the copilot in the capability.

`image`

To ensure that everything works properly, Copilot for Sales needs to:
- Identify which of your application APIs is relevant for getting insights to enrich a specific copilot capability.
- Pass the required contextual information to your application API.
- Identify the right parts of your application APIs to render in the capability.


You, as a plugin maker, must build:
1. The APIs that match the expectations of the copilot features you are trying to extend. The API used to extend a capability in Copilot for Sales must accept the required inputs from the app and return the required outputs expected by the app.
1. A power platform connector with the APIs and oAuth authentication.
1. A copilot plugin that adds the copilot provided descriptions to the connector.

    Copilot doesn't require adherence to a specific API specification. The naming of the API or its input/output parameters and structure are not constraints for Copilot. Your responsibility is to ensure that your APIs can handle the inputs supplied by Copilot and return the expected outputs. Additionally, you must provide appropriate descriptions to enable Copilot to correctly match them during runtime.

For instance, suppose you wish to enhance the [Key sales info](key-sales-info.md) capability in Copilot for Sales. To do this, you'll need to create an API that, at the very least, accepts a CRM record reference (passed as 'recordType' and 'recordId') as input and provides the insight title, description, and date as output. This API should be added to a new or existing Power Platform connector that utilizes OAuth for authentication. Furthermore, the APIs in the connector should be supplemented with descriptions as required by Copilot for Sales.

## Copilot capabilities that can be extended

Extensibility enables you to enhance existing capabilities or add new capabilities in Copilot for Sales. You can bring data and insights from your application into the copilot experience. The following capabilities can be extended:
- [Email summary](email-summary-premium.md)
- [Key sales information](key-sales-info.md)
- [Opportunity summary](view-opportunity-summary.md)
- [Record details](view-record-details.md)

Additionally, you can introduce new Q&A capabilities to the chat features in Copilot for Sales. However, it's important to note that you cannot add new capabilities to the non-chat features in Copilot for Sales.

## Extend Copilot for Sales

1. [Decide which of the capabilities you want to extend](#copilot-capabilities-that-can-be-extended).
    
    > [!NOTE]
    > If you want to extend any capability other than the ones listed [here](#copilot-capabilities-that-can-be-extended), contact us using [this link](https://aka.ms/SalesCopilotPartnerSignUp).

2. Implement the APIs to extend the capabilities you chose in step 1.
    1. Latest activities in opportunity summary - [GetRelatedActivities](api-get-related-activities.md)
    1. Records from non-CRM applications related to CRM records - [GetRelatedRecords](api-get-related-records.md)

3. Add the above APIs to an existing or a new [Power Platform copilot enabled connector](https://go.microsoft.com/fwlink/?linkid=2251841) and get your connector certified.

-------------------------------------------------------------------------------------
## Show latest activities from your application in opportunity summary

Copilot for Sales displays [opportunity summary](view-opportunity-summary.md) when a seller reads an email or prepares for a meeting with customer. You can extend this capability to show latest activities from your application in opportunity summary by implementing the `GetRelatedActivities` API and surfacing it in a Power Platform connector.

The following image shows an example of how the [output of the GetRelatedActivities API](api-get-related-activities.md#example) is mapped to the opportunity summary.

:::image type="content" source="media/extend-oppty-summ.png" alt-text="Screenshot showing anatomy of latest activities from a partner application.":::

|Annotation|Description|
|----------|-----------|
|1|Section showing latest activities from partner application in opportunity summary. The section title is the name of the Power Platform connector.|
|2|Activity descriptions from API response.|
|3|Citation number to see details about the activity.|
|4|Citation card showing details about the activity.|
|5|Icon and title of the activity. The icon is retrieved from the Power Platform connector metadata. The title text is the title of the activity.|
|6|Additional properties of the activity from API response.|
|7|Name of the partner application. The name displayed is the name of the Power Platform connector.|
|8|Link to view activity details in the partner application. It is based on the URL of the activity in API response.|


## Show records from your application related to CRM records

Copilot for Sales displays [related records](view-record-details.md) when a seller reads an email or prepares for a meeting with customer. You can extend this capability to show records from your application related to CRM records in Copilot for Sales by implementing the `GetRelatedRecords` API and surfacing it in a Power Platform connector.

> [!NOTE]
> Currently, related records from partner applications are shown only for opportunities and accounts.

The following image shows an example of how the [output of the GetRelatedRecords API](api-get-related-records.md#example) is mapped to the related records.

:::image type="content" source="media/extend-record-details.png" alt-text="Screenshot showing anatomy of related records from a partner application.":::

|Annotation|Description|
|----------|-----------|
|1|Card showing related records from partner application.|
|2|Icon and title of the card. The icon is retrieved from the Power Platform connector metadata. The card title is the name of the Power Platform connector.|
|3|Related record titles from API response. Two additional properties from API response are rendered as key fields of each related record.|
|4|More actions icon to either copy a link to the record or view record details in the partner application. The link is based on the URL of the related record in API response.|
|5|Additional properties of the related record from API response.|

### See also

[Get activities and records from partner applications](api-ref-partner-apps.md)