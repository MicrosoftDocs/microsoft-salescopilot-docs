---
title: Sample Connector (preview)
description: Sample connector to easily get started with extending Copilot for Sales.
ms.date: 05/29/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
  - ai-gen-title
---

# Sample Connector (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Refer to the following guidelines when creating the OpenAPI definition for the connector and its actions.

- The sample connector contains placeholder for the API paths. You can replace these placeholders with the actual API paths.
- HTTP methods should be same as the ones specified in the sample OpenAPI definition.
- OpenAPI definition returned by the connector is used to map the input and output parameters by descriptions. All the required parameters in the sample OpenAPI definition must be present in the actual connector definition with right descriptions.
- Input parameter types should be same as the ones specified in the OpenAPI definition. 
- APIs described by the OpenAPI definition shouldn't contain any other required parameters that aren't present in the sample OpenAPI definition. If there are any other required parameters, Copilot for Sales won't invoke the APIs and will fail with an internal error.
- Do not use `connectorId` as an input parameter in the OpenAPI definition as it's a reserved parameter.
- Properties of output objects that are marked as required in the OpenAPI definition must be present in the API response.
- Each connector action should complete its execution within 5 seconds, especially the connector actions that enhance existing capabilities. 

## Getting started

1. [Download the sample connector solution](https://go.microsoft.com/fwlink/p/?linkid=2272334).
2. [Import the downloaded connector solution using Power Apps](/power-apps/maker/data-platform/import-update-export-solutions). Ensure to use an environment that has Dynamics 365 apps enabled.
3. [Navigate to Copilot Studio and create an extension for the connector](/microsoft-copilot-studio/copilot-ai-plugins?tabs=c4s#author-a-connector-action).

### See also

[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)
