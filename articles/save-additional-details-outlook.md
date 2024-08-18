---
title: Configure how Outlook emails and events are saved to CRM
description: Learn how to configure fields that sellers can use to categorize emails and meetings in the CRM using Microsoft Copilot for Sales in Outlook.
ms.date: 06/10/2024
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.reviewer: shjais
ms.custom:
  - bap-template
ai-usage: ai-assisted
---

# Configure how Outlook emails and events are saved to CRM

As an administrator, you can configure the fields that sellers can use to categorize emails and meetings that they save to the customer relationship management (CRM) system. By categorizing emails and meetings in their CRM inbox, sellers can easily find and track their interactions with customers. For example, sellers might want to categorize emails and meetings based on priority, account, or deal stage.

## Prerequisites

CRM administrators must access admin settings from the Copilot for Sales app in Teams. For more information, go to [Microsoft Copilot for Sales admin settings](administrator-settings-for-viva-sales.md).

## Configure the fields to save to the CRM

You can select the fields that are saved to the CRM together with emails or meetings. Those fields are then shown to sellers when they save emails or meetings to the CRM.

1. In Copilot for Sales admin settings, select **Save to \<*type of CRM system*\>**.
1. Select **Save emails to \<*type of CRM system*\>** or **Save meetings to \<*type of CRM system*\>**, depending on the type of activity that you want to configure.

    :::image type="content" source="media/add-category-outlook.png" alt-text="Screenshot showing the Save emails to Salesforce settings in Copilot for Sales admin settings in Teams.":::

1. (Optional) Select **Refresh data** to get the latest updates to the fields from the CRM. For example, if the CRM administrator updated a field label in the CRM, you can refresh the data to view the updated label in Copilot for Sales.
1. In the **Categorize with fields** section, select **Add fields**.
1. In the **Add category** dialog box, select the fields that should be shown to sellers.

    The **Add category** dialog box shows all out-of-box and custom fields of the email and appointment entities in the CRM, except system fields. The dialog box shows only fields of the following types: option sets, lookup and text, multiple lines of text (plaintext/Memo), Boolean, and integer.

1. Save your changes.

The fields that you configured are now available to sellers when they save emails or meetings to the CRM. For more information, go to [Save Outlook activities to your CRM](save-outlook-activities-crm.md).
