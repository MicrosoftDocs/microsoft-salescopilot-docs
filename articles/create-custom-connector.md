---
title: Create a custom connector with your plugin APIs (preview)
description: 
ms.date: 05/15/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
---

# Create a custom connector with your plugin APIs (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This article provides concise instructions to help you quickly start building a Power Platform connector using your application APIs, aimed at extending Copilot for Sales. For a more comprehensive understanding of connectors, see [Connectors overview](/connectors/overview).

## Create a cusom connector

Download the OpenAI file to quickly start with the connector actions needed to extend Copilot for Sales. Note that the OpenAI file contains swagger for an API designed to get content suggestions in an email. This can be disregarded as the Copilot for Sales user interface does not support this API.

You can create a custom connector either from [Power Apps](https://make.powerapps.com/) or [Power Automate](https://flow.microsoft.com/). 

Ensure to use an environment that has Dynamics 365 apps enabled, as these are the environments used in Copilot for Sales Outlook add-in. Environments without Dynamics 365 apps, such as the default environment, are not supported for custom connectors. to create a new environment with Dynamics 365 apps enabled, see [Create an environment with a database](/power-platform/admin/create-environment#create-an-environment-with-a-database)

For steps to create a custom connector, see [Create a custom connector from an OpenAPI definition](/connectors/custom-connectors/define-openapi-definition).