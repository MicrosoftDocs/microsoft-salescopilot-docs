---
title: Configure how Outlook emails and events are saved to CRM
description: Learn how to configure fields that sellers can use to categorize emails and meetings in CRM using Microsoft Copilot for Sales in Outlook.
ms.date: 08/19/2024
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

As an administrator, you can configure the fields that sellers can use to categorize their emails and meetings when they're saved to CRM. By categorizing emails and meetings in their CRM inbox, sellers can easily find and track their interactions with customers. For example, sellers might want to categorize emails and meetings based on priority, account, or deal stage.

You can also control whether sellers can save attachments along with the email or meeting to CRM. When attachments saving is enabled, you can also configure whether all attachments are selected or not by default to be saved to CRM. In either case, sellers can choose which attachments to save when they save the email or meeting to CRM.

## Prerequisites

CRM administrators must access administrator settings from the Copilot for Sales app in Teams. More information: [Administrator settings for Copilot for Sales](administrator-settings-for-viva-sales.md)

## Configure fields to save in CRM

1. In Copilot for Sales admin settings, select **Save to (CRM)**.

1. Select **Save emails to (CRM)** or **Save meetings to (CRM)** depending on the type of activity you want to configure.
   You can select different fields to save along with the email or meeting to CRM. The fields you select are displayed to sellers when they save the email or meeting to CRM.

    :::image type="content" source="media/add-category-outlook.png" alt-text="Screenshot of Save emails to CRM settings page in Copilot for Sales in Teams.":::

1. (Optional) Select **Refresh data** to get the latest updates to the fields from CRM. For example, if the CRM administrator has updated a field label in CRM, you can refresh the data to see the updated label in Copilot for Sales.

1. In the **Categorize with fields** section, select **Add fields** and select the fields from the **Add category** dialog.

   The **Add category dialog** displays all the out-of-the-box and custom fields of email and appointment entities in CRM, except the system fields. Only fields of type option sets, lookup and text, multiple lines of text (plaintext/Memo), boolean, integer are displayed in the dialog.

1. Save the changes.

   Sellers can now see the fields you configured when they save emails or meetings to CRM. More information: [Save Outlook activities to your CRM](save-outlook-activities-crm.md)

## Configure attachment saving settings

1. In Copilot for Sales admin settings, select **Save to (CRM)**.

1. To configure attachment saving settings for emails:

    1. Under the **Save emails to (CRM)** section, turn on **Save attachments with emails**.

    1. To save all attachments by default, select **Save all attachments in the email by default**. If you don't select this option, sellers can choose which attachments to save when they save the email to CRM. 

        :::image type="content" source="media/save-attach-admin.png" alt-text="Screenshot of Save attachments with emails admin settings.":::

1. To configure attachment saving settings for meetings:

    1. Under the select **Save meetings to (CRM)**, turn on **Save attachments with meetings**.

    1. To save all attachments by default, select **Save all attachments in the meeting by default**. If you don't select this option, sellers can choose which attachments to save when they save the meeting to CRM.

### See also

[Save Outlook activities to your CRM](save-outlook-activities-crm.md)