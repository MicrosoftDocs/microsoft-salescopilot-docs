---
title: Sample OpenAPI definition (preview)
description: Sample OpenAPI definition for the API implementation.
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

# Sample OpenAPI definition (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Refer to the following guidelines when creating the OpenAPI definition for the API implementation.

- The OpenAPI definition contains placeholders for the actual API paths. You can replace the placeholders with the actual API paths. The actual OpenAPI definition provided by the connector is used and requests are built based on the API paths in the OpenAPI definition.
- HTTP methods should be same as the ones specified in the OpenAPI definition.
- Input parameter names should be the same as the ones specified in the OpenAPI definition. OpenAPI definition returned by the connector is used to map the input parameters by descriptions. All the required input parameters in the sample OpenAPI definition must be present in the actual connector definition.
- Input parameter types should be same as the ones specified in the OpenAPI definition. 
- APIs described by the OpenAPI definition shouldn't contain any other required parameters that aren't present in the sample OpenAPI definition. If there are any other required parameters, Copilot for Sales won't invoke the APIs and will fail with an internal error.
- Do not use `connectorId` as an input parameter in the OpenAPI definition as it's a reserved parameter.
- Properties of output objects that are marked as required in the OpenAPI definition must be present in the API response.

## Sample OpenAPI file

[Download the OpenAPI file](https://go.microsoft.com/fwlink/p/?linkid=2272334) to quickly start with the connector actions needed to extend Copilot for Sales.

### See also

[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build application APIs to extend Copilot for Sales](build-apis.md)