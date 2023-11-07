---
title: Standardize error responses (preview)
description: Standardize error responses to ensure consistent and understandable messages.
ms.date: 11/13/2023
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

# Standardize error responses (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

Error responses must be standardized to ensure that the error messages are consistent and easy to understand. The following table lists the schema for the error object expected in the response body.

|Name|Data type|Required|Description|
|----|---------|--------|-----------|
|errorCode|String|Yes|Short and easy to identify an error category.|
|errorMessage|String|No|Developer friendly for more details on the error.|
|activityId|String|No|Unique identifier for the request.|
|details|Object|No|Additional details about the error. Content might vary based on the error type.<br>For example, a case when a user doesn't have correct privileges: <br>{<br>“resourceType”: “envelope”,<br>“resourceId”: “&lt;envelopeId&gt;”<br>}|

The following table lists a few scenarios and the expected error codes:

|Scenario|Error code|HTTP status code|
|--------|----------|----------------|
|User is connected to a different CRM than specified in the input|INVALID_CRM_CONNECTION|400|
|Record not found or has been deleted|RECORD_NOT_FOUND|404|
|User is not authenticated (typically in case of token expiration)|INVALID_TOKEN_SPECIFIED|401|
|User is not authorized to perform an action (insufficient privileges)|INSUFFICIENT_PERMISSIONS|403|
|Too many requests sent to the connector|REQUEST_THROTTLED|429|
|Unhandled service error|INTERNAL_SERVER_ERROR|500|

### See also

[GetRelatedActivities](api-get-related-activities.md) <br>
[GetRelatedRecords](api-get-related-records.md)