---
title: Enrich opportunity insights with data from your application (preview)
description: Enhance sales information with the Sales app in Outlook. Extend its capabilities by using data from your own application.
ms.date: 11/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Enrich opportunity insights with data from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

While sellers read and compose emails in Outlook, they can use the Sales app to view opportunity insights to get more information about the opportunity related to the email.

You can extend the opportunity insights capability that the Sales app provides with insights from your own application.

## API description

You must add the following API description to the action. In this way, the Sales app can identify the correct API that must be invoked to enrich the capability.

*This action gets additional sales insights that will be shown in C4S key sales info card in outlook sidecar. The action enhances the existing skills of copilot for sales.*

## API operation

This API uses Operation Type: GET

## Input parameters

The Sales app is designed to provide the following input parameters to your APIs.

| Name | Data type/format | Required | Details | Description to add in the action |
|------|------------------|----------|---------|----------------------------------|
| recordType | String | Yes | The record type in customer relationship management (CRM). The record can specify the account, opportunity, lead, or contact that is related to the email. | This input identifies the record type in CRM for which key sales info is requested. |
| recordId | String | Yes | The record ID in CRM. | This input provides the unique identifier of the CRM record for which key sales info is requested. |
| crmType | String | No | The type of CRM system. The valid values are *Salesforce* and *Dynamics 365*. | This input indicates the type of CRM in which the CRM record exists, for which key sales info is requested. |
| crmOrgUrl | String | No | The CRM organization URL. | This input indicates the URL of the CRM environment in which the CRM record exists, for which key sales info is requested. |
| top | Integer | No | The number of insights to fetch. | This input indicates the number of sales highlights to fetch. |
| skip | Integer | No | The number of insights to skip. | This input indicates the number of items to skip when fetching sales highlights. |

## Output parameters

The Sales app expects to receive a list of insights (objects) from your APIs, and it expects each insight to have specific parameters. To ensure that the Sales app can correctly parse the output, the response structure must adhere to the guidelines in the following table. 

| Parameter | Data type | Required | Details |
|---------|----|--------|-----------|
| value | Array | Yes | A list of insights (objects) that are defined as described in the [Schema for insights](#schema-for-insights) section. |
| hasMoreResults | Boolean | No | A value that indicates whether more results are available. |

### Schema for insights

| Name | Data type/format | Required | Details | Description to add in the action |
|------|------------------|----------|---------|----------------------------------|
| title | String | Yes | The title of the sales insight citation card. It should include only the partner's name and can have up to 20 characters. | This output indicates the title of citation card for the insight. |
| description | String | Yes | The description of the sales insight. It's shown as a bullet point in the **Key sales info** pane and can have up to 130 characters. Here is an example: *Validation: Next steps: Align with timeline and success criteria*. | This output indicates the text of the insight to be included in key sales info. |
| url | String | No | A valid URL to open the insight in the partner application. | This output indicates the URL to learn more about the insight. |
| dateTime | DateTime | No | The date and time of the activity in UTC format. If the activity has both a start time and an end time, the application must determine which time to show. The format follows the OpenAPI specification. Here is an example: *2017-07-21T17:32:28Z*. | This output indicates the time associated with the insight. |
| additionalProperties | An object that has **Property Name** and **Property Value** values of the *String* type | No | A set of name-value pairs that indicate additional properties of the related insight that the action returns. This information is shown in a pop-up card when users select insights in the **Key sales info** pane. | This output indicates additional properties as name-value pairs of each related insight returned by the action. |

### Example

```json
{
    "value": [
        {
            "title": "Contract signed",
            "description": "Kenny Smith sent Renewal Contract on 04/23/2023 related to 50 Cafe A-100 Automatic",
            "dateTime": "2023-09-07T03:42:35.4662309Z",
            "url": https://contosohub.com,
            "additionalProperties": {
                "Contract name": "Renewal contract for Fourth Coffee",
                "Signed by": "Alberto Burgos, Tony Benis",
                "Signed": "9/7/23",
                 "Related Opportunity": "50 CafeA-100 Automatic"
            }
        }
    ],
    "hasMoreResults": false
}
```

The example in the following image shows how the output of the API is mapped to the opportunity insights.

:::image type="content" source="media/extend-oppty-insights.png" alt-text="Screenshot showing insights from partner apps in opportunity insights.":::

Legend:

1. Card that shows data from your partner application. 
1. Section that shows insights from the partner application. The section title is derived from the name of the Microsoft Power Platform connector. 
1. Descriptions of the insight from the API response.
1. Citation numbers that can be selected to view details about the insight.
1. Citation card that shows details about the insight.
1. Icon and title of the insight. The icon is retrieved from the Microsoft Power Platform connector metadata. The title is the title of the insight from the API response.
1. Additional properties of the insight from the API response.
1. Name of the partner application. The name that is shown is the name of the Microsoft Power Platform connector.
1. Link that can be selected to view insight details in the partner application. It's based on the URL of the insight in the API response.

### Related information

[View opportunity insights in the Sales app](key-sales-info.md)<br>
[Enrich email summaries with insights from your application](extend-email-summary.md)<br>
[Enrich email drafts with file links from your application](extend-email-draft.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Sales in Microsoft 365 Copilot with partner applications](extend-sales-app.md)<br>
[Build extensions for Sales in Microsoft 365 Copilot](build-apis.md)
