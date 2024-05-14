---
title: Enrich email summary with insights from your application (preview)
description: Enhance email summaries in Outlook using Copilot for Sales and insights from your own application, sourced from CRM systems like Dynamics 365 or Salesforce.
ms.date: 05/15/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Enrich email summary with insights from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

With Copilot in Outlook and Copilot for Sales together, email summaries are displayed in Outlook with sales information sourced from your CRM system, such as Dynamics 365 or Salesforce CRM. You can extend the email summary capability provided by Copilot for Sales with insights from your own application.

## API description

You need to add the API description to the action to enable Copilot for Sales to identify the correct API to invoke for enriching this capability. The description must be as follows:

`This action gets additional sales insights that will be shown in C4S email summary experience inside outlook summary. The action enhances the existing skills of copilot for sales.`

## Input parameters

Copilot for Sales is designed to provide the following input parameters to your APIs.

| Name | Data type / Format | Required | Details | Description to be added to the action |
|------|--------------------|----------|---------|---------------------------------------|
| recordType | String | No | Record Type in CRM. The value can be account, opportunity, lead, or contact that is related to the email. | This input identifies the record type in CRM which is related to the summarized email. |
| recordId | String | No | Record ID in CRM for which related records are requested. | This input provides the unique identifier of the CRM record which is related to the summarized email. |
| crmType | String | No | Type of the CRM system. Valid values are Salesforce and Dynamics 365. | This input indicates the type of CRM in which the record related to the summarized email exists. |
| crmOrgUrl | String | No | CRM Organization URL | This input indicates the URL of the CRM environment in which the record related to the summarized email exists. |
| emailContacts | String | Yes | Comma separated email addresses. For example: `kenny@contoso.com,logan@contoso.com` | This input indicates a list of all relevant participant emails in the current email thread. |
| Top | Integer | No | Number of insights to fetch | This input indicates the number of insights to fetch. |
| Skip | Integer | No | Number of insights to skip | This input indicates the number of items to skip when fetching insights. |

## Output parameters

Copilot for Sales anticipates receiving a list of insights (objects), each with specific parameters, from your APIs. To ensure the Copilot for Sales can parse the output correctly, it's crucial to follow the response structure outlined below.

|Parameter|Data type|Required|Details|
|---------|----|--------|-----------|
|value|Array|Yes|List of insights (objects) defined as mentioned in [Schema for insight](#schema-for-insight)|
|hasMoreResults|Boolean|No|Indicates if there are more results available.|

### Schema for insight

| Name | Data type / Format | Required | Details | Description to be added in action |
|------|--------------------|----------|---------|----------------------------------|
| Title | String, up to 20 characters | Yes | Title of the sales insight. | This output indicates the title of the partner section and should include only the partner's name. |
| Description | String | Yes | Insight delivered to the users. Ex: Your colleagues Mona Kane, Ray Tanaka and Daniela Smith have worked with them before. | This output indicates the text you would like to be included in the email summary. |

> [!NOTE]
> While the API requirements for extending the email summary and record summary capabilities may look similar, they must be added as separate actions in the connector.

### Example

```json
{
  "value": [
    {
      "title": "From Contoso Customer Insights",
      "description": "Your colleagues Mona Kane, Ray Tanaka and Daniela Smith have worked with them before."
    }
  ],
  "hasMoreResults": false
}
```

The following image shows an example of how the output of the API is mapped to the email summary.

`image`

### See also

[Add a new Q&A capability to the Sales chat](extend-m365-chat.md)<br>
[Enrich key sales info with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summary with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)