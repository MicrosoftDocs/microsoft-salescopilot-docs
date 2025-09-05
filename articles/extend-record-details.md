---
title: Enrich CRM record details with insights from your application (preview)
description: Enhance your CRM record details with insights from your application by using the Copilot for Sales extension capability.
ms.date: 06/26/2025
ms.topic: how-to
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

Sellers can view details about a saved contact, together with associated records such as accounts and opportunities. You can extend the customer relationship management (CRM) record details capability that Copilot for Sales provides with insights from your own application.

## API description

You must add the following API description to the action. In this way, Copilot for Sales can identify the correct API that must be invoked to enrich the capability.

*This action gets records related to a CRM record. The action enhances the existing skills of Copilot for Sales.*

## API operation

This API uses Operation Type: GET

## Input parameters

Copilot for Sales is designed to provide the following input parameters to your APIs.

| Name | Data type/format | Required | Details | Description to add in the action |
|------|------------------|----------|---------|----------------------------------|
| recordType | String | Yes | The type of entity or object in CRM that related records are requested for. The value includes the language-agnostic unique name of the entity or object type, not the display name that can be localized. Examples include *account* and *opportunity*. | This input identifies the record type in CRM for which related records are requested. |
| recordId | String | Yes | The unique identifier of the CRM record. | This input provides the unique identifier of the CRM record for which related records are requested. |
| top | Integer | No | The number of activities to fetch. | This input indicates the number of related records to fetch. |
| skip | Integer | No | The number of activities to skip. | This input indicates the number of records to skip when fetching related records. |
| crmType | String | No | The type of CRM system. The valid values are *Dynamics 365* and *Salesforce*. | This input indicates the type of CRM the related records are fetched from. |
| crmOrgUrl | String | No | The host name of the CRM organization, such as *contoso.crm.dynamics.com*. | This input indicates the URL of the CRM environment the related records are fetched from. |

> [!NOTE]
> This extension point supports rendering insights from  up to five connector extensions in the Outlook sidecar.

## Output parameters

Copilot for Sales expects to receive a list of insights (objects) from your APIs, and it expects each insight to have specific parameters. To ensure that Copilot for Sales can correctly parse the output, the response structure must adhere to the guidelines in the following table.

| Parameter | Data type | Required | Details |
|-----------|-----------|----------|---------|
| value | Array | Yes | A list of insights (objects) that are defined as described in the [Schema for insights](#schema-for-insights) section. |
| hasMoreResults | Boolean | No | A value that indicates whether more results are available. |

### Schema for insights

| Name | Data type/format | Required | Details | Description to add in the action |
|------|------------------|----------|---------|----------------------------------|
| recordId | String | Yes | The unique identifier of the record. | This output uniquely identifies each related record returned by the action. |
| recordTypeDisplayName | String | Yes | The display name of the record type, such as *Contract*. It should be localized in the language that is specified through the `Accept-Language` header. | This output indicates the display name of record type of each related record returned by the action. |
| recordTypePluralDisplayName | String | Yes | The plural display name of the record type, such as *Contracts*. It should be localized in the language that is specified through the `Accept-Language` header. | This output indicates the plural display name of the record type of each related record returned by the action. |
| recordType | String | Yes | The system name of the record type, such as *contract*. | This output indicates the type of each related record returned by the action. |
| recordTitle | String | Yes | The name of the record, such as *Contoso 2023 Renewal Contract*. | This output indicates the title of each related record returned by the action. |
| url | String | No | A valid URL to open the record in the partner application. | This output indicates the URL of each related record returned by the action. |
| additionalProperties | An object that has **Property Name** and **Property Value** values of the *String* type | No | <p>Additional properties that are shown in the detailed view. Property names and values are in natural language in the language that is specified through the `Accept-Language` header. Here is an example.</p><pre>{<br> "Status reason": "Signed off",<br> "Owner": "Kenny Smith"<br>}</pre> | This output indicates additional properties as name-value pairs of each related record returned by the action. |

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

The example in the following image shows how the output of the API is mapped to the related records.

:::image type="content" source="media/extend-record-details.svg" alt-text="Screenshot showing the anatomy of related records from a partner application.":::

Legend:

1. Card that shows related records from the partner application.
1. Icon and title of the card. The icon is retrieved from the Microsoft Power Platform connector metadata. The title is the name of the Microsoft Power Platform connector.
1. Related record titles from the API response. Two additional properties from the API response are rendered as key fields of each related record.
1. "More actions" button that can be used either to copy a link to the record or to view record details in the partner application. The link is based on the URL of the related record in the API response.
1. Additional properties of the related record from the API response.

### Related information

[View record details](view-record-details.md)<br>
[Enrich email summaries with insights from your application](extend-email-summary.md)<br>
[Enrich email drafts with file links from your application](extend-email-draft.md)<br>
[Enrich opportunity insights with data from your application](extend-opportunity-insights.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft 365 Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build Copilot for Sales extensions](build-apis.md)
