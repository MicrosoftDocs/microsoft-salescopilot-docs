---
title: Connect a contact to your CRM 
description: Learn how to connect a contact to your CRM.
ms.date: 06/26/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom: sfi-image-nochange
---

# Connect a contact to your CRM

You'll get the most benefit from everything Sales app can do for you when your external contacts are available in your CRM system. In Sales app, we call this connecting a contact to your CRM. Contacts that are connected to your CRM are referred to as _Saved contacts_.

When you read an email from external contacts or compose an email to external contacts, and open the Sales app pane, Sales app searches your CRM for the contact's primary email address. The external contact is connected to a CRM contact based on one of the following conditions:

- External email address matches only one CRM contact  
- External email address matches none of the CRM contacts  
- External email address matches multiple CRM contacts

> [!NOTE]
> If you're using Dynamics 365 as your CRM, Sales app matches the email address of the external contact only with the EmailAddress1 field of the contact record in Dynamics 365 and not with EmailAddress2 or EmailAddress3 field. Ensure that email address is populated in the EmailAddress1 field to connect the external contact to the CRM contact. If the email address is populated in the EmailAddress2 or EmailAddress3 field, Sales app won't match the external contact with the CRM contact and considers it as an unsaved contact.

## External email address matches only one CRM contact

If the address you entered in your email matches only one contact in the CRM, Sales app automatically connects them. The connected contacts are displayed in the **Contacts** card.

## External email address matches none of the CRM contacts

If the email address you entered doesn't match any of the contacts in your CRM, [create a contact](create-contact-crm-sales-copilot.md) in your CRM.

## External email address matches multiple CRM contacts

If the email address you entered matches multiple contacts in the CRM, you must manually select and connect to the correct CRM contact. Sales app displays a message on the **Highlights** card about multiple matches of a contact.

1. In the **Sales** pane, select the contact in the **Contacts** card, and then select **Choose contact**.

    :::image type="content" source="media/choose-contact-crm.png" alt-text="Screenshot showing to choose contact from CRM tab.":::

1. Select the contact you want to connect to.

    :::image type="content" source="media/choose-correct-contact.png" alt-text="Screenshot showing to choose the correct contact.":::

    - If none of the matches are correct, select **Create a new contact** to [create a contact](create-contact-crm-sales-copilot.md).  
    - If you've connected the external contact to an incorrect CRM contact by mistake, you can [change the connected record](change-connected-crm-contact.md).

### Related information

[Create a contact in your CRM](create-contact-crm-sales-copilot.md)
