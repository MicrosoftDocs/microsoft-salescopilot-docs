---
title: Connect a contact to your CRM 
description: Learn how to connect a contact to your CRM.
ms.date: 04/27/2026
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom: sfi-image-nochange
---

# Connect a contact to your CRM

You'll get the most benefit from everything Sales agent can do for you when your external contacts are available in your CRM system. In Sales agent, we call this connecting a contact to your CRM. Contacts that are connected to your CRM are referred to as _Saved contacts_.

When you read an email from external contacts or compose an email to external contacts, and open the **Sales** pane, the Sales agent searches your CRM for the contact's primary email address. The external contact is connected to a CRM contact based on one of the following conditions:

- External email address matches only one CRM contact  
- External email address matches none of the CRM contacts  
- External email address matches multiple CRM contacts

> [!NOTE]
> The Sales agent matches external contacts against all email fields on the Contact record type (or Salesforce object), including custom email fields added by CRM administrators in the [Sales agent Forms settings](customize-forms-and-fields.md).

## External email address matches only one CRM contact

If the address you entered in your email matches only one contact in the CRM, the Sales agent automatically connects them. The connected contacts are displayed in the **Contacts** card.

## External email address matches none of the CRM contacts

If the email address you entered doesn't match any of the contacts in your CRM, [create a contact](create-contact-crm.md) in your CRM.

## External email address matches multiple CRM contacts

If the email address you entered matches multiple contacts in the CRM, you must manually select and connect to the correct CRM contact. The Sales agent displays a message on the **Highlights** card about multiple matches of a contact.

1. In the **Sales** pane, select the contact in the **Contacts** card, and then select **Choose contact**.

    :::image type="content" source="media/choose-contact-crm.png" alt-text="Screenshot showing to choose contact from CRM tab.":::

1. Select the contact you want to connect to.

    :::image type="content" source="media/choose-correct-contact.png" alt-text="Screenshot showing to choose the correct contact.":::

    - If none of the matches are correct, select **Create a new contact** to [create a contact](create-contact-crm.md).  
    - If you've connected the external contact to an incorrect CRM contact by mistake, you can [change the connected record](change-connected-crm-contact.md).

### Related information

[Create a contact in your CRM](create-contact-crm.md)
