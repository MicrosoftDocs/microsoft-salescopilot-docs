---
title: Configure how Outlook emails and events are saved to CRM
description: Learn how to configure fields that sellers can use to categorize emails and meetings in the CRM using the Sales agent in Outlook.
ms.date: 08/06/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
ms.reviewer: shjais
ms.custom:
  - bap-template
ai-usage: ai-assisted
---

# Configure how Outlook emails and events are saved to CRM

As an administrator, you can customize how sellers save and categorize emails and meetings in their customer relationship management (CRM) system. This article explains how to configure fields for categorization, manage attachment saving options, and control which activities can be saved to CRM. Use these settings to help sellers organize customer interactions and streamline their workflow in Outlook.

## Prerequisites

CRM administrators must access admin settings from the Sales agent in either Outlook or Teams. For more information, go to [Sales agent admin settings](administrator-settings-sales-app.md).

## Enable or disable saving emails and meetings to CRM

You can control if sellers can save emails and meetings to the CRM. By default, the settings to save emails and meetings to the CRM are turned on. If you turn them off, sellers will no longer be able to save emails and meetings to the CRM.

1. In the Sales agent admin settings, select **Save to (CRM)**.
1. To turn off saving emails to CRM, turn off **Save emails to (CRM)**.
1. To turn off saving meetings to CRM, turn off **Save meetings to (CRM)**.

    :::image type="content" source="media/save-to-crm.png" alt-text="Screenshot showing the settings to save Outlook activities to CRM in the Sales agent admin settings in Teams.":::

## Configure the fields to save to the CRM

You can select the fields that are saved to the CRM together with emails or meetings. Those fields are then shown to sellers when they save emails or meetings to the CRM. Sellers can easily find and track customer interactions by categorizing emails and meetings in their CRM inbox. For example, sellers might want to categorize emails and meetings based on priority, account, or deal stage.

> [!NOTE]
> - Additional fields for categorization are not supported in the following scenarios: 
>   - When saving recurring meeting series to Dynamics 365.
>   - When tracking draft emails.

**Prerequisite**: Depending on the type of activity that you want to configure, [saving emails or meetings to CRM must be enabled](#enable-or-disable-saving-emails-and-meetings-to-crm).

1. In the Sales agent admin settings, select **Save to (CRM)**.  
1. Select **Save emails to (CRM)** or **Save meetings to (CRM)**, depending on the type of activity that you want to configure.
1. (Optional) Select **Refresh data** to get the latest updates to the fields from the CRM. For example, if the CRM administrator updated a field label in the CRM, you can refresh the data to view the updated label in the Sales agent.  
1. In the **Categorize with fields** section, select **Add fields**.  

    :::image type="content" source="media/add-category-outlook.png" alt-text="Screenshot showing the Save emails to CRM settings in the Sales agent admin settings in Teams.":::

1. In the **Add category** dialog box, select the fields that should be shown to sellers.  
    The **Add category** dialog box shows all out-of-box and custom fields of the email and appointment entities in the CRM, except system fields. The dialog box shows only fields of the following types: option sets, look up and text, multiple lines of text (plaintext/Memo), Boolean, and integer.  
1. Save your changes.  

The fields you configured are now available to sellers when they save emails or meetings to the CRM. For more information, go to [Save Outlook activities to your CRM](save-outlook-activities-crm.md).

## Configure how emails and meetings are connected to CRM records

> [!NOTE]
> This feature supports only Dynamics 365.

By default, sellers can connect a saved email or meeting to a single record in Dynamics 365. That record is stored in the **Regarding** field in the email or meeting activity in Dynamics 365. You can change this behavior to give sellers more flexibility in how they associate activities with CRM records. You can configure whether sellers can connect a saved email or meeting to one record, multiple records, or a primary record and related records. The connection options you configure apply to both emails and meetings.

1. Depending on the type of activity that you want to configure, [enable saving emails or meetings to CRM](#enable-or-disable-saving-emails-and-meetings-to-crm).
1. In the Sales agent admin settings, select **Save to Dynamics 365**.
1. Select **Save emails to (CRM)** or **Save meetings to (CRM)**, depending on the type of activity that you want to configure.
1. Under **Choose how (emails or meetings) are connected to Dynamics 365 records**, select one of the following options:
    - **Connect to one record**: Sellers can connect the activity to a single CRM record by using the **Regarding** field. This option is the default behavior.
    - **Connect to multiple records**: Sellers can connect the activity to one or more CRM records by using the **Related to** field.
    - **Connect to a primary record and related records**: Sellers can connect the activity to a primary record by using the **Regarding** field, and to additional records by using the **Related to** field.

    :::image type="content" source="media/multi-regarding.png" alt-text="Screenshot showing the options to connect emails and meetings to multiple CRM records in the Sales agent admin settings.":::

1. Save your changes.

When sellers save an email or meeting to CRM, the fields they see reflect the option you configured.

> [!IMPORTANT]
> Post-meeting experiences such as saving meeting notes and associating insights derived from those notes are based only on the CRM record connected through the **Regarding** field. Records connected through the **Related to** field aren't used for these experiences.

## Configure attachment saving settings

You can control whether sellers can save attachments along with the email or meeting to CRM. When attachment saving is enabled, you can also configure whether all attachments are selected or not by default to be saved to CRM. In either case, sellers can choose which attachments to save when they save the email or meeting to CRM.

> [!NOTE]
> Saving attachments is not supported when saving recurring meeting series to Dynamics 365.

**Prerequisite**: Depending on the type of activity that you want to configure, [saving emails or meetings to CRM must be enabled](#enable-or-disable-saving-emails-and-meetings-to-crm).

1. In the Sales agent admin settings, select **Save to (CRM)**.  
1. To configure attachment saving settings for emails:  
    1. Under the **Save emails to (CRM)** section, turn on **Save attachments with emails**.  
    1. To save all attachments by default, select **Save all attachments in the email by default**. If you don't select this option, sellers can choose which attachments to save when they save the email to CRM.  
        :::image type="content" source="media/save-attach-admin.png" alt-text="Screenshot of Save attachments with emails admin settings.":::  
1. To configure attachment saving settings for meetings:  
    1. Under the **Save meetings to (CRM)** section, turn on **Save attachments with meetings**.  
    1. To save all attachments by default, select **Save all attachments in the meeting by default**. If you don't select this option, sellers can choose which attachments to save when they save the meeting to CRM.

### Related information

[Save Outlook activities to your CRM](save-outlook-activities-crm.md)

