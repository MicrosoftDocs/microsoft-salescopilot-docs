---
title: Build application APIs to extend Copilot for Sales (preview)
description: Explore how to build application APIs that enhance capabilities and introduce new ones for Copilot for Sales.
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

# Build application APIs to extend Copilot for Sales (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This section outlines what Copilot for Sales expects from your application APIs that either enhance an existing capability or introduce a new one. It covers the following aspects:

- The input context that your application APIs can anticipate from Copilot for Sales (capability).
- The kind of insights that each capability can display in the user interface (and hence, what your APIs should provide).
- The descriptions needed at the API level, and for each API input and output, to assist Copilot for Sales in identifying the correct API to invoke at runtime.

> [!NOTE]
> These definitions are provided with high confidence, but they are subject to change based on our internal reviews, testing, and feedback. Some descriptions might currently be empty. We are in the process of defining these and will provide updates in a future version of the guide.

In this section, you'll find the information to enrich the following Copilot for Sales capabilities with insights from your application:

- [Email summary](extend-email-summary.md)
- [Key sales information](extend-key-sales-info.md)
- [CRM record summary](extend-record-summary.md)
- [CRM record details](extend-record-details.md)
- [Q&A capabilities in chat](extend-m365-chat.md)

### See also

[Add a new Q&A capability to the Sales chat](extend-m365-chat.md)<br>
[Enrich email summary with insights from your application](extend-email-summary.md)<br>
[Enrich key sales info with insights from your application](extend-key-sales-info.md)<br>
[Enrich CRM record details with insights from your application](extend-record-details.md)<br>
[Enrich CRM record summary with insights from your application](extend-record-summary.md)<br>
[Extend Microsoft Copilot for Sales with partner applications](extend-copilot-for-sales.md)