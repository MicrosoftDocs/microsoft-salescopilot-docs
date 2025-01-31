---
title: Enrich email drafts with file links from your application (preview)
description: Enhance email drafts in Outlook by using Copilot for Sales and file links from your own application, sourced from CRM systems such as Dynamics 365 or Salesforce.
ms.date: 12/11/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Enrich email drafts with file links from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

When you use Copilot for Sales to draft an email, it considers the email's intent and uses CRM information from Salesforce or Dynamics 365 to create the draft. You can extend the email drafting capability that Copilot for Sales provides with recommended files from your own application.

> [!NOTE]
> This feature is supported only for email drafts created using the Copilot for Sales side pane in Outlook.

## API description

You must add the following API description to the action. In this way, Copilot for Sales can identify the correct API that must be invoked to enrich the capability.

*This action gets files relevant to the email conversation, which will be shown in C4S email drafts in Outlook. The action enhances the existing skills of copilot for sales.*

## API Operation

This API uses Operation Type: POST

## Input payload

This payload goes as the request body of the API request.

| Name           | Data Type | Required | Details | Description to add in the action |
|----------------|-----------|----------|---------|----------------------------------|
| resourceData   | Object    | Yes      | The resource data to be used for fetching the suggested content. For the data structure, go to [Extensibility email data model](#extensibility-email-data-model). | This input identifies the email content which is a collection of email thread, subject, and other details. |
| resourceType   | String    | Yes      | The type of resource for which to fetch content suggestions. For example, 'email-thread' or 'teams-chat'. | This input identifies the type of resource shared for fetching suggested file links which in this case is 'email-thread'. |
| recordType     | String    | No       | The type of CRM record such as account or opportunity. | This input identifies the record type in CRM, which is related to the email thread. |
| recordId       | String    | No       | The unique identifier of the CRM record to use for suggested contents. | This input provides the unique identifier of the CRM record that is related to the email thread. |
| crmType        | String    | No       | The type of CRM system, if connected. The valid values are Salesforce and Dynamics 365. | This input indicates the type of CRM in which the record related to the email thread exists. |
| crmOrgUrl      | String    | No       | The CRM organization URL. | This input indicates the URL of the CRM environment in which the record related to the email thread exists. |
| inputPrompt    | String    | No       | The currently used suggested prompt given by the user to generate email draft. For example, "Reply to a Concern" or "Make a Proposal". | This input indicates the prompt provided by the user while drafting an email. |
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
| cc  | String[]  | Receivers' email addresses added in the Cc field of the email. | This input provides all the receiver's email addresses that are included in the Cc field of the email. |
| bcc | String[]  | Receivers' email addresses added in the Bcc field of the email.  | This input provides all the receiver's email addresses that are added in the Bcc field of the email. |
| sentDateTime  | DateTimeOffset | The date and time of the email in UTC format along with the Offset property. For more information, go to DateTimeOffset Struct (System) | This input provides the timestamp of the email. |
| messageId | String  | The Graph message Id of the email. | This input provides the message ID of the email. |
| conversationId | String  | The Graph conversation Id of the email thread. | This input provides the conversation ID of the email thread. |


## Output parameters

| Property | Data Type | Required | Details |
|----------|-----------|----------|---------|
| value           | Array     | Yes      | A list of file links (objects) that are defined as described in the Schema for file or link content suggestions response. |
| hasMoreResults  | Boolean   | No       | A value that indicates whether more results are available. |

### Schema for file or link content suggestions response

| Name  | Data Type Format | Required | Details | Description to add in the action |
|-----------|-----------|----------|------------|----------------|
| contentType  | string | Yes | The type of content to show. More information, go to [Predefined values for contentType](#predefined-values-for-contenttype) | This output indicates the type of content included with the email draft. |
| content | string  | Yes | Actual content included. It can either be a web page or a URL of the file. | This output indicates the actual content that is included with the email draft. It can either be a web page or a URL. |
| contentTitle  | string  | Yes | Title of the suggested content shown to the user.   | This output indicates the title of the content.    |
| contentDescription | string | Yes  | Description of the suggested content shown to the user.  | This output indicates the text to be included when describing the files.  |
| contentIconUrl | string | No  | Icon of the suggested content shown to the user. If not provided, a generic icon is used. | This output indicates the icon to be included for the content.                                   |
| additionalProperties  | Object  | No  | A set of name-value pairs that indicate additional properties of the related file link that the action returns. | This output indicates additional properties as name-value pairs of each related link returned by the action. |

### Predefined values for contentType

| String value    | Type of content                        |
|-----------------|----------------------------------------|
| content-file    | External File (Generic)                |
| content-web     | External Webpage                       |
| content-doc     | Microsoft Word Document                |
| content-pdf     | Microsoft PDF Document                 |
| content-pptx    | Microsoft PowerPoint Presentation      |
| content-xlsx    | Microsoft Excel Spreadsheet            |

### Example

```json
{
  "value": [
    {
      "contentType": 0,
      "content": "https://www.bing.com",
      "contentTitle": "Purchase Contract",
      "contentDescription": "Purchase Contract Description",
      "contentIconUrl": null,
      "additionalProperties": {
        "Recipients": "Logan Edwards",
        "Sender Name": "Kenny Smith"
      }
    },
    {
      "contentType": 3,
      "content": "https://www.microsoft.com",
      "contentTitle": "Strategy Planning",
      "contentDescription": "Strategy Planning Description",
      "contentIconUrl": null,
      "additionalProperties": {
        "Recipients": "Gabriela Edwards",
        "Sender Name": "Maria Smith"
      }
    },
    {
      "contentType": 1,
      "content": "https://www.bing.com",
      "contentTitle": "Contoso Website",
      "contentDescription": "Contoso Website Description",
      "contentIconUrl": null,
      "additionalProperties": {
        "Total Views": "100",
        "Domain": "Contoso.com"
      }
    }
  ],
  "hasMoreResults": false
}

```

The example in the following image shows how the output of the API is mapped to the email draft.

:::image type="content" source="media/extend-email-draft.png" alt-text="Screenshot showing file links from partner apps in the email draft.":::

Legend:

1. File links from partner apps.

## See also

[Summarize an email thread using sales information with Copilot in Outlook](email-summary-premium.md)<br>
[Enrich email summaries with insights from your application](extend-email-summary.md)<br>
[Enrich key sales information with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft 365 Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build Copilot for Sales extensions](build-apis.md)
