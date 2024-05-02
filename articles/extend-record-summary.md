---
title: Enrich CRM record summary with insights from your application API (preview)
description: 
ms.date: 02/02/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
  - ai-gen-title
---

# Enrich CRM record summary with insights from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

When preparing for a customer meeting or reading an email, sellers seek pertinent CRM information such as customer queries, concerns, and notes to gain a better understanding of the context prior to the meeting. Copilot for Sales uses AI to generate a summary of each CRM record, highlighting crucial details such as sales stage, budget, and projected close date. You can extend the CRM record summary capability provided by Copilot for Sales with insights from your own application.

## API description

You need to add the API description to the plugin action to enable Copilot for Sales to identify the correct API to invoke for enriching this capability. The description must be as follows:

`This action gets additional sales insights related to a CRM record that will be shown in the C4S record summary card. The action enhances the existing skills of copilot for sales.`

## Input parameters

Copilot for Sales is designed to provide the following input parameters to your plugin APIs.

| Name | Data type / Format | Required | Details | Description to be added in plugin |
|------|--------------------|----------|---------|-----------------------------------|
| recordType | String | Yes | Entity or Object type in CRM for which related insights such as activities are requested. It includes language agnostic unique name of the entity or object type, and not the display name that can be localized. For example, account, opportunity, and so on. | This input indicates the entity or object type in CRM for which insights are requested. |
| recordId | String | Yes | Unique identifier of the CRM record. | This input indicates the unique identifier of the CRM record for which insights are requested. |
| startDateTime | String with format 'date-time' | No | Start date and time to look up insights. The format is as per OpenAPI specification, for example, 2017-07-21T17:32:28Z. | This input indicates the start date and time for insights requested. |
| endDateTime | String with format 'date-time' | No | End date and time to look up insights. The format is as per OpenAPI specification, for example, 2017-07-21T17:32:28Z. | This input indicates the end date and time for insights requested. |
| top | Integer | No | Number of insights to fetch. | This input indicates the number of insights to fetch. |
| skip | Integer | No | Number of insights to skip. | This input indicates the number of insights to skip. |
| crmType | String | No | Valid values are Dynamics 365 and Salesforce. | This input indicates the type of CRM in which the CRM record exists, for which insights are requested. |
| crmOrgUrl | String | No | Host name of the CRM organization. For example, contoso.crm.dynamics.com. | This input indicates the URL of the CRM environment in which the CRM record exists, for which insights are requested. |

> [!NOTE]
> - Authentication is expected to be handled by the constructs in the Power Platform connector and is outside the scope of this API.
> - Current user's language is passed in the request header as `Accept-Language`. Use this for any language specific operations.
> - Read the following headers from the request to your connector and send them to your backend for a better diagnostics:
>   - `x-ms-client-request-id`: A unique identifier for the incoming request. 
>   - `x-ms-user-agent`: Value used as "sales-copilot".

## Output parameters

Copilot for Sales anticipates receiving a list of insights (objects), each with specific parameters, from your plugin APIs. To ensure that Copilot for Sales can parse the output correctly, it's crucial to follow the response structure outlined below.

|Parameter|Data type|Required|Details|
|---------|----|--------|-----------|
|value|Array|Yes|List of insights (objects) defined as mentioned in [Schema for insight](#schema-for-insight)|
|hasMoreResults|Boolean|No|Indicates if there are more results available.|

### Schema for insight

| Name | Data type / Format | Required | Details | Description to be added in plugin |
|------|--------------------|----------|---------|-----------------------------------|
| Title | String | Yes | Title of the insight in the citation card. It is the natural language title of the insight in the language specified in the `Accept-Language` request header. For example, Contract signed. | This output indicates the title of the activity in the citation card. |
| Description | String | Yes | Description of the insight displayed as bullet points in the record summary. It is the natural language description of the insight in the language specified with the `Accept-Language` header. For example, Kenny, Logan, and two others signed the Contoso 2023 Renewal Contract on 9/7/2023. | This output indicates the description of the insight. |
| dateTime | String with format 'date-time' | Yes | Date and time of the activity in UTC format. If there is a start and end time, application needs to decide which one to show. The format is as per OpenAPI specification, for example, 2017-07-21T17:32:28Z. | This output indicates the time associated with the insight. |
| url | String | No | A valid URL to open activity in the partner application. | This output indicates the URL to open insight. |
| additionalProperties | Object with Property Name and Property Value | No | Additional properties displayed in the detailed view. Property names and values are in natural language in the language specified with the `Accept-Language` header. For example, <br>{<br> "Status reason": "Signed off",<br> "Owner": "Kenny Smith" <br>} | This output indicates additional properties displayed in the detailed view of the insight. |

### Example

```json
{
        "value": [
             {
                "title": "Auto Renewal Contract",
                "description": "Kenny Smith sent AutomaticRenewalcontract.docx on 11/11/2023 12:50:53 PM",
                "dateTime": "12:50 PM, 11/11/23",
                "url": https://app.docusign.com/documents/details/000baf00-2342-42ab-8eff-00000000000,
                "additionalProperties": {
                    "Recipients": "Logan Edwards",
                    "Sender Name": "Kenny Smith",
                    "Status": "Sent",
                    "Date": "12:50 PM, 11/11/23"
                }
            },
            {
                "title": "Purchase Contract",
                "description": "Logan Edwards completed PurchaseContract.docx on 11/11/2023 12:56:14 PM",
                "dateTime": "12:56 PM, 11/11/23",
                "url": https://app.docusign.com/documents/details/000baf11-2342-42ab-8eff-00000000000,
                "additionalProperties": {
                    "Recipients": "Logan Edwards",
                    "Sender Name": "Kenny Smith",
                    "Status": "Completed",
                    "Date": "12:56 PM, 11/11/23"
                }
            }
        ],
        "hasMoreResults": false
    }

```

The following image shows an example of how the output of the API is mapped to the record summary.

:::image type="content" source="media/extend-oppty-summ.png" alt-text="Screenshot showing anatomy of latest activities from a partner application.":::

|Annotation|Output parameter|
|----------|-----------|
|1|Section showing insights from partner application in record summary. The section title is derived from the name of the Power Platform connector.|
|2|Descriptions of the insight, obtained from the API response.|
|3|Citation number to see details about the insight.|
|4|Citation card showing details about the insight.|
|5|Icon and title of the insight. The icon is retrieved from the Power Platform connector metadata. The title text is the title of the insight from API response.|
|6|Additional properties of the insight from API response.|
|7|Name of the partner application. The name displayed is the name of the Power Platform connector.|
|8|Link to view insight details in the partner application. It is based on the URL of the insight in API response.|


### See also

[GetRelatedRecords](api-get-related-records.md)