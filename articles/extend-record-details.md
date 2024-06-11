---
title: Enrich CRM record details with insights from your application (preview)
description: Enhance your CRM record details with insights from your application using the Copilot for Sales extension capability.
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

# Enrich CRM record details with insights from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Sellers can view details about a saved contact, along with its associated records such as accounts and opportunities. You can extend the CRM record details capability provided by Copilot for Sales with insights from your own application.

## API description

You need to add the API description to the action to enable Copilot for Sales to identify the correct API to invoke for enriching this capability. The description must be as follows:

`This action gets records related to a CRM record. The action enhances the existing skills of Copilot for Sales.`

## Input parameters

Copilot for Sales is designed to provide the following input parameters to your APIs.

| Name | Data type / Format | Required | Details | Description to be added in action |
|------|--------------------|----------|---------|-----------------------------------|
| recordType | String | Yes | Entity or Object type in CRM for which related records are requested. It includes language agnostic unique name of the entity or object type, and not the display name that can be localized. For example, account, opportunity, and so on. | This input identifies the record type in CRM for which related records are requested. |
| recordId | String | Yes | Unique identifier of the CRM record. | This input provides the unique identifier of the CRM record for which related records are requested. |
| top | Integer | No | Number of activities to fetch. | This input indicates the number of related records to fetch. |
| skip | Integer | No | Number of activities to skip. | This input indicates the number of records to skip when fetching related records. |
| crmType | String | No | Valid values are Dynamics 365 and Salesforce. | This input indicates the type of CRM the related records are fetched from. |
| crmOrgUrl | String | No | Host name of the CRM organization. For example, `contoso.crm.dynamics.com`. | This input indicates the URL of the CRM environment the related records are fetched from. |

> [!NOTE]
> - Authentication is expected to be handled by the constructs in the Power Platform connector and is outside the scope of this API.
> - Current user's language is passed in the request header as `Accept-Language`. Use this for any language specific operations.
> - Read the following headers from the request to your connector and send them to your backend for a better diagnostics:
>   - `x-ms-client-request-id`: A unique identifier for the incoming request. 
>   - `x-ms-user-agent`: Value used as "sales-copilot".

## Output parameters

Copilot for Sales anticipates receiving a list of insights (objects), each with specific parameters, from your APIs. To ensure the Copilot for Sales can parse the output correctly, it's crucial to follow the response structure outlined below.

|Parameter|Data type|Required|Details|
|---------|----|--------|-----------|
|value|Array|Yes|List of insights (objects) defined as mentioned in [Schema for insight](#schema-for-insight)|
|hasMoreResults|Boolean|No|Indicates if there are more results available.|

### Schema for insight

| Name | Data type / Format | Required | Details | Description to be added in action |
|------|--------------------|----------|---------|-----------------------------------|
| recordId | String | Yes | Unique identifier of the record. | This output uniquely identifies each related record returned by the action. |
| recordTypeDisplayName | String | Yes | Display name of the record type which should be localized in the language specified with the `Accept-Language` header. For example, Contract. | This output indicates the display name of record type of each related record returned by the action. |
| recordTypePluralDisplayName | String | Yes | Plural display name of the record type which should be localized in the language specified with the `Accept-Language` header. For example, Contracts. | This output indicates the plural display name of the record type of each related record returned by the action. |
| recordType | String | Yes | System name of the record type. For example, contract. | This output indicates the type of each related record returned by the action. |
| recordTitle | String | Yes | Name of the record. For example, Contoso 2023 Renewal Contract. | This output indicates the title of each related record returned by the action. |
| url | String | No | A valid URL to open record in the partner application. | This output indicates the URL of each related record returned by the action. |
| additionalProperties | Object with Property Name and Property Value | No | Additional properties displayed in the detailed view. Property names and values are in natural language in the language specified with the `Accept-Language` header. For example, <br>{<br> "Status reason": "Signed off",<br> "Owner": "Kenny Smith" <br>} | This output indicates additional properties as name-value pairs of each related record returned by the action. |

### Example

```json
{
  "value": [
    {
      "recordId": "ID1",
      "recordTypeDisplayName": "Contract",
      "recordTitle": "50 Cafe A-100 Automatic Renewal Contract",
      "recordTypePluralDisplayName": "Documents",
      "recordType": "contract",
      "url": "https://contosohub.com/contract/id1",
      "additionalProperties": {
        "Status": "Signed",
        "Date": "9/7/23",
        "Signed by": "Alberto Burgos, Tony [last name]"
      }
    },
    {
      "recordId": "ID2",
      "recordTypeDisplayName": "Contract",
      "recordTitle": "ABC Company 2023 Renewal Contract",
      "recordTypePluralDisplayName": "Documents",
      "recordType": "contract",
      "url": "https://contosohub.com/contract/id2",
      "additionalProperties": {
        "Status": "Delivered",
        "Date": "9/3/23",
         "Signed by": "Alberto Burgos"
      }
    }
  ],
  "hasMoreResults": false
}

```

The following image shows an example of how the output of the API is mapped to the related records.

:::image type="content" source="media/extend-record-details.svg" alt-text="Screenshot showing anatomy of related records from a partner application.":::

Legend:
1. Card showing related records from partner application.
2. Icon and title of the card. The icon is retrieved from the Power Platform connector metadata. The card title is the name of the Power Platform connector.
3. Related record titles from API response. Two additional properties from API response are rendered as key fields of each related record.
4. More actions icon to either copy a link to the record or view record details in the partner application. The link is based on the URL of the related record in API response.
5. Additional properties of the related record from API response.

### See also

[Add a new Q&A capability to the Sales chat](extend-m365-chat.md)<br>
[Enrich email summary with insights from your application](extend-email-summary.md)<br>
[Enrich key sales info with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record summary with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)
