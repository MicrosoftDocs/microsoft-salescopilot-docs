---
title: Extend Microsoft Copilot for Sales with partner applications (preview)
description: Extend Copilot for Sales to integrate with partner applications to provide contextual insights and recommendations in Teams and Outlook.
ms.date: 06/14/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
---

# Extend Microsoft Copilot for Sales with partner applications (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Microsoft Copilot for Sales is an AI assistant designed for sales teams to maximize productivity and close more deals, bringing sales insights and next-generation AI into the tools you use daily like Microsoft Outlook, Microsoft Teams, and other Microsoft 365 apps.

Copilot for Sales connects to CRMs such as Salesforce Sales Cloud and Microsoft Dynamics 365 Sales out-of-box. However, sales is more than CRM. Sales teams often use specialized applications for account planning, prospecting, revenue intelligence, quoting, eSignature, and more. Customers and makers of sales applications can now bring data and insights from any of their applications into the Copilot for Sales experience. 

If you're a partner application developer, you can integrate your application with Copilot for Sales to provide contextual insights and recommendations in the context of the seller's daily workflow in Microsoft Teams and Outlook.

This article provides guidance on how to extend Copilot for Sales with your application APIs. It provides the following information:
- Capabilities you can extend in Copilot for Sales.
- Input and output parameters for the APIs you need to build.
- Specific descriptions searched by Copilot for Sales within your action to determine the intended API for a particular capability. It also guides you on how to manage the input and output for these APIs. 

Here's a video that gives you a quick overview about Copilot for Sales extensibility.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1lMwg]

## How does extensibility work in Copilot for Sales?

Copilot for Sales in Microsoft 365 is composed of multiple individual capabilities that are made available contextually to users. Each of these features is backed by a skill service owned by Copilot for Sales. When an end user interacts with a capability, the skill service for the capability generates the insights to deliver as part of that capability. Out-of-the-box, the skill service uses data in Graph and CRMs to get insights. With extensibility, the skill service calls into your application APIs made available in your action in real-time to get additional insights to enrich the capability. When the skill service calls into your application APIs, it passes all available context that your application APIs accept; and expects to get back insights in a format that aligns with how the insights are presented to users of the Copilot for Sales in the capability.

:::image type="content" source="media/extend-copilot-sales-arc.svg" alt-text="Screenshot showing extensibility architecture":::

To ensure that everything works properly, Copilot for Sales needs to:
- Identify which of your application APIs is relevant for getting insights to enrich a specific Copilot for Sales capability.
- Pass the required contextual information to your application API.
- Identify the right parts of your application APIs to render in the capability.


You, as a maker, must build:
1. The APIs that match the expectations of the Copilot for Sales capabilities you're trying to extend. The API used to extend a capability in Copilot for Sales must accept the required inputs from Copilot for Sales and return the required outputs expected by Copilot for Sales.
1. A Power Platform connector with the APIs and oAuth authentication.
1. An action that adds the Copilot for Sales provided descriptions to the connector.

    Copilot for Sales doesn't require adherence to a specific API specification. The naming of the API or its input/output parameters and structure aren't constraints for Copilot. Your responsibility is to ensure that your APIs can handle the inputs supplied by Copilot and return the expected outputs. Additionally, you must provide appropriate descriptions to enable Copilot to correctly match them during runtime.

For instance, suppose you wish to enhance the [Key sales info](key-sales-info.md) capability in Copilot for Sales. To do this, you need to create an API that, at least, accepts a CRM record reference (passed as 'recordType' and 'recordId') as input and provides the insight title, description, and date as output. This API should be added to a new or existing Power Platform connector that utilizes OAuth for authentication. Furthermore, the APIs in the connector should be supplemented with descriptions as required by Copilot for Sales.

## Copilot capabilities that can be extended

Extensibility enables you to enhance existing capabilities or add new capabilities in Copilot for Sales. You can bring data and insights from your application into the copilot experience. The following capabilities can be extended:
- [Email summary](email-summary-premium.md)
- [Key sales information](key-sales-info.md)
- [Opportunity summary](view-opportunity-summary.md)
- [Record details](view-record-details.md)

Additionally, you can introduce new Q&A capabilities to the chat features in Copilot for Sales. However, it's important to note that you can't add new capabilities to the non-chat features in Copilot for Sales.

## Extend Copilot for Sales

1. [Decide which of the capabilities you want to extend](#copilot-capabilities-that-can-be-extended).
    
    > [!NOTE]
    > If you want to extend any capability other than the ones listed [here](#copilot-capabilities-that-can-be-extended), contact us using [this link](https://aka.ms/CopilotForSalesExtensibilityPreview).

1. Get started with creating an extension
    1. [Create a custom connector with your APIs](custom-connector-action.md#create-and-test-a-custom-connector-in-power-platform).
    1. [Create and publish an action in Microsoft Copilot Studio](custom-connector-action.md#create-and-publish-an-action-in-microsoft-copilot-studio).
    1. [Enable the connector action for users](custom-connector-action.md#enable-the-connector-action-for-users).
    1. [Get your connector and action certified (optional)](custom-connector-action.md#get-your-connector-and-action-certified-optional).

1. [Know the extension points](build-apis.md) to extend the capabilities you chose in step 1.

### See also

[Add a new Q&A capability to the Sales chat](extend-m365-chat.md)<br>
[Enrich email summary with insights from your application](extend-email-summary.md)<br>
[Enrich key sales info with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summary with insights from your application](extend-record-summary.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)