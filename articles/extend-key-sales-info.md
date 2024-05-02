---
title: Enrich key sales info with insights from your application (preview)
description: 
ms.date: 05/15/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/07/2023
---

# Enrich key sales info with insights from your application (preview)

[!INCLUDE [production-ready-preview-dynamics365](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Sellers can use Copilot for Sales while reading and composing emails in Outlook to view key sales information about contacts, accounts, and opportunities that are related to the email. Key sales information is based on either the opportunity connected to the email or the most relevant opportunity based on the contacts and accounts in the email. You can extend the key sales information capability provided by Copilot for Sales with insights from your own application.

## API description

You need to add the API description to the plugin action to enable Copilot for Sales to identify the correct API to invoke for enriching this capability. The description must be as follows:

`This action gets additional sales insights that will be shown in C4S key sales info card in outlook sidecar. The action enhances the existing skills of copilot for sales.`

## Input parameters

Copilot for Sales is designed to provide the following input parameters to your plugin APIs.

| Name | Data type / Format | Required | Details | Description to be added in plugin |
|------|--------------------|----------|---------|----------------------------------|
| recordType | String with one for the following values: account, opportunity, lead, contact. | Yes | Record Type in CRM. | This input identifies the record type in CRM for which key sales info is requested. |
| recordId | String | Yes | Record ID in CRM. | This input provides the unique identifier of the CRM record for which key sales info is requested |
| crmType | String | No | Type of CRM system. Valid values: Salesforce, Dynamics365 | This input indicates the type of CRM in which the CRM record exists, for which key sales info is requested |
| crmOrgUrl | String | No | CRM Organization URL. | This input indicates the URL of the CRM environment in which the CRM record exists, for which key sales info is requested |
| top | Integer | No | Number of insights to fetch. | This input indicates the number of sales highlights to fetch |
| skip | Integer | No | Number of insights to skip. | This input indicates the number of items to skip when fetching sales highlights |