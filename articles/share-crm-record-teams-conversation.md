---
title: Share a CRM record in a Teams conversation
description: Learn how to share a CRM record in a Teams conversation.
ms.date: 12/11/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Share a CRM record in a Teams conversation

Copilot for Sales does even more than offer rich insights after a Teams meeting with customers. You can also use it to share a customer's record in a Teams chat or channel as an adaptive card.

With the Copilot for Sales app, you can:

- Search for a record to share

- Paste a link to a record that will unfurl into a rich adaptive card

## Search for a CRM record to share

1. Go to the conversation in which you want to share the contact. Select the **Copilot for Sales** icon under the message box.

   :::image type="content" source="media/viva-sales-icon.png" alt-text="Screenshot showing the Copilot for Sales icon under message box.":::

    If the Copilot for Sales icon isn't there, select **Messaging extensions** (**...**), search for the **Copilot for Sales** app, and then select it.

1. In the **Copilot for Sales** window, search for and select the record.

   > [!NOTE]
   >
   > - By default, the recently accessed records are displayed, without performing any search. You can either search for the record or use [advanced search](#share-a-record-using-advanced-search) to search for a particular record type.
   >
   > - If you change the name of a record type in CRM, they are not updated in Adaptive Card or messaging extensions in Teams. For example, if you rename Account to Customer, the name in Adaptive Card and messaging extensions will show as Account.

   :::image type="content" source="media/viva-sales.png" alt-text="Screenshot showing the Copilot for Sales window.":::

    The record card is added to the message box.

   :::image type="content" source="media/viva-sales-contact-card.png" alt-text="Screenshot showing the Copilot for Sales contact card.":::

   > [!NOTE]
   > The fields on a record's card are displayed as configured by your CRM administrator.

1. Send the message to the chat.

### Share a record using advanced search

1. Go to the conversation in which you want to share the contact. Select the **Copilot for Sales** icon under the message box.

    If the Copilot for Sales icon isn't there, select **Messaging extensions** (**...**), search for the **Copilot for Sales** app, and then select it.

1. In the **Copilot for Sales** window, select **Advanced search** in the upper-right corner.

1. In the **Advanced search** window, enter or select the following values:

    - **Search for a record to share**: Name of the record to share.

    - **Filter by**: Record type to search for.

      > [!NOTE]
      > The **All** filter allows you to search for a record of any record type added to Copilot for Sales by your administrator. Other filters are specific to a record type and allow you to search for that record type.

      :::image type="content" source="media/advanced-search.png" alt-text="Screenshot showing the advanced search in Teams app.":::

1. From the results, preview a record by selecting the down arrow next to the record name. Select a record to share it as a card on the chat.

## Paste a link to a CRM record

1. [Copy the record link from the Copilot for Sales app in Outlook](share-link-crm-record.md).

1. Go to the conversation in which you want to share the record. Paste the link.

    The record card is added to the message box.

   :::image type="content" source="media/contact-card-link.png" alt-text="Screenshot showing the Copilot for Sales contact card link.":::

1. Send the message to the chat.

> [!NOTE]
> You must copy the record link from the Copilot for Sales add-in in Outlook. If you copy the record link from the CRM system, it doesn't add the Copilot for Sales record card.
