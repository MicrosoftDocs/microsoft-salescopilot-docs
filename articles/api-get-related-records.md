---
title: GetRelatedRecords (preview)
description: Get related records from partner application to be shown in Sales Copilot when a seller views details of a CRM record.
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


# GetRelatedRecords (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

The `GetRelatedRecords` API is used to get related records from your application to be shown in Sales Copilot when a seller views details of a CRM record. The API is called when the seller views details of a CRM record. 

## Input parameters

The API is called with the following parameters:

|Parameter|Data type|Required|Description|
|---------|----|--------|-----------|
|recordType|String|Yes|Entity or Object type in CRM for which related records are requested. It includes language agnostic unique name of the entity or object type, and not the display name that can be localized. For example, account, opportunity, and so on.|
|recordId|String|Yes|Unique identifier of the CRM record.|
|top|Integer|No|Number of activities to fetch.|
|skip|Integer|No|Number of activities to skip.|
|crmType|String|No|Valid values are Dynamics 365 and Salesforce.|
crmOrgUrl|String|No|URL of the CRM organization. <br>Send host name only, for example, https://contoso.crm.dynamics.com.|

> [!NOTE]
> - Authentication is expected to be handled by the constructs in the Power Apps connector and is outside the scope of this API.
> - Current user's language is passed in the request header as `Accept-Language`. Use this for any language specific operations.
> - Read the following headers from the request to your connector and send them to your backend for a better diagnostics:
>   - `x-ms-client-request-id`: A unique identifier for the incoming request. 
>   - `x-ms-user-agent`: Value used as "sales-copilot".

## Output parameters

The API is expected to return related records in the following format:

|Parameter|Data type|Required|Description|
|---------|----|--------|-----------|
|value|Each related record has the information as mentioned in [Schema for a related record](#schema-for-a-related-record).|Yes|List of related records from non-CRM application.|
|hasMoreResults|Boolean|No|Indicates if there are more results available.|

### Schema for a related record

|Parameter|Data type|Required|Description|
|---------|----|--------|-----------|
|recordId|String|Yes|Unique identifier of the record.|
|recordTypeDisplayName|String|Yes|Display name of the record type which should be localized in the language specified with the `Accept-Language` header. For example, Contract.|
|recordTypePluralDisplayName|String|Yes|Plural display name of the record type which should be localized in the language specified with the `Accept-Language` header. For example, Contracts.|
|recordType|String|Yes|System name of the record type. For example, contract.|
|recordTitle|String|Yes|Name of the record. For example, Contoso 2023 Renewal Contract.|
|url|String|No|URL to open record in the partner application.|
|additionalProperties|Object with Property Name and Property Value|No|Additional properties displayed in the detailed view. Property names and values are in natural language in the language specified with the `Accept-Language` header. For example, <br>{<br>“Status reason”: “Signed off”,<br>“Owner”: “Kenny Smith”<br>}|

### See also

[GetRelatedActivities](api-get-related-activities.md)