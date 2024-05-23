---
title: Add a new question and answer (Q&A) capability to the Sales chat (preview)
description: Enhance your Microsoft 365 Copilot chat with a new Q&A feature for sellers, introducing insights from various applications directly.
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

# Add a new question and answer (Q&A) capability to the Sales chat (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Copilot for Sales extends the Microsoft 365 Copilot chat by providing sellers with a question and answer (Q&A) experience to ask questions and get answers from a partner application within the chat interface. By using your actions, you can introduce new Q&A capabilities to the chat experience, thereby bringing insights from various applications directly to the sellers in the chat interface.

> [!NOTE]
> This feature is not enabled by default. To enable this feature, contact us using [this link](https://aka.ms/CopilotForSalesExtensibilityPreview).

:::image type="content" source="media/extend-sales-chat.png" alt-text="Screenshot showing sales chat.":::

## Input parameters

Introducing new capabilities to the Q&A experience significantly differs from enriching the out-of-the-box capabilities in the nonchat experience. Unlike the latter, the former doesn't have predefined inputs from Copilot for Sales. Instead, based on the context and user's question in the chat, the copilot orchestrator passes relevant inputs to the parameters defined in the swagger actions. Currently, this experience supports parameters of data types such as int, double, and string, but doesn't support complex or nested objects.

> [!NOTE]
> Copilot for Sales currently does not have the capability to pass the entire user utterance as-is to a action. It only supports simple skill-like APIs, such as computing engagement scores for an opportunity.

## Output parameters

Copilot for Sales anticipates that APIs introducing new capabilities to the chat return one or more adaptive cards. There are three variations in terms of how Copilot for Sales expects and displays the response from your action.

See the [sample expected output in the .json format](#sample-expected-output-in-the-json-format) for example about returning the output parameters.

### Structured data or insights about one record or topic

:::image type="content" source="media/extend-sales-chat-one-topic.svg" alt-text="Screenshot showing one record in sales chat.":::

Legend:
1. Logo – sourced from the action metadata
2. Title – obtained from the API response 
3. Subtitle – derived from the API response
4. Section displaying additional information as key-value pairs – sourced from the API response 
5. Call to action – The URL is derived from the API response. The button text can either be `Open <object type>` or `Open in <action name>`.

### Structured data or insights about multiple records or topic

When the API returns multiple adaptive cards, Copilot for Sales compiles a summary of the cards and provide citations that can be selected to view each individual card.

:::image type="content" source="media/extend-sales-chat-multiple-topics.svg" alt-text="Screenshot showing multiple records in sales chat.":::

Legend:
1. Summary card by Copilot for Sales
2. Citation number to view more details from summary
3. Citation card to show full details of each adaptive card returned by the API

### Free form data or insights

:::image type="content" source="media/extend-sales-chat-free-form.svg" alt-text="Screenshot showing free form data in sales chat.":::

Legend:
1. Card from Copilot for Sales based on the API response 
2. Title – formulated from the action name as `Info from <action name>` 
3. Body text (one paragraph, max 230 characters) derived from the API response 
4. Other sections in the body, each with a title (max three words) and text bullets (1 sentence each). Minimum 1 bullet, Maximum 5 bullets 
5. Call to action – The URL is sourced from the API response. The button text is in the format `Open in <action name>` 

### Sample expected output in the .json format

```json
{
    "adaptiveCards": [
      {
        "adaptiveCard": "<a serialized adaptive card with version 1.5 (see the example of adaptive card below)>",
        "previewCardData": {
          "title": "title 1",
          "subTitle": "subTitle 1",
          "url": "https://adaptivecards.io/"
        }
      },
      {
        "adaptiveCard": "<a serialized adaptive card with version 1.5 (see the example of adaptive card below)>",
        "previewCardData": {
          "title": "title 1",
          "subTitle": "subTitle 1",
          "url": "https://adaptivecards.io/"
        }
      }
    ]
  }
```

Here's an example of an adaptive card in .json format. To visualize it, open [Designer | Adaptive Cards](https://adaptivecards.io/designer/), and then paste the following .json content into the **Card Payload Editor** area.

```json
{
    "type": "AdaptiveCard",
    "body": [
        {
            "type": "TextBlock",
            "text": "Info from [Partner name]",
            "wrap": true,
            "weight": "default"
        },
        {
            "type": "TextBlock",
            "text": "Body 1 a short sentence a short sentence  a short sentence a short sentence a short sentence. This is some awesome text.",
            "wrap": true,
            "spacing": "None"
        },
        {
            "type": "Container",
            "spacing": "Medium",
            "items": [
                {
                    "type": "TextBlock",
                    "text": "Body 2 (optional)",
                    "wrap": true,
                    "spacing": "Large"
                },
                {
                    "type": "TextBlock",
                    "text": "- Smith sent Renewal Contract on 04/23/2023",
                    "wrap": true,
                    "spacing": "None"
                },
                {
                    "type": "TextBlock",
                    "text": "- Alberto Burgos is the primary contact for the Alpine Ski House account.",
                    "wrap": true,
                    "spacing": "None"
                },
                {
                    "type": "TextBlock",
                    "text": "- Smith sent Renewal Contract on 04/23/2023",
                    "wrap": true,
                    "spacing": "None"
                }
            ]
        },
        {
            "type": "Container",
            "spacing": "Medium",
            "items": [
                {
                    "type": "TextBlock",
                    "text": "Body 5 (optional)",
                    "wrap": true
                },
                {
                    "type": "TextBlock",
                    "text": "- Body 3 (paragraph with bullets)",
                    "wrap": true,
                    "spacing": "None"
                },
                {
                    "type": "TextBlock",
                    "text": "- Body 3 (paragraph with bullets)",
                    "wrap": true,
                    "spacing": "None"
                },
                {
                    "type": "TextBlock",
                    "text": "- Body 3 (paragraph with bullets)",
                    "wrap": true,
                    "spacing": "None"
                }
            ]
        }
    ],
    "actions": [
        {
            "type": "Action.OpenUrl",
            "title": "Open [partner name]",
            "url": "https://adaptivecards.io",
            "iconUrl": "https://connectoricons-prod.azureedge.net/master/1.0.1460.2388/docusign/icon.png"
        }
    ],
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "version": "1.5"
}
```

### See also

[Enrich email summary with insights from your application](extend-email-summary.md)<br>
[Enrich key sales info with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summary with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)
