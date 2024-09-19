---
title: Build Copilot for Sales extensions (preview)
description: Explore how to build extensions that enhance capabilities and introduce new ones for Copilot for Sales.
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

# Build Copilot for Sales extensions (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This section outlines what Copilot for Sales expects from your application APIs that either enhance an existing capability or introduce a new one. It covers the following aspects:

- The input context that your application APIs can expect from Copilot for Sales (the capability)
- The type of insights that each capability can show in the user interface (and therefore what your APIs should provide)
- The descriptions that are needed at the API level, and for each API input and output, to help Copilot for Sales identify the correct API to invoke at runtime

> [!NOTE]
> Although these definitions are provided with high confidence, they are subject to change based on our internal reviews, testing, and feedback. Some descriptions might currently be empty. We are in the process of defining these descriptions and will provide updates in a future version of the guide.

This section provides the information that you need to enrich the following Copilot for Sales capabilities with insights from your application:

- [Email summaries](extend-email-summary.md)
- [Key sales information](extend-key-sales-info.md)
- [Customer relationship management (CRM) record summaries](extend-record-summary.md)
- [CRM record details](extend-record-details.md)
- [Question and answer (Q&A) capabilities in chat](extend-m365-chat.md)

## See also

[Add new question and answer (Q&A) capabilities to the Sales chat](extend-m365-chat.md)<br>
[Enrich email summaries with insights from your application](extend-email-summary.md)<br>
[Enrich key sales information with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summaries with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft 365 Copilot for Sales with partner applications](extend-copilot-for-sales.md)
