---
title: Enrich email summaries with insights from your application (preview)
description: Enhance email summaries in Outlook by using Copilot for Sales and insights from your own application, sourced from CRM systems such as Dynamics 365 or Salesforce.
ms.date: 05/29/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Enrich email summaries with insights from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

When Copilot in Outlook and Copilot for Sales are used together, email summaries that are shown in Outlook include sales information that is sourced from your customer relationship management (CRM) system, such as Dynamics 365 or Salesforce CRM. You can extend the email summary capability that Copilot for Sales provides with insights from your own application.

## API description

You must add the following API description to the action. In this way, Copilot for Sales can identify the correct API that must be invoked to enrich the capability.

*This action gets additional sales insights that will be shown in C4S email summary experience inside outlook summary. The action enhances the existing skills of copilot for sales.*

## Input parameters

Copilot for Sales is designed to provide the following input parameters to your APIs.

| Name | Data type/format | Required | Details | Description to add in the action |
|------|------------------|----------|---------|----------------------------------|
| recordType | String | No | The record type in CRM. The record can specify the account, opportunity, lead, or contact that is related to the email. | This input identifies the record type in CRM, which is related to the summarized email. |
| recordId | String | No | The record ID in CRM that related records are requested for. | This input provides the unique identifier of the CRM record that is related to the summarized email. |
| crmType | String | No | The type of CRM system. The valid values are *Salesforce* and *Dynamics 365*. | This input indicates the type of CRM in which the record related to the summarized email exists. |
| crmOrgUrl | String | No | The CRM organization URL. | This input indicates the URL of the CRM environment in which the record related to the summarized email exists. |
| emailContacts | String | Yes | A comma-separated list of email addresses, such as `kenny@contoso.com,logan@contoso.com`. | This input indicates a list of all relevant participant emails in the current email thread. |
| Top | Integer | No | The number of insights to fetch. | This input indicates the number of insights to fetch. |
| Skip | Integer | No | The number of insights to skip. | This input indicates the number of items to skip when fetching insights. |

## Output parameters

Copilot for Sales expects to receive a list of insights (objects) from your APIs, and it expects each insight to have specific parameters. To ensure that Copilot for Sales can correctly parse the output, the response structure must adhere to the guidelines in the following table.

| Parameter | Data type | Required | Details |
|-----------|-----------|----------|---------|
| value | Array | Yes | <p>A list of insights (objects) that are defined as described in the [Schema for insights](#schema-for-insights) section.</p><p>**Note**: Although this parameter includes a list of insights, only the first insight is used in the email enrichment summary.</p> |
| hasMoreResults | Boolean | No | A value that indicates whether more results are available. |

### Schema for insights

| Name | Data type/format | Required | Details | Description to add in the action |
|------|------------------|----------|---------|----------------------------------|
| Title | String of up to 20 characters | Yes | The title of the sales insight. | This output indicates the title of the partner section and should include only the partner's name. |
| Description | String | Yes | The insight that is delivered to users, such as *Your colleagues Mona Kane, Ray Tanaka, and Daniela Smith have worked with them before.* | This output indicates the text you would like to be included in the email summary. |

> [!NOTE]
> Although the API requirements for extending email summary capabilities and record summary capabilities might look similar, they must be added as separate actions in the connector.

### Example

```json
{
    "value": [
        {
            "title": "From Contoso Customer Insights",
            "description": "Your colleagues Mona Kane, Ray Tanaka, and Daniela Smith have worked with them before."
        }
    ],
    "hasMoreResults": false
}
```

The example in the following image shows how the output of the API is mapped to the email summary.

:::image type="content" source="media/extend-email-summary.svg" alt-text="Screenshot showing insights from partner apps in the email summary.":::

Legend:

1. Title of the insight. Insights that have the same title are grouped together.
1. Description of the insight. Each insight has one description.

## See also

[Add new question and answer (Q&A) capabilities to the Sales chat](extend-m365-chat.md)<br>
[Enrich key sales information with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build Copilot for Sales extensions](build-apis.md)
