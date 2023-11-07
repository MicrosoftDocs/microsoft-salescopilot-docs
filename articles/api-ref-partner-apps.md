---
title: 
description: 
ms.date: 11/13/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
---

# Get latest activities and related records from partner applications in Sales Copilot (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

The opportunity summary in Sales Copilot shows latest activities from your connected CRM system. It provides a list of latest developments related to the opportunity. The content is generated using notes in the timeline of the opportunity record in your CRM system. This capability can be extended to show latest activities from non-CRM applications (first-party or third-party) to provide a unified view of related activities across applications.

When you view details of a CRM record in Sales Copilot, you can see related records from your connected CRM system. This capability can be extended to show related records from non-CRM applications (first-party or third-party) to provide a unified view of related records across applications.

Implement the following APIs to extend the Sales Copilot capabilities:
- GetRelatedActivities
- GetRelatedRecords

## GetRelatedActivities

The `GetRelatedActivities` API is used to get latest activities from your application to be shown in the opportunity summary. The API is called when the opportunity summary is shown to the seller. The API is called with the following parameters:

|Parameter|Type|Required|Description|
|---------|----|--------|-----------|
|recordType|String|Yes|Entity or Object type in CRM for which releated activities are requested. It includes:<ul></ul>
