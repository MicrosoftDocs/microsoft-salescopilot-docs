---
title: Create a contact in your CRM from Copilot for Sales
description: Learn how to create a contact in your CRM from Copilot for Sales.
ms.date: 03/18/2024
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

## Signature available in email

If you open the **Copilot for Sales** pane from an incoming email that contains the signature of the sender, and you add the contact to your CRM, Copilot for Sales prefills the contact details based on the signature and highlights the fields that it populated. You can update the information and select **Save**.

This capability is available only for emails in the [supported languages](supported-languages.md#ai-in-copilot-for-sales).

:::image type="content" source="media/pre-fill.png" alt-text="Screenshot showing prefilled details from signature.":::

### See also

[Create a new record in your CRM from Copilot for Sales](create-new-record.md)