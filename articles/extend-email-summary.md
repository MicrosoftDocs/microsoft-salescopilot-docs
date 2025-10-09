---
title: Enrich email summary with content suggestions from your application (preview) 
description: Enhance email summaries in Outlook by using Sales app with content suggestions from your own application, sourced from CRM systems such as Dynamics 365 or Salesforce.
ms.date: 09/29/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Enrich email summary with content suggestions from your application (preview) 

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

When Copilot in Outlook and Sales app are used together, email summaries that are shown in Outlook include sales information that is sourced from your customer relationship management (CRM) system, such as Dynamics 365 or Salesforce CRM. You can extend the email summary capability that Sales app provides with insights from your own application.

> [!NOTE]
> This API replaces the existing _Email Summary Skill_ API (Operation Id: scp-get-email-insights) with a new version. 

## API description

You must add the following API description to the action. This helps Sales app identify the correct API to invoke for enriching the capability.

*This action gets additional sales insights that will be shown in C4S email summary experience inside outlook summary. The action enhances the existing skills of copilot for sales.*

## API details

- **API name**: Email Summary Skill Version 2
- **Swagger operation Id**: scp-get-email-insights-v2
- **Swagger operation method**: post 
- **Path**: `<PowerAppsConnectorHostName>/api/enhanceskills/email-insights-v2`


## Input payload

This payload goes as the request body of the API request.

| Name           | Data Type | Required | Details | Description to add in the action |
|----------------|-----------|----------|---------|----------------------------------|
| resourceData   | Object    | Yes      | The resource data to be used for fetching the suggested content. For the data structure, go to [Extensibility email data model](#extensibility-email-data-model). | This input identifies the email content which is a collection of email thread, subject, and other details. |
| relatedEntities   | Array    | No      | The array of related entities. For the data structure, go to [Related entity data model](#related-entity-data-model). | This input identifies the array of CRM records, which is related to the email thread. |
| crmType        | String    | No       | The type of CRM system, if connected. The valid values are Salesforce and Dynamics 365. | This input indicates the type of CRM in which the record related to the email thread exists. |
| crmOrgUrl      | String    | No       | The CRM organization URL. | This input indicates the URL of the CRM environment in which the record related to the email thread exists. |
| top            | Integer   | No       | The number of items to fetch. | This input indicates the number of file links to fetch. |
| skip           | Integer   | No       | The number of items to skip. | This input indicates the number of items to skip when fetching suggested file links. |

### Extensibility email data model

| Property  | Type | Details | Description to add in the action |
|-----------|------|---------|----------|
| plaintextBody | String  | The complete email body includes all the previous messages of the email thread in it.| This input provides all the content from the email thread in text format.   |
| fullHtmlBody | String  | The full HTML version of the email body that includes all the previous messages of the email thread in it. | This input provides all the content from the email thread in HTML format. |
| subject   | String   | Subject of the email. | This input provides the subject of the email.   |
| from    | String   | Sender's email address.  | This input provides the sender's email address. |
| to  | String[]  | Receiver's email addresses.   | This input provides the receiver's email address. |
| cc  | String[]  | Receiver's email addresses added in the Cc field of the email. | This input provides all the receiver's email addresses that are included in the Cc field of the email. |
| bcc | String[]  | Receiver's email addresses added in the Bcc field of the email.  | This input provides all the receiver's email addresses that are added in the Bcc field of the email. |
| sentDateTime  | DateTimeOffset | The date and time of the email in UTC format along with the Offset property. For more information, go to [DateTimeOffset Struct (System)](/dotnet/api/system.datetimeoffset?view=net-9.0&preserve-view=true) | This input provides the timestamp of the email. |
| messageId | String  | The Graph message Id of the email. | This input provides the message ID of the email. |
| conversationId | String  | The Graph conversation Id of the email thread. | This input provides the conversation ID of the email thread. |

### Related entity data model

| Property    | Type   | Required | Details | Description to add in the action |
|-------------|--------|----------|-----------|-----------------------------|
| entityId    | String | Yes   | The type of CRM record such as account or opportunity.  | This input provides the unique identifier of the CRM record that is related to the email thread. |
| entityType  | String | Yes   | The unique identifier of the CRM record to use for suggested contents. | This input identifies the record type in CRM, which is related to the email thread. |
| entitySource| String | No  | This input indicates the entity source, currently contains "connected" or empty values. | This input indicates the entity source type.  |

## Output parameters

Sales app expects to receive a list of insights (objects) from your APIs, and it expects each insight to have specific parameters. To ensure that Sales app can correctly parse the output, the response structure must adhere to the guidelines in the following table.

| Parameter | Data type | Required | Details |
|-----------|-----------|----------|---------|
| value | Array | Yes | <p>A list of insights (objects) that are defined as described in the [Schema for insights](#schema-for-insights) section.</p><p>**Note**: Although this parameter includes a list of insights, only the first insight is used in the email enrichment summary for Outlook Canvas experience.</p> |
| hasMoreResults | Boolean | No | A value that indicates whether more results are available. |

### Schema for insights

| Name | Data type/format | Required | Details | Description to add in the action |
|------|------------------|----------|---------|----------------------------------|
| insight | String | Yes | The insight that is delivered to users, such as *Your colleagues Mona Kane, Ray Tanaka, and Daniela Smith have worked with them before.* | This  output indicates the text you would like to be included in the email summary. |

### Example

```json
{
    "value": [
        {
            "insight": "Your colleagues Mona Kane, Ray Tanaka and Daniela Smith have worked with them before."
        },
        {
            "insight": "The email was opened three times in the last month."
        }
    ],
    "hasMoreResults": false
}
 
```

The example in the following image shows how the output of the API is mapped to the email summary in side pane.

:::image type="content" source="media/extend-email-summary-sidepane.png" alt-text="Screenshot showing insights from partner apps in the email summary.":::

Legend:

1. Title of the insight. Insights that have the same title are grouped together.
1. Descriptions of the insight. Each insight has one description.

The example in the following image shows how the output of the API is mapped to the email summary in the email body.

:::image type="content" source="media/extend-email-summary-oncanvas.png" alt-text="Screenshot showing insights from partner apps in the email body.":::

Legend:

1. Title of the insight. Insights that have the same title are grouped together.
1. Description of the insight. Each insight has one description.

### Related information

[Summarize an email thread using sales information with Copilot in Outlook](email-summary-premium.md)<br>
[Enrich opportunity insights with data from your application](extend-opportunity-insights.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Sales with partner applications](extend-copilot-for-sales.md)<br>
[Enrich email drafts with file links from your application](extend-email-draft.md)<br>
[Build Sales app extensions](build-apis.md)
