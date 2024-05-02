---
title: Build application APIs to extend Copilot for Sales (preview)
description: Discover how to build application APIs to extend Copilot for Sales.
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

# Build application APIs to extend Copilot for Sales (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

This section outlines what Copilot for Sales expects from your application APIs that either enhance an existing capability or introduce a new one. It covers the following aspects:

- The input context that your application APIs can anticipate from Copilot for Sales (capability).
- The kind of insights that each capability can display in the user interface (and hence, what your APIs should provide).
- The descriptions needed at the API level, as well as for each API input and output, to assist Copilot for Sales in identifying the correct API to invoke at runtime.

> [!NOTE]
> These definitions are provided with high confidence, but they are subject to change based on our internal reviews, testing, and feedback. Some descriptions might currently be empty. We are in the process of defining these and will provide updates in a future version of the guide.

In this section, you will find the information to enrich the following Copilot for Sales capabilities with insights from your application:

- Email summary
- Key sales information
- CRM record summary
- CRM record details
- Q&A capabilities in chat

### See also

[Extend Copilot for Sales with partner applications](extend-sales-copilot.md)