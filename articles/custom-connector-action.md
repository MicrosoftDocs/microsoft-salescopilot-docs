---
title: Create a custom connector and connector action (preview)
description: Learn how to build a custom connector for Microsoft Power Platform and create an action in Microsoft Copilot Studio to enhance Copilot for Sales.
ms.date: 09/16/2024
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

This article provides concise instructions to help you quickly start to build a Microsoft Power Platform connector by using your application APIs, so that you can extend Copilot for Sales. For more comprehensive information about connectors, go to [Connectors overview](/connectors/overview).

After you build your custom connector, you must create an action in Microsoft Copilot Studio, enable it for your users, and get it certified.

## Create and test a custom connector in Microsoft Power Platform

[Download the OpenAI file](https://go.microsoft.com/fwlink/p/?linkid=2272334) to quickly get started with the connector actions that are needed to extend Copilot for Sales. The OpenAI file contains swagger for an API that is designed to get content suggestions in an email. You can disregard this swagger, because the Copilot for Sales user interface doesn't support the API.

You can create a custom connector from either [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/). 

Be sure to use an environment where Dynamics 365 apps are enabled, because environments of this type are used in the Copilot for Sales Outlook add-in. Environments without Dynamics 365 apps, such as the default environment, aren't supported for custom connectors. To create a new environment where Dynamics 365 apps are enabled, go to [Create an environment with a database](/power-platform/admin/create-environment#create-an-environment-with-a-database).

When you set up authentication for the connector, be sure to use the OAuth 2.0 authentication type, and be sure to use Microsoft Entra ID as the authentication provider. (Microsoft Entra ID was previously known as Azure Active Directory or Azure AD.) In this way, your back-end service can receive Microsoft Entra ID tokens that can then be exchanged when Microsoft services such as Microsoft Graph are invoked. The connector and the back-end service are secured by using two different application registrations, as described in [Set up Microsoft Entra ID authentication](/connectors/custom-connectors/create-web-api-connector#set-up-microsoft-entra-id-authentication).

For the steps to create a custom connector, set up authentication, and test the connector, go to [Create a custom connector from an OpenAPI definition](/connectors/custom-connectors/define-openapi-definition).

> [!NOTE]
> To automatically create connection for connector plugins using Microsoft Entra ID, you must set the **Enable on-behalf-of login** value to "true" in the **Security** section of the custom connector. For more information, see [Manage connections](/power-apps/maker/canvas-apps/add-manage-connections#consent-dialog-fine-grained-permssions)

## Create and publish an action in Copilot Studio

Actions determine what operations are performed with the custom insights and data sources, such as the custom connectors that you built. They enable Copilot for Sales to identify the external sources that insights should be extracted from to enrich the Copilot for Sales experience. You can create actions based on the connector that you developed by using Copilot Studio. For more information, go to [Create and configure copilot plugins](/microsoft-copilot-studio/copilot-plugins-overview).

> [!NOTE]
> If Copilot for Sales doesn't currently appear in Copilot Studio, ask your administrator to [deploy the Copilot for Sales enhanced Teams app](/microsoft-sales-copilot/enable-license#deploy-the-copilot-for-sales-app).

## Enable the connector action for users

Before Copilot for Sales users can access a connector action that is published in Copilot Studio, a Copilot for Sales administrator must enable it. If you want to enable a connector action for your copilot users, ask your administrator to [follow these steps](/microsoft-copilot-studio/manage-copilot-for-sales).

> [!NOTE]
> - Actions enabled by your administrator could take upto four hours to be ingested in Copilot for Sales experiences.
> - When you enable a connector action for Copilot for Sales, Copilot for Sales users in Microsoft 365 and Teams applications might be able to send and receive data from external sources by using Copilot for Sales, even if the same connector action was disallowed for direct use with Microsoft 365. Before you enable a connector action, we recommend that you ensure that it complies with your organization's policies.
> - The data and insights that connector actions bring to Copilot for Sales experiences are powered by third parties. They might be subject to third-party terms and conditions and/or privacy policies. We recommend that you validate these connector actions for compliance with your organization's policies.

## Get your connector and action certified (optional)

After you create a custom connector and connector action in Copilot Studio, they become accessible in your tenant. If you want to make your connector and action available to all Copilot for Sales users, you must get them certified. Learn more about [getting your Power Platform connector and plugin certified](/connectors/custom-connectors/submit-certification). To get your connector and action certified, you must [prepare Power Platform connector and plugin files for certification](/connectors/custom-connectors/certification-submission).

## See also

[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build Copilot for Sales extensions](build-apis.md)
