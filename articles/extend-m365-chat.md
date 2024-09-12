---
title: Add new question and answer (Q&A) capabilities to the Sales chat (preview)
description: Enhance your Microsoft 365 Copilot chat with a new Q&A feature for sellers, to introduce insights directly from various applications.
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

# Add new question and answer (Q&A) capabilities to the Sales chat (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Copilot for Sales extends the Microsoft 365 Copilot chat by providing a question and answer (Q&A) experience to sellers, so that they can ask questions and get answers from a partner application in the chat interface. You can introduce new Q&A capabilities in the chat experience by using your actions. In this way, you can bring insights from various applications directly to sellers in the chat interface.

> [!NOTE]
> This feature isn't enabled by default. To enable it, contact us by using the [Sign up for Copilot for Sales Extensibility Preview form](https://aka.ms/CopilotForSalesExtensibilityPreview).

:::image type="content" source="media/extend-sales-chat.png" alt-text="Screenshot showing the Sales chat.":::

## Input parameters

The process of introducing new capabilities in the Q&A experience differs significantly from the process of enriching the out-of-box capabilities in the non-chat experience. For the Q&A experience, there are no predefined inputs from Copilot for Sales. Instead, based on the context and the user's question in the chat, the copilot orchestrator passes relevant inputs to the parameters that are defined in the swagger actions. Currently, this experience supports parameters of data types such as *int*, *double*, and *string*. However, it doesn't support complex or nested objects.

> [!NOTE]
> Copilot for Sales can't currently pass the entire user utterance as-is to an action. It supports only simple skill-like APIs, such as computing engagement scores for an opportunity.

## Output parameters

Copilot for Sales expects APIs that introduce new capabilities in the chat to return one or more adaptive cards. There are three variations in terms of how Copilot for Sales expects and displays the response from your action:

- Structured data or insights about one record or topic
- Structured data or insights about multiple records or topic
- Free-form data or insights

For an example that shows how the output parameters are returned, go to the [Sample expected output in JSON format](#sample-expected-output-in-json-format) section.

### Structured data or insights about one record or topic

:::image type="content" source="media/extend-sales-chat-one-topic.svg" alt-text="Screenshot showing one record in the Sales chat.":::

Legend:

1. Logo that is sourced from the action metadata.
1. Title that is obtained from the API response.
1. Subtitle that is derived from the API response.
1. Section that shows additional information as key-value pairs. The data is sourced from the API response.
1. "Call to action" button. The URL is derived from the API response. The button text can be either "Open \<*object type*\>" or "Open in \<*action name*\>."

### Structured data or insights about multiple records or topic

When the API returns multiple adaptive cards, Copilot for Sales compiles a summary of the cards and provides numbered citations. Users can select the citation numbers to view the individual cards.

:::image type="content" source="media/extend-sales-chat-multiple-topics.svg" alt-text="Screenshot showing multiple records in the Sales chat.":::

Legend:

1. Summary card that Copilot for Sales generates
1. Citation number that can be selected to open more details from the summary
1. Citation card that shows the full details of one adaptive card that the API returned

### Free-form data or insights

:::image type="content" source="media/extend-sales-chat-free-form.svg" alt-text="Screenshot showing free-form data in the Sales chat.":::

Legend:

1. Card that Copilot for Sales generates based on the API response.
1. Title that is based on the action name, in the form "Info from \<*action name*>."
1. Body text that is derived from the API response. It has one paragraph and a maximum of 230 characters.
1. Other sections in the body. Each section has a title (a maximum of three words) and a list of textual bullet points (one sentence each). In each section, there must be at least one bullet point, and there can be a maximum of five bullet points.
1. "Call to action" button. The URL is sourced from the API response. The button text is in the form "Open in \<*action name*\>."

### Sample expected output in JSON format

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

Here is an example of an adaptive card in JavaScript Object Notation (JSON) format. To visualize it, open the [Adaptive Card Designer](https://adaptivecards.io/designer/), and paste the following JSON content into the **Card Payload Editor** area.

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
            "text": "Body 1 a short sentence a short sentence a short sentence a short sentence a short sentence. This is some awesome text.",
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

## See also

[Enrich email summaries with insights from your application](extend-email-summary.md)<br>
[Enrich key sales information with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build Copilot for Sales extensions](build-apis.md)
