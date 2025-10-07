---
title: Standardize error responses (preview)
description: Standardize error responses to ensure consistent and understandable messages.
ms.date: 03/28/2025
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

# Standardize error responses (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Error responses must be standardized to ensure that the error messages are consistent and easy to understand. The following table lists the schema for the error object that is expected in the response body.

| Name | Data type | Required | Description |
|------|-----------|----------|-------------|
| errorCode | String | Yes | A short and easy-to-identify error category. |
| errorMessage | String | No | A developer-friendly message for more details about the error. |
| activityId | String | No | A unique identifier for the request. |
| details | Object | No | <p>More details about the error. Content might vary, depending on the error type.</p><p>The following example shows a case where a user doesn't have the correct privileges.</p><pre>{<br> "resourceType": "envelope",<br> "resourceId": "&lt;envelopeId&gt;"<br>}</pre> |

The following table lists a few scenarios and the expected error codes.

| Scenario | Error code | HTTP status code |
|----------|------------|------------------|
| The customer relationship management (CRM) system that the user is connected to differs from the one that is specified in the input. | INVALID_CRM_CONNECTION | 400 |
| The CRM system of record wasn't found, or it was deleted. | RECORD_NOT_FOUND | 404 |
| The user isn't authenticated. (This scenario typically occurs when the token expires.) | INVALID_TOKEN_SPECIFIED | 401 |
| The user isn't authorized to perform an action. (In other words, the user has insufficient privileges). | INSUFFICIENT_PERMISSIONS | 403 |
| Too many requests were sent to the connector. | REQUEST_THROTTLED | 429 |
| An unhandled service error occurred. | INTERNAL_SERVER_ERROR | 500 |

### Related information

[Extend Sales with partner applications](extend-copilot-for-sales.md)<br>
[Build Copilot for Sales extensions](build-apis.md)
