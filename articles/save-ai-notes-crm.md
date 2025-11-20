---
title: Configure how AI meeting notes are saved from Teams recap to CRM
description: Learn how to configure how AI meeting notes are saved from Teams recap to CRM using the Sales app in Teams.
ms.date: 11/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ai-usage: ai-assisted
---

# Configure how AI meeting notes are saved from Teams recap to CRM

As an administrator, you can enable or disable the ability to save AI-generated meeting notes to CRM directly from Teams meeting recap summary page. By default, this feature is enabled. 

This feature allows your sellers to keep their CRM up to date with the latest meeting notes, ensuring that important information is captured and accessible to the entire team. This helps to improve collaboration and communication within the organization, ultimately leading to better sales outcomes.

To configure how AI meeting notes are saved from Teams recap to CRM: 

1. In the Sales app admin settings, select **Save to (CRM)**. 
1. Under the **Save AI meeting notes from Teams to (CRM)** section, turn on or off the **Save AI meeting notes from Teams recap** toggle.
1. Select one of the following options:
   - **Save to appointment description field by default**: This option saves the AI-generated meeting notes to the appointment description field in CRM by default.
       > [!NOTE]
       > If you're using Salesforce as your CRM, the **Description** field of the **Event** object does not support HTML formatting. Therefore, the AI-generated meeting notes are saved as plain text in the **Description** field.
   - **Save to specified record**: This option allows you to select a specific record and its field in CRM where the AI-generated meeting notes will be saved. You can choose from a list of available records in your CRM system. After you select this option, perform the following steps:
     1. Select **Add record**.
     1. In the **Add a record type** window, select the record type from the list of available records or search for a specific record type using the search bar.
     1. Select **Next**.
     1. In the **Select a field** window, select the field where you want to save the AI-generated meeting notes. 
     1. Select **Add and save**.
        > [!NOTE]
        > If you're using Salesforce as your CRM, ensure that the field you select is of type **Rich Text Area** because it supports HTML formatting.

### Related information

[Save AI-generated meeting notes to CRM](view-meeting-summary-recap.md#save-ai-generated-meeting-notes-to-crm)