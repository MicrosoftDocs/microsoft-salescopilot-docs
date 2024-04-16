---
title: Create a contact in your CRM from Copilot for Sales
description: Learn how to create a contact in your CRM from Copilot for Sales.
ms.date: 04/15/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Create a contact in your CRM from Copilot for Sales

If an external contact doesn't exist in your CRM, create a contact in the CRM right from Copilot for Sales.

> [!TIP]
> Enter the contact's email address in the following format when you compose an email or meeting invitation: **FirstName LastName &lt;email address&gt;**. If you do, the corresponding items in the CRM contact form fill automatically.

To create a contact:

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

This capability is available only for emails in the [supported languages](supported-languages.md#ai-in-copilot-for-sales).

:::image type="content" source="media/pre-fill.png" alt-text="Screenshot showing prefilled details from signature.":::

## Add new contacts through quick CRM actions in email banners

When you read an email from external contacts and have at least one contact (in the email thread) that's not saved in CRM, the banner message at the top of the email enables you to add the new contacts through quick CRM actions.

1. Open an email with external contacts.
2. Select **Add contact** or **Add contacts**.
3. In the **Copilot for Sales** pane, hover over the unsaved contact, and then select **Add**.
4. In the **New contact** form, add the required information, and then select **Save**.

Currently, banner messages with quick CRM actions are available on up to two external emails per day. If you wish to disable these banners, [ask your admininstrator to disable them](m365-admin-setting.md).

### See also

[Create a new record in your CRM from Copilot for Sales](create-new-record.md)
