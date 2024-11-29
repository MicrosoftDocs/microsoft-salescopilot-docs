---
title: Extend Microsoft 365 Copilot for Sales with partner applications (preview)
description: Extend Copilot for Sales to integrate with partner applications to provide contextual insights and recommendations in Teams and Outlook.
ms.date: 11/29/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
---

# Extend Microsoft 365 Copilot for Sales with partner applications (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Copilot for Sales is an AI assistant that helps sales teams maximize productivity and close more deals. It brings sales insights and next-generation AI into the tools that you use daily, such as Outlook, Microsoft Teams, and other Microsoft 365 apps.  
Out of the box, Copilot for Sales connects to customer relationship management (CRM) systems such as Salesforce Sales Cloud and Dynamics 365 Sales. However, there is more to sales than just CRM. Sales teams often use specialized applications for account planning, prospecting, revenue intelligence, quoting, eSignature, and more. Customers and makers of sales applications can now bring data and insights from any of their applications into the Copilot for Sales experience.  
If you're a partner application developer, you can integrate your application with Copilot for Sales to provide contextual insights and recommendations in the context of the seller's daily workflow in Teams and Outlook.  
This article provides guidance about how to extend Copilot for Sales by using your application APIs. It provides the following information:  

- Capabilities that you can extend in Copilot for Sales  
- Input and output parameters for the APIs that you must build  
- Specific descriptions that Copilot for Sales searches for in your action to determine the intended API for a capability

The article also provides guidance about how to manage the input and output for the APIs.  

Watch the following video to learn more about Copilot for Sales extensibility.  

> [!VIDEO 28b9cf57-b05f-4b68-8a37-49310e749e1c]

## How does extensibility work in Copilot for Sales?

Copilot for Sales in Microsoft 365 consists of multiple individual capabilities that are made available contextually to users. Each capability is backed by a skill service that is owned by Copilot for Sales. When a system user interacts with a capability, the skill service for that capability generates the insights that are delivered as part of the capability. Out of the box, the skill service uses data in Microsoft Graph and CRMs to get insights. Through extensibility, the skill service gets additional insights, and therefore enriches the capability, by calling into your application APIs that are made available in your action in real time. When the skill service calls into your application APIs, it passes all available context that your application APIs accept. In return, it expects to receive insights in a format that is aligned with the way that insights are presented to Copilot for Sales users in the capability.

:::image type="content" source="media/extend-copilot-sales-arc.svg" alt-text="Diagram showing the extensibility architecture":::

To ensure that everything works correctly, Copilot for Sales must perform the following actions:

- Identify which of your application APIs is relevant for getting insights to enrich a specific Copilot for Sales capability.  
- Pass the required contextual information to your application API.  
- Determine which parts of your application APIs to render in the capability.

As a maker, you must build the following elements:

1. APIs that match the expectations of the Copilot for Sales capabilities that you're trying to extend. The API that is used to extend a capability in Copilot for Sales must accept the required inputs from Copilot for Sales and return the required outputs that Copilot for Sales expects.  
1. A Microsoft Power Platform connector that uses the APIs and OAuth authentication.  
1. An action that adds the Copilot for Sales–provided descriptions to the connector.  
    Copilot for Sales doesn't require adherence to a specific API specification. The naming of the API or its input/output parameters and structure aren't constraints for Copilot. You're responsible for ensuring that your APIs can handle the inputs that Copilot supplies, and that they return the expected outputs. Additionally, you must provide appropriate descriptions to ensure that Copilot can correctly match them during runtime.

For example, you want to enhance the [key sales information](key-sales-info.md) capability in Copilot for Sales. For this extension, you must create an API that, at a minimum, accepts a CRM record reference (passed as `recordType` and `recordId` parameter values) as input and provides the insight title, description, and date as output. This API should be added to a new or existing Microsoft Power Platform connector that uses OAuth for authentication. Additionally, the APIs in the connector should be supplemented with descriptions as required by Copilot for Sales.

## Copilot capabilities that can be extended

Through extensibility, you can enhance existing capabilities or add new capabilities in Copilot for Sales. You can bring data and insights from your application into the copilot experience. The following capabilities can be extended:

- [Email summaries](email-summary-premium.md)
- [Key sales information](key-sales-info.md)
- [Opportunity summaries](view-opportunity-summary.md)
- [Record details](view-record-details.md)

Additionally, you can introduce new question and answer (Q&A) capabilities in the chat features in Copilot for Sales. However, it's important to note that you can't add new capabilities to the non-chat features in Copilot for Sales.

## Extend Copilot for Sales

1. [Decide which capability you want to extend](#copilot-capabilities-that-can-be-extended).

    > [!NOTE]
    > If you want to extend a capability that isn't listed in the [Copilot capabilities that can be extended](#copilot-capabilities-that-can-be-extended) section, contact us by using the [Sign up for Copilot for Sales Extensibility Preview form](https://aka.ms/CopilotForSalesExtensibilityPreview).

1. Start to create an extension.  
    1. [Create a custom connector by using your APIs](custom-connector-action.md#create-and-test-a-custom-connector-in-microsoft-power-platform).  
    1. [Create and publish an action in Microsoft Copilot Studio](custom-connector-action.md#create-and-publish-an-action-in-copilot-studio).  
    1. [Enable the connector action for users](custom-connector-action.md#enable-the-connector-action-for-users).  
    1. [Get your connector and action certified (optional)](custom-connector-action.md#get-your-connector-and-action-certified-optional).  
1. [Learn about the extension points](build-apis.md) that you can use to extend the capability that you chose in step 1.

### Related information

[Add new question and answer (Q&A) capabilities to the Sales chat](extend-m365-chat.md)  
[Enrich email summaries with insights from your application](extend-email-summary.md)  
[Enrich key sales information with insights from your application](extend-key-sales-info.md)  
[Enrich CRM record details with insights from your application](extend-record-details.md)  
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)  
[Build Copilot for Sales extensions](build-apis.md)
