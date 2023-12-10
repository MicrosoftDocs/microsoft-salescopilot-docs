---
title: GetRelatedActivities API (preview)
description: Get the latest activities from partner application to be shown in the opportunity summary.
ms.date: 12/11/2023
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

# GetRelatedActivities (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

The `GetRelatedActivities` API is used to get latest activities from your application to be shown in the opportunity summary. The API is called when the opportunity summary is shown to the seller. 

## Input parameters

The API is called with the following parameters:

|Parameter|Data type|Required|Description|
|---------|----|--------|-----------|
|recordType|String|Yes|Entity or Object type in CRM for which related activities are requested. It includes language agnostic unique name of the entity or object type, and not the display name that can be localized. For example, account, opportunity, and so on.|
|recordId|String|Yes|Unique identifier of the CRM record.|
|startDateTime|String with format 'date-time'|No|Start date and time to look up activities. The format is as per OpenAPI specification, for example, 2017-07-21T17:32:28Z.|
|endDateTime|String with format 'date-time'|No|End date and time to look up activities. The format is as per OpenAPI specification, for example, 2017-07-21T17:32:28Z.|
|top|Integer|No|Number of activities to fetch.|
|skip|Integer|No|Number of activities to skip.|
|crmType|String|No|Valid values are Dynamics 365 and Salesforce.|
crmOrgUrl|String|No|Host name of the CRM organization. For example, `contoso.crm.dynamics.com`.|

> [!NOTE]
> - Authentication is expected to be handled by the constructs in the Power Platform connector and is outside the scope of this API.
> - Current user's language is passed in the request header as `Accept-Language`. Use this for any language specific operations.
> - Read the following headers from the request to your connector and send them to your backend for a better diagnostics:
>   - `x-ms-client-request-id`: A unique identifier for the incoming request. 
>   - `x-ms-user-agent`: Value used as "sales-copilot".

## Output parameters

The API is expected to return activities in the following format:

|Parameter|Data type|Required|Description|
|---------|----|--------|-----------|
|value|Each activity has the information as mentioned in [Schema for an activity record](#schema-for-an-activity-record).|Yes|List of latest activity records from non-CRM application.|
|hasMoreResults|Boolean|No|Indicates if there are more results available.|

### Schema for an activity record

|Parameter|Data type|Required|Description|
|---------|----|--------|-----------|
|title|String|Yes|Title of the activity in the citation card.<br>It is the natural language title of the activity in the language specified in the `Accept-Language` request header. For example, Contract signed.|
|description|String|Yes|Description of the activity displayed as bullet points in the opportunity summary.<br>It is the natural language description of the activity in the language specified with the `Accept-Language` header. For example, Kenny, Logan, and two others signed the Contoso 2023 Renewal Contract on 9/7/2023.|    
|dateTime|String with format 'date-time'|Yes|Date and time of the activity in UTC format. If there is a start and end time, application needs to decide which one to show.<br>The format is as per OpenAPI specification, for example, 2017-07-21T17:32:28Z.|
|url|String|No|A valid URL to open activity in the partner application.|
|additionalProperties|Object with Property Name and Property Value|No|Additional properties displayed in the detailed view. Property names and values are in natural language in the language specified with the `Accept-Language` header. For example, <br>{<br>“Status reason”: “Signed off”,<br>“Owner”: “Kenny Smith”<br>}|

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

To see an example of how the above response is displayed in the Copilot for Sales pane, see [Show latest activities from your application in opportunity summary](extend-sales-copilot.md#show-latest-activities-from-your-application-in-opportunity-summary).

### See also

[GetRelatedRecords](api-get-related-records.md)