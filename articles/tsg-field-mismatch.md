---
title: Field mismatch between Dynamics 365 and Sales Copilot
description: Troubleshoot and resolve field mismatching errors between Dynamics 365 and Sales Copilot with this article.
ms.date: 01/05/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-title
  - ai-seo-date:12/22/2023
  - ai-gen-desc
---

# Field mismatch between Dynamics 365 and Sales Copilot

This article helps you troubleshoot and resolve error in Sales Copilot when a user gets a field mismatching error for a record.

## Who is affected?

| Requirement type |Description  |
|---------|---------|
|**Client app**     |  Sales Copilot Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Dynamics 365        |
|**Users**     | Users who get a field mismatch error  |

## Symptom

When users try to use Sales Copilot, the following error message is displayed indicating a field mismatch between CRM and Sales Copilot: `Align missing fields` 

Due to this error, users are unable to use Sales Copilot.

:::image type="content" source="media/tsg-field-mismatch.png" alt-text="Field mismatch error.":::

## Cause

A field in a record exists in Sales Copilot but not in CRM. The field is removed from the CRM after an administator has configured fields of the record from admin settings in Sales Copilot.

## Solution

Check with the record owner to see if the field is removed by mistake. If the field is removed by mistake, ask the record owner to add the field back to the record in CRM. If the field is removed intentionally, [remove the field from the record in Sales Copilot](customize-forms-and-fields.md#remove-fields).

## Is your issue still not resolved?

Visit the [Sales Copilot - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.