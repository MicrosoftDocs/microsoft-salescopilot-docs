---
title: Connect a contact to your CRM 
description: Learn how to connect a contact to your CRM.
ms.date: 07/20/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Connect a contact to your CRM

You’ll get the most benefit from everything Sales Copilot can do for you when your external contacts are available in your CRM system. In Sales Copilot, we call this connecting a contact to your CRM. Contacts that are connected to your CRM are referred to as _Saved contacts_.

When you read an email from external contacts or compose an email to external contacts, and open the Sales Copilot pane, Sales Copilot searches your CRM for the contact’s primary email address. The external contact is connected to a CRM contact based on one of the following conditions:

- External email address matches only one CRM contact

- External email address matches none of the CRM contacts

- External email address matches multiple CRM contacts

## External email address matches only one CRM contact

If the address you entered in your email matches only one contact in the CRM, Sales Copilot automatically connects them. The connected contacts are displayed in the **Contacts** card on the **Dynamics 365** or **Salesforce** tab.

## External email address matches none of the CRM contacts

If the email address you entered doesn’t match any of the contacts in your CRM, select **Add contact** or **Add contacts** to [create a contact](create-contact-crm-sales-copilot.md) in your CRM.

## External email address matches multiple CRM contacts

If the email address you entered matches multiple contacts in the CRM, you must manually select and connect to the correct CRM contact. Sales Copilot displays a message on the **Highlights** card about multiple matches of a contact.

1. In the **Sales Copilot** pane, select **Choose contact** on the **Highlights** card.

    :::image type="content" source="media/choose-contact-highlights.png" alt-text="Screenshot showing to choose contact from the Highlights tab.":::

    Alternatively, you can select the **Dynamics 365** or **Salesforce** tab, select the contact in the **Contacts** card, and then select **Choose contact**.

    :::image type="content" source="media/choose-contact-crm.png" alt-text="Screenshot showing to choose contact from CRM tab.":::

2. Select the contact you want to connect to.

    :::image type="content" source="media/choose-correct-contact.png" alt-text="Screenshot showing to choose the correct contact.":::

    If none of the matches are correct, select **Create a new contact** to [create a contact](create-contact-crm-sales-copilot.md).
    
    If you've connected the external contact to an incorrect CRM contact, by mistake, you can [change the connected record](change-connected-crm-contact.md).