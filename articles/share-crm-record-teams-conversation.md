---
title: Share a CRM record in Teams or Outlook
description: Learn how to share a CRM record in a Teams conversation or email using Copilot for Sales.
ms.date: 10/30/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Share a CRM record in Teams or Outlook

Copilot for Sales enables you to share a CRM record with your team members in a Teams chat or channel conversation, or in an email allowing them to view the record details in the flow of their work. The CRM record is shared as an adaptive card that is kept up to date based on the data in your CRM system.

In Teams, the adaptive card also displays the AI-generated summary of the record, enabling you to quickly catch up on the details of the record within the flow of your conversation. The AI-generated summary is displayed only if the Copilot features are enabled for your organization.  

You can share a CRM record using the Copilot for Sales search message extension, the /mention feature if your administrator has turned it on, or by pasting a link to the record in the chat or email. When you share a record, an adaptive card is created that displays the record details, such as the record name, owner, and key fields.

> [!NOTE]
>
> - For Outlook support, ensure that the [enhanced Teams app has been deployed](sales-copilot-faq.md#what-is-enhanced-teams-app).
> - If you're using Dynamics 365 as your CRM system, and you receive an adaptive card in an email or a Teams chat or channel, you can view data in the adaptive even if you aren't signed in to the Copilot for Sales app in Outlook or if you're signed in to a different Dynamics environment, as long as you have read access for the record and Copilot for Sales privileges.
> - If you're using Salesforce as your CRM system, and you receive an adaptive card in an email or a Teams chat or channel, you must be signed in to Salesforce in the Copilot for Sales app in Outlook to view data in the adaptive card while also having read access for the record and Copilot for Sales privileges.
> - Data in the adaptive card is refreshed from the CRM system every time you view the card in Teams chat or email, or when you manually refresh the card.

## Share a CRM record in Teams using search message extensions

1. Go to the conversation in which you want to share the CRM record. Select **More apps** (**...**), search for the **Copilot for Sales** app, and then select it. If the app is pinned to the action bar, select the **Copilot for Sales** icon under the message box.

   :::image type="content" source="media/viva-sales-icon.png" alt-text="Screenshot showing the Copilot for Sales icon under message box.":::

1. In the **Copilot for Sales** window, search for and select the record.

   > [!NOTE]
   >
   > - By default, the recently accessed records are displayed, without performing any search. You can either search for the record or select [Advanced search](#share-a-record-using-advanced-search) to search for a particular record type.
   >
   > - If you change the name of a record type in CRM, they aren't updated in Adaptive Card or messaging extensions in Teams. For example, if you rename Account to Customer, the name in Adaptive Card and messaging extensions is displayed as Account.

   :::image type="content" source="media/viva-sales.png" alt-text="Screenshot showing the Copilot for Sales window.":::

    The record card is added to the message box.

    :::image type="content" source="media/entity-summary-adaptive-card.png" alt-text="Screenshot showing the AI-generated record summary in adaptive card.":::

   > [!NOTE]
   > The fields on a record's card are displayed as configured by your CRM administrator.

1. Send the message to the chat.

If the recipients don't have the Copilot for Sales app installed in Teams, a message is displayed at the bottom of the card prior to sending the message. The message informs the recipients that they need to install the Copilot for Sales app to view the record details. Once the app is installed, the adaptive card is displayed with the record details if the recipients have access to the CRM record, otherwise, a link to the record is displayed in the card.

If the app is blocked by the admin, the message informs the recipients that they need to contact their admin to enable the app.

## Share a CRM record in Outlook using search message extensions

The experience of using the Copilot for Sales search message extension when composing an email is a bit different in classic Outlook desktop, new Outlook desktop, and Outlook on the web. 

> [!NOTE]
> If you're using Classic Outlook desktop, the capability to share a CRM record is supported only on [Current Channel](/microsoft-365-apps/updates/overview-update-channels#current-channel-overview).

### Classic Outlook desktop

1. On the ribbon, select **Copilot for Sales** or **All Apps** > **Copilot for Sales**.  
1. In the pop-up, select **Copilot for Sales**.  
    Alternatively, you can select [Advanced search](#share-a-record-using-advanced-search) to search for a particular record type.

    :::image type="content" source="media/search-outlook-classic.png" alt-text="Screenshot showing search option in the Copilot for Sales app in classic Outlook.":::

1. In the **Copilot for Sales** pane, select a record from the list of recently accessed records or search for and select the CRM record.

    :::image type="content" source="media/search-pane-outlook-classic.png" alt-text="Screenshot showing search pane for the Copilot for Sales app in classic Outlook.":::

    The adaptive card is added to the email.

    :::image type="content" source="media/viva-sales-contact-card.png" alt-text="Screenshot showing the Copilot for Sales contact card.":::

### New Outlook desktop and Outlook on the web

1. On the ribbon, select **Apps** > **Copilot for Sales**.  
1. In the pop-up, select **Search Copilot for Sales**.

    :::image type="content" source="media/search-outlook-new.png" alt-text="Screenshot showing search option in the Copilot for Sales app in new Outlook.":::

1. In the **Copilot for Sales** pop-up, select a record from the list of recently accessed records or search for and select the CRM record.

    :::image type="content" source="media/search-pane-outlook-new.png" alt-text="Screenshot showing search pop-up for the Copilot for Sales app in new Outlook.":::

    The adaptive card is added to the email.

## Share a CRM record in Outlook using /mention

Your administrator needs to [turn on this feature](share-crm-record-admin.md) before you can use it. 

1. In the body of the email or calendar invite, type a forward slash (/) symbol. Copilot for Sales displays a list of recently accessed records.

1. Select a record from the list or search for a record by entering the first few letters of the record name.

1. Select the record from the search results.

    :::image type="content" source="media/mentions-outlook-search.png" alt-text="Screenshot showing the Copilot for Sales search in Outlook.":::

    The adaptive card is added to the email.

    :::image type="content" source="media/mentions-outlook-adaptive-card.png" alt-text="Screenshot showing the adaptive card added in Outlook email.":::

## Share a record using advanced search

1. In the **Advanced search** window, enter or select the following values:  
    - **Search for a record to share**: Name of the record to share.  
    - **Filter by**: Record type to search for.

      > [!NOTE]
      > The **All** filter allows you to search for a record of any record type added to Copilot for Sales by your administrator. Other filters are specific to a record type and allow you to search for that record type.

      :::image type="content" source="media/advanced-search.png" alt-text="Screenshot showing the advanced search in Teams app.":::

1. From the results, preview a record by selecting the down arrow next to the record name. Select a record to share it as a card on the chat.

## Paste a link to a CRM record

1. [Copy the record link from the Copilot for Sales app in Outlook](share-link-crm-record.md).  
1. Paste the link in the chat or email.  
    The record card is added to the message box.

   :::image type="content" source="media/contact-card-link.png" alt-text="Screenshot showing the Copilot for Sales contact card link.":::

1. Send the message to the chat.

> [!NOTE]
> You must copy the record link from the Copilot for Sales add-in in Outlook. If you copy the record link from Salesforce, it doesn't unfurl to display the adaptive card. However, if you copy the record link from Dynamics 365, it unfurls to display the adaptive card.

### Related information

[Access the Copilot for Sales app](open-app.md)  
[Share a link to a CRM record](share-link-crm-record.md)
