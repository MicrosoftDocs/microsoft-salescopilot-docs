---
title: Create a custom connector and connector action (preview)
description: Discover how to build a custom connector for Power Platform and create an action in Microsoft Copilot Studio, aimed at enhancing Copilot for Sales.
ms.date: 05/20/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Create a custom connector and connector action (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This article provides concise instructions to help you quickly start building a Power Platform connector using your application APIs, aimed at extending Copilot for Sales. For a more comprehensive understanding of connectors, see [Connectors overview](/connectors/overview).

After you have built your custom connector, you must create an action in Microsoft Copilot Studio, enable it for your users, and get it certified.

## Create and test a custom connector in Power Platform

[Download the OpenAI file](https://go.microsoft.com/fwlink/p/?linkid=2272334) to quickly start with the connector actions needed to extend Copilot for Sales. The OpenAI file contains swagger for an API designed to get content suggestions in an email. This can be disregarded as the Copilot for Sales user interface doesn't support this API.

You can create a custom connector either from [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/). 

Ensure to use an environment that has Dynamics 365 apps enabled, as these are the environments used in Copilot for Sales Outlook add-in. Environments without Dynamics 365 apps, such as the default environment, aren't supported for custom connectors. To create a new environment with Dynamics 365 apps enabled, see [Create an environment with a database](/power-platform/admin/create-environment#create-an-environment-with-a-database).

When setting up the authentication for the connector, ensure to use the OAuth 2.0 authentication type and Microsoft Entra ID (formerly known as Azure Active Directory) as the authentication provider. This enables your backend service to receive Microsoft Entra ID tokens that can then be exchanged when invoking Microsoft services such as Graph. The connector and the backend service are secured using two different application registrations as mentioned in the [Set up Microsoft Entra ID authentication](/connectors/custom-connectors/create-web-api-connector#set-up-microsoft-entra-id-authentication) article.

For steps to create a custom connector, set up authentication, and test the connector, see [Create a custom connector from an OpenAPI definition](/connectors/custom-connectors/define-openapi-definition).

## Create and publish an action in Microsoft Copilot Studio

Actions determine the operations to be performed with the custom insights and data sources, such as the custom connectors you've built. They enable Copilot for Sales in identifying which external sources to extract insights from, thereby enriching the Copilot for Sales experience. You can create actions based on the connector you've developed using Microsoft Copilot Studio. More information: [Create and configure copilot plugins](/microsoft-copilot-studio/copilot-plugins-overview).

> [!NOTE]
> - To see Copilot for Sales in Copilot Studio, reach out to your admin to deploy the Copilot for Sales enhanced Teams app, see [Deploy the Copilot for Sales app](/microsoft-sales-copilot/enable-license#deploy-the-copilot-for-sales-app)

## Enable the connector action for users

For Copilot for Sales users to access a connector action published in Microsoft Copilot Studio, it must first be enabled by a Copilot for Sales administrator. To enable a connector action for your copilot users,
ask your administrator to [sign up for the preview feature](https://aka.ms/SalesCopilotExtensibilityPreview). The Microsoft team will get in touch to validate the request and enable the feature for your organization. 

> [!NOTE]
> - By enabling a connector action for Copilot for Sales, you may be allowing Copilot for Sales users on Microsoft 365 and Teams applications to send and receive data from external sources using Copilot for Sales even if the same connector action has been disallowed for use directly with Microsoft 365. It is recommended to ensure that this action complies with your organization policies before enabling it.
> - The data and insights that connector actions bring to Copilot for Sales experiences are powered by third parties and may be subject to third party terms and conditions and/or privacy policies. We recommend you validate such connector actions for compliance with your organization policies.

## Get your connector and action certified (optional)

Upon creating a custom connector and connector action in Microsoft Copilot Studio, it becomes accessible within your tenant. However, if you wish to make it available to all Copilot for Sales users, you must get your connector and action certified. More information: More information: [Create and configure copilot plugins](/microsoft-copilot-studio/copilot-plugins-overview).

### See also

[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)
