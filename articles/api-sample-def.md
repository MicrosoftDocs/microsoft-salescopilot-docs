---
title: Sample connector (preview)
description: Sample connector to help you easily start to extend Sales.
ms.date: 09/29/2025
ms.topic: concept-article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
  - ai-gen-title
---

# Sample connector (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

You can use the certified connector action based on [Contoso Hub - Connectors](/connectors/contosohub/) to check out the extensibility points available in Sales.

To try the certified connector action, follow the instructions in [Manage extensions for Sales app](/microsoft-copilot-studio/manage-copilot-for-sales) and enable the Contoso Hub connector action for Sales app.


You can edit the sample connector and action to get started quickly. Refer to the following guidelines when you edit the create the connector or its actions:

- The sample connector contains placeholders for the API paths. You can replace these placeholders with the actual API paths.
- HTTP methods should match the ones that are specified in the sample OpenAPI definition.
- The OpenAPI definition that the connector returns is used to map the input and output parameters based on the descriptions. All the required parameters in the sample OpenAPI definition must be present in the actual connector definition, and they must have correct descriptions.
- Input parameter types should match the ones that are specified in the OpenAPI definition. 
- APIs that are described by the OpenAPI definition should not contain any required parameters that aren't present in the sample OpenAPI definition. Otherwise, Sales app doesn't invoke the APIs and fails with an internal error.
- Don't use `connectorId` as an input parameter in the OpenAPI definition, because it's a reserved parameter.
- Properties of output objects that are marked as required in the OpenAPI definition must be present in the API response.
- Each connector API should complete its execution within five seconds, especially the connector actions that enhance existing capabilities.
- Authentication is expected to be handled by the constructs in the Microsoft Power Platform connector and is outside the scope of each API.
- The current user's language is passed in the request header as `Accept-Language`. Use it for any language-specific operations.
- Read the following headers from the request to your connector, and send them to your back end for better diagnostics:

    - `x-ms-client-request-id`: A unique identifier for the incoming request.
    - `x-ms-user-agent`: "sales-copilot" is used as the value.


### Related information

[Extend Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build Sales app extensions](build-apis.md)
