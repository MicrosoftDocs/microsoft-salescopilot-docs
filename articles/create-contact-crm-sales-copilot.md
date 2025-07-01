---
title: Create a contact in your CRM from Copilot for Sales
description: Learn how to create a contact in your CRM from Copilot for Sales.
ms.date: 02/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Create a contact in your CRM from Copilot for Sales

If an external contact doesn't exist in your CRM, create a contact in the CRM right from Copilot for Sales.

> [!TIP]
> Enter the contact's email address in the following format when you compose an email or meeting invitation: **FirstName LastName &lt;email address&gt;**. If you do, the corresponding items in the CRM contact form fill automatically.

Here's the video that shows how to create a contact in your CRM from Copilot for Sales:

> [!VIDEO ee9d39c5-4f97-4355-9515-e7ace2866ebf]

**To create a contact**:

1. In the **Copilot for Sales** pane, hover over an unsaved contact, and then select **Add to (CRM)**.

   :::image type="content" source="media/dynamics-salesforce.png" alt-text="Screenshot showing how to add multiple external contacts on the Dynamics 365 tab.":::

1. In the **New contact** form, add the required information, and then select **Save**.

   > [!NOTE]
   > If your administrator has disabled the inline record creation, the **New Contact** form opens in your CRM to fill in the details. More information: [Configure new contact creation](customize-forms-and-fields.md#configure-new-record-creation)

   :::image type="content" source="media/add-person.png" alt-text="Screenshot showing how to create a contact inline.":::

   > [!NOTE]
   > You can also open the contact form in your CRM. Select **Open in (CRM)**, and then enter details.

    Copilot for Sales automatically connects the new CRM contact to your external contact.

> [!IMPORTANT]
>
> With the implementation of the global create feature in Copilot for Sales, contact creation might fail when you are using the external contact creation process. To continue creating contacts in CRM, perform the following steps in Teams admin settings:
>1. Go to **Settings** > **Environment** > **Forms** > **Contact**.  
>1. Select one of the following options:  
>      - **Create new records inside Copilot for Sales**  
>      - **Create new records by opening Salesforce from a link**  
>1. Save the settings and create the contact again.

## Signature available in email

If you open the **Copilot for Sales** pane from an incoming email that contains the signature of the sender, and you add the contact to your CRM, Copilot for Sales prefills the contact details based on the signature and highlights the fields that it populated. You can update the information and select **Save**.

This capability is available only for emails in the [supported languages](introduction.md#supported-languages-and-geographies-and-geographies).

:::image type="content" source="media/pre-fill.png" alt-text="Screenshot showing prefilled details from signature.":::

## Add new contacts through quick CRM actions in email banners

When you read, compose, or reply to emails with external contacts in the From, To, or Cc fields, you can add new contacts to your CRM using quick CRM actions in the banner message. 

When you read an email from external contacts, if at least one contact in the email thread isn't saved in your CRM, the banner message at the top of the email includes an action that you can use to add the new contacts. Currently, banner messages in this scenario are available on up to two external emails per user per day. If you don't want these banners to appear, [ask your administrator to disable them](m365-admin-setting.md).

When you compose an email, create a meeting invite, or reply to an email or a meeting invite with external contacts, if at least one contact in the email isn't saved in your CRM, the banner message at the top of the email includes an action to add the new contacts. The banner message in this scenario is displayed for every email that contains external contacts.

1. Open an email that has external contacts.
1. In the banner message, select **Add contact** or **Add contacts**.
1. In the **Copilot for Sales** pane, hover over the unsaved contact, and then select **Add**. If [leads support is enabled](customize-forms-and-fields.md#configure-leads-support-preview) in your environment, you can choose to add it as a lead or a contact.

    :::image type="content" source="media/banner-add-contact.png" alt-text="Screenshot showing a banner message with a quick action for adding a new contact.":::

1. In the **New contact** or **New lead** form, add the required information, and then select **Save**.


### Related information

[Create a new record in your CRM from Copilot for Sales](create-new-record.md)<br>
[Configure new record creation](customize-forms-and-fields.md#configure-new-record-creation)
