---
title: Enrich key sales info with insights from your application (preview)
description: Enhance sales information with Copilot for Sales in Outlook. Extend its capabilities using insights from your own application.
ms.date: 05/20/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Enrich key sales info with insights from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Sellers can use Copilot for Sales while reading and composing emails in Outlook to view key sales information about contacts, accounts, and opportunities that are related to the email. Key sales information is based on either the opportunity connected to the email or the most relevant opportunity based on the contacts and accounts in the email. You can extend the key sales information capability provided by Copilot for Sales with insights from your own application.

## API description

You need to add the API description to the action to enable Copilot for Sales to identify the correct API to invoke for enriching this capability. The description must be as follows:

`This action gets additional sales insights that will be shown in C4S key sales info card in outlook sidecar. The action enhances the existing skills of copilot for sales.`

## Input parameters

Copilot for Sales is designed to provide the following input parameters to your APIs.

| Name | Data type / Format | Required | Details | Description to be added in action |
|------|--------------------|----------|---------|----------------------------------|
| recordType | String | Yes | Record Type in CRM. The value can be account, opportunity, lead, or contact that is related to the email. | This input identifies the record type in CRM for which key sales info is requested. |
| recordId | String | Yes | Record ID in CRM. | This input provides the unique identifier of the CRM record for which key sales info is requested. |
| crmType | String | No | Type of CRM system. Valid values are Salesforce and Dynamics 365 | This input indicates the type of CRM in which the CRM record exists, for which key sales info is requested. |
| crmOrgUrl | String | No | CRM Organization URL. | This input indicates the URL of the CRM environment in which the CRM record exists, for which key sales info is requested. |
| top | Integer | No | Number of insights to fetch. | This input indicates the number of sales highlights to fetch. |
| skip | Integer | No | Number of insights to skip. | This input indicates the number of items to skip when fetching sales highlights. |

## Output parameters

Copilot for Sales anticipates receiving a list of insights (objects), each with specific parameters, from your APIs. To ensure the Copilot for Sales can parse the output correctly, it's crucial to follow the response structure as described in the following table. 

|Parameter|Data type|Required|Details|
|---------|----|--------|-----------|
|value|Array|Yes|List of insights (objects) defined as mentioned in [Schema for insight](#schema-for-insight)|
|hasMoreResults|Boolean|No|Indicates if there are more results available.|

### Schema for insight

| Name | Data type / Format | Required | Details | Description to be added in action |
|------|--------------------|----------|---------|----------------------------------|
| Title | String | Yes | Title of the sales insight citation card. Should include only the partner's name. Title can be up to 20 characters. | This output indicates the title of citation card for the insight. |
| description | String | Yes | Description of the sales insight displayed as a bullet point in the key sales info panel. For example: `Validation: Next steps: Align with timeline and success criteria`. Description can be up to 130 characters. | This output indicates the text of the insight to be included in key sales info. |
| url | String | No | A valid URL to open the insight in the partner application. | This output indicates the URL to learn more about the insight. |
| dateTime | DateTime | No | Date and time of the activity in UTC format. If there's a start and end time, application needs to decide which one to show. The format is as per OpenAPI specification, for example, 2017-07-21T17:32:28Z. | This output indicates the time associated with the insight. |
| additionalProperties | Object with Property Name and Property Value | No | This output indicates additional properties as name-value pairs of the related insight returned by the action. This is displayed in a pop-up card when clicking on the insights in the key-sales-info panel. | This output indicates additional properties as name-value pairs of each related insight returned by the action. |

### Example

```json
{
  "value": [
    {
      "title": "Next best action from Contoso Hub",
      "description": "Validation next step: Align on timeline and success criteria",
      "dateTime": "2024-05-07T03:42:35.4662309Z",
      "url": null,
      "additionalProperties": {
        "Current step": "Step name",
        "Next step": "Step name",
        "Due date": "Date"
      }
    },
    {
      "title": "Next best action from Contoso Hub",
      "description": "Nina and Daisy in your team are connected to Alberto and can help influence the deal",
      "dateTime": "2024-05-07T03:42:35.4663109Z",
      "url": null,
      "additionalProperties": {
        "Current step": "Step name",
        "Next step": "Step name",
        "Due date": "Date"
      }
    }
  ],
  "hasMoreResults": false
}
```

The following image shows an example of how the output of the API is mapped to the key sales info.

:::image type="content" source="media/extend-ksi.svg" alt-text="Screenshot showing insights from partner apps in key sales info.":::

Legend:
1. Section showing insights from partner application. The section title is derived from the name of the Power Platform connector. 
1. Descriptions (of insight) from API response.
1. Citation numbers to see details about the insight.
1. Citation card showing details about the insight.
1. Icon and title of the insight. The icon is retrieved from the Power Platform connector metadata. The title text is the title of the insight from API response.
1. Additional properties of the insight from API response.
1. Name of the partner application. The name displayed is the name of the Power Platform connector.
1. Link to view insight details in the partner application. It is based on the URL of the insight in API response.

### See also

[Add a new question and answer (Q&A) capability to the Sales chat](extend-m365-chat.md)<br>
[Enrich email summary with insights from your application](extend-email-summary.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summary with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)