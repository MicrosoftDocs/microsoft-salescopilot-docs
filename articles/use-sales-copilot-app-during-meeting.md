---
title: Use Copilot for Sales app during a meeting
description: Learn how to use the Copilot for Sales app during a meeting.
ms.date: 04/15/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Use Copilot for Sales app during a meeting

With the Copilot for Sales app, you can view and edit the connected CRM record during the meeting in Teams. This helps you access and update the CRM record in the flow of your work.

> [!NOTE]
> You must [save and connect the meeting to a CRM record](save-outlook-activities-crm.md) to view details of the connected record.

## Open the Copilot for Sales app

Select the **Copilot for Sales** icon on the meeting toolbar. The **Copilot for Sales** panel opens on the right side of the meeting window. If you don't see the Copilot for Sales icon, select **Apps**, and then select **Copilot for Sales**.

> [!NOTE]
> You must invite at least one connected contact for Outlook to add the Copilot for Sales app to the meeting.

If the meeting is connected to an opportunity in CRM, an [opportunity summary](view-opportunity-summary.md) card is displayed showing the key details and status of the current opportunity.

The connected record is displayed in the **Connected to** card. If the meeting is not connected and saved to CRM, a message is displayed to save and connect the meeting to a CRM record. For details about saving a meeting to CRM, see [Save Outlook activities to your CRM](save-outlook-activities-crm.md).

## View real-time sales tips

As a seller, you can get real-time sales tips during your meetings with sales contacts in the Copilot for Sales panel in Microsoft Teams. These tips provide information about competitors or brands mentioned in the meeting, and help you respond to inquiries. The information you need is right in front of you, and this leads to better communication and helps you close deals faster.

> [!NOTE]
> - You must transcribe the meeting to get real-time sales tips.
> - You must check the content carefully. AI-generated summaries may be missing information and can contain inaccurate details.

To view real-time sales tips during a meeting, [open the Copilot for Sales app](#open-the-copilot-for-sales-app).

If you don't start transcribing the meeting, you'll see a banner that encourages you to record the meeting to get real-time sales tips.

An introduction card is displayed in the Copilot for Sales panel explaining how real-time sales tips work and the benefits it offers.

When you start recording the meeting, the real-time sales tips are displayed in the **Copilot for Sales** panel. When someone on the call mentions a brand or a competitor, a card is automatically shown with key information from Bing or your CRM to help you get context and respond quickly to inquiries. You must select **Get brand info** to view detailed information.

The brand information is based on Bing knowledge graph. The competitor information is displayed from your CRM system, if it's available, and includes strengths and weaknesses of the competitor mentioned in the meeting. 

:::image type="content" source="media/real-time-tips.png" alt-text="Screenshot showing real-time sales tips in Microsoft Teams during a meeting.":::

To view data sources used in getting brand and competitor information, select **(n) references** at the bottom-left of the card, and then select the links to see Bing search results or competitor in CRM system.

:::image type="content" source="media/real-time-tips-ref.png" alt-text="Screenshot showing references for real-time-tips.":::


## View connected record details

1. [Open the Copilot for Sales app](#open-the-copilot-for-sales-app).

1. In the **Connected to** card, select the record to see its details in the **Copilot for Sales** panel.

You can also open a record in CRM to view its complete details. The record details open in a new tab. Perform either of the following actions to open a record in CRM:

- Hover over the record, select **More actions** (**...**), and then select **Open in (CRM)**.

- Select the record to see its details in the **Copilot for Sales** panel, select **More actions** (**...**), and then select **Open in (CRM)**.


## Copy link to connected record

You can copy a link to the connected record and then share it in a Teams chat or an email message. When you paste the record's link into Teams chat, it will unfurl into a rich adaptive card. When you paste the record's link in an email message, a link to the record is pasted.

1. [Open the Copilot for Sales app](#open-the-copilot-for-sales-app).

1. Hover over the record and select **More actions** (**...**) > **Copy link**.

Alternatively, you can select the connected record to open its details, and then select **More actions** (**...**) > **Copy link**.

## Edit connected record

1. [Open the connected record details](#view-connected-record-details).

1. Select **More actions** (**...**) > **Edit record**.
