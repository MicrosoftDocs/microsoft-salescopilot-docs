---
title: Enrich CRM record summaries with insights from your application (preview)
description: Enhance CRM record summaries in Sales app by using AI and insights from your own application, improving customer understanding.
ms.date: 03/28/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Enrich CRM record summaries with insights from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

To better understand the context of a meeting that they are preparing for or an email that they are reading, sellers want relevant customer relationship management (CRM) information, such as customer queries, concerns, and notes. Sales app uses AI to generate a summary of each CRM record. This summary highlights crucial details, such as the sales stage, budget, and projected close date. You can extend the CRM record summary capability that Sales app provides with insights from your own application.

## API description

You must add the following API description to the action. In this way, Sales app can identify the correct API that must be invoked to enrich the capability.

*This action gets additional sales insights related to a CRM record that will be shown in the C4S record summary card. The action enhances the existing skills of copilot for sales.*

## API operation

This API uses Operation Type: GET

## Input parameters

Sales app is designed to provide the following input parameters to your APIs.

| Name | Data type/format | Required | Details | Description to add in the action |
|------|--------------------|----------|---------|-----------------------------------|
| recordType | String | Yes | The type of entity or object in CRM that related insights such as activities are requested for. The value includes the language-agnostic unique name of the entity or object type, not the display name that can be localized. Examples include *account* and *opportunity*. | This input indicates the entity or object type in CRM for which insights are requested. |
| recordId | String | Yes | The unique identifier of the CRM record. | This input indicates the unique identifier of the CRM record for which insights are requested. |
| startDateTime | String in 'date-time' format | No | The start date and time to look up insights. The format follows the OpenAPI specification. Here is an example: *2017-07-21T17:32:28Z*. | This input indicates the start date and time for insights requested. |
| endDateTime | String in 'date-time' format | No | The end date and time to look up insights. The format follows the OpenAPI specification. Here is an example: *2017-07-21T17:32:28Z*. | This input indicates the end date and time for insights requested. |
| top | Integer | No | The number of insights to fetch. | This input indicates the number of insights to fetch. |
| skip | Integer | No | The number of insights to skip. | This input indicates the number of insights to skip. |
| crmType | String | No | The valid values are *Dynamics 365* and *Salesforce*. | This input indicates the type of CRM in which the CRM record exists, for which insights are requested. |
| crmOrgUrl | String | No | The host name of the CRM organization, such as *contoso.crm.dynamics.com*. | This input indicates the URL of the CRM environment in which the CRM record exists, for which insights are requested. |

## Output parameters

Sales app expects to receive a list of insights (objects) from your APIs, and it expects each insight to have specific parameters. To ensure that Sales app can correctly parse the output, the response structure must adhere to the guidelines in the following table.

| Parameter | Data type | Required | Details |
|-----------|-----------|----------|---------|
| value | Array | Yes | A list of insights (objects) that are defined as described in the [Schema for insights](#schema-for-insights) section. |
| hasMoreResults | Boolean | No | A value that indicates whether more results are available. |

### Schema for insights

| Name | Data type/Format | Required | Details | Description to be added in action |
|------|------------------|----------|---------|-----------------------------------|
| title | String | Yes | The title of the insight on the citation card. It's the natural language title of the insight in the language that is specified through the `Accept-Language` request header. Here is an example: *Contract signed*. | This output indicates the title of the activity in the citation card. |
| description | String | Yes | The description of the insight. It's shown as bullet points in the record summary and is the natural language description of the insight in the language that is specified through the `Accept-Language` header. Here is an example: *Kenny, Logan, and two others signed the Contoso 2023 Renewal Contract on 9/7/2023*. | This output indicates the description of the insight. |
| dateTime | String in 'date-time' format | Yes | The date and time of the activity in UTC format. If the activity has both a start time and an end time, the application must determine which time to show. The format follows the OpenAPI specification. Here is an example: *2017-07-21T17:32:28Z*. | This output indicates the time associated with the insight. |
| url | String | No | A valid URL to open the activity in the partner application. | This output indicates the URL to open insight. |
| additionalProperties | An object that has **Property Name** and **Property Value** values of the *String* type | No | <p>Additional properties that are shown in the detailed view. Property names and values are in natural language in the language that is specified through the `Accept-Language` header. Here is an example.</p><pre>{<br> "Status reason": "Signed off",<br> "Owner": "Kenny Smith"<br>}</pre> | This output indicates additional properties displayed in the detailed view of the insight. |

> [!NOTE]
> Although the API requirements for extending email summary capabilities and record summary capabilities might look similar, they must be added as separate actions in the connector.

### Example

```json
{
    "value": [
        {
            "title": "Contract signed",
            "description": "You have 5 connections in Fourth Coffee Inc",
            "dateTime": "2024-05-07T03:28:38.0667701Z",
            "url": null,
            "additionalProperties": {
                "Contract name": "50 Cafe-A-100 Automatic Renewal Contract",
                "Signed by": "Alberto Burgos, Tony",
                "Signed": "9/7/23"
            }
        },
        {
            "title": "Contract signed",
            "description": "Multiple stakeholders from Fourth Coffee have visited the Contoso website four times in the last four months",
            "dateTime": "2024-05-07T03:28:38.0669445Z",
            "url": null,
            "additionalProperties": {
                "Contract name": "50 Cafe-A-100 Automatic Renewal Contract",
                "Signed by": "Alberto Burgos, Tony",
                "Signed": "9/7/23"
            }
        }
    ],
    "hasMoreResults": false
}
```

The example in the following image shows how the output of the API is mapped to the record summary.

:::image type="content" source="media/extend-oppty-summ.svg" alt-text="Screenshot showing the anatomy of the latest activities from a partner application.":::

Legend:

1. Section that shows insights from the partner application. The section title is derived from the name of the Microsoft Power Platform connector. 
1. Descriptions of the insight from the API response.
1. Citation numbers that can be selected to view details about the insight.
1. Citation card that shows details about the insight.
1. Icon and title of the insight. The icon is retrieved from the Microsoft Power Platform connector metadata. The title text is the title of the insight from the API response.
1. Additional properties of the insight from the API response.
1. Name of the partner application. The name that is shown is the name of the Microsoft Power Platform connector.
1. Link that can be selected to view insight details in the partner application. It's based on the URL of the insight in the API response.

### Related information

[View record summary](view-opportunity-summary.md) <br>
[Enrich email summaries with insights from your application](extend-email-summary.md)<br>
[Enrich email drafts with file links from your application](extend-email-draft.md)<br>
[Enrich opportunity insights with data from your application](extend-opportunity-insights.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Extend Sales app with partner applications](extend-sales-app.md)<br>
[Build Sales app extensions](build-apis.md)
