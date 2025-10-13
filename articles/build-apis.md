---
title: Build Sales app extensions (preview)
description: Explore how to build extensions that enhance capabilities and introduce new ones for Sales app.
ms.date: 06/26/2025
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/07/2024
---

# Build Sales app extensions (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This section outlines what Sales app expects from your application APIs that either enhance an existing capability or introduce a new one. It covers the following aspects:

- The input context that your application APIs can expect from Sales app (the capability)  
- The type of insights that each capability can show in the user interface (and therefore what your APIs should provide)  
- The descriptions that are needed at the API level, and for each API input and output, to help Sales app identify the correct API to invoke at runtime

> [!NOTE]
> Although these definitions are provided with high confidence, they are subject to change based on our internal reviews, testing, and feedback. Some descriptions might currently be empty. We are in the process of defining these descriptions and will provide updates in a future version of the guide.

This section provides the information that you need to enrich the following Sales app capabilities with insights from your application:

- [Email summaries](extend-email-summary.md)
- [Opportunity insights](extend-opportunity-insights.md)
- [Customer relationship management (CRM) record summaries](extend-record-summary.md)
- [CRM record details](extend-record-details.md)

### Related information

[Enrich email summaries with insights from your application](extend-email-summary.md)<br>
[Enrich opportunity insights with data from your application](extend-opportunity-insights.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Sales app with partner applications](extend-sales-app.md)
