---
title: Use Copilot for Sales app during a meeting
description: Learn how to use the Copilot for Sales app during a meeting.
ms.date: 07/25/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

<!-- Unsure about the wording in line 81, where it says "... select the links to see Bing search results or competitor in CRM system." Should it say "...select the links to see Bing search results or competitor information in your CRM system"? --> 


# Use Copilot for Sales app during a meeting

The Copilot for Sales app in Microsoft Teams helps you prepare for and conduct meetings with your sales contacts. You can view the meeting preparation card, view and edit the connected CRM record, and get real-time sales tips during the meeting. This helps you stay focused on the meeting and close deals faster.

## Get meeting preparation card

The meeting preparation card helps you get the latest information related to the meeting from CRM. This helps you stay informed and up to date.

**Prerequisites**: The following prerequisites must be met to view the meeting preparation card in Microsoft Teams:

- [Copilot AI features must be turned on in your environment](suggested-replies.md).
- [You must be connected to a CRM organization in the Copilot for Sales app](sign-in-crm-outlook.md).
- [At least one external contact that is saved in CRM must be invited to the meeting](connect-contact.md).


The meeting preparation card is displayed in your personal chat with the **Copilot for Sales** bot 45 to 75 minutes before the meeting starts. If the meeting is scheduled less than an hour before the start time, the card is triggered once the meeting invite is sent. This card helps you prepare for the meeting and get context about the attendees and the connected record. The content of the card is based on the connected opportunity. 

The meeting preparation card contains the following information when a meeting is connected to an opportunity in CRM. 

> [!NOTE]
> - If the meeting is not connected to an opportunity, the card displays general meeting information, meeting participants, and recent communication.
> - The meeting preparation card is not displayed for recurring meetings.

- **General meeting information**: Information about the meeting such as its name, date, time, connected account, and connected opportunity.
- **Meeting participants**: Information about the external participants and their role in the opportunity.
- **Recent communication**: Displays up to two most recent email and meeting communications with the external participants (must be a CRM contact) in the last three months. You can select an email to open it in the browser. You can also select a meeting to open its meeting recap in Teams. 
- **Opportunity info**: Summary of the key information about the related opportunity.
- **Notes from CRM**: Two recent notes from the opportunity timeline.
- **Open tasks**: Total number of open tasks and count of high-priority tasks.
- **Related records**: Number of related opportunities and number of related cases for the account.

:::image type="content" source="media/meeting-prep-card.png" alt-text="Screenshot showing meeting preparation card.":::

> [!NOTE]
> You must check the AI-generated content carefully because it can have mistakes. It's your responsibility to review the AI-generated content to make sure it's accurate and appropriate.

## Open the Copilot for Sales app

Select the **Copilot for Sales** icon on the meeting toolbar. The **Copilot for Sales** panel opens on the right side of the meeting window. If you don't see the Copilot for Sales icon, select **Apps** and then select **Copilot for Sales**.

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

An introduction card is displayed in the Copilot for Sales panel explaining how real-time sales tips work and the benefits they offer.

When you start recording the meeting, the real-time sales tips are displayed in the **Copilot for Sales** panel. When someone on the call mentions a brand or a competitor, a card is automatically shown with key information from Bing or your CRM to help you get context and respond quickly to inquiries. You must select **Get brand info** to view detailed information.

The brand information is based on a Bing knowledge graph. The competitor information is displayed from your CRM system, if it's available, and includes strengths and weaknesses of the competitor mentioned in the meeting. 

:::image type="content" source="media/real-time-tips.png" alt-text="Screenshot showing real-time sales tips in Microsoft Teams during a meeting.":::

To view data sources used in getting brand and competitor information, select **(n) references** at the bottom-left of the card, and then select the links to see Bing search results or competitor in CRM system.

:::image type="content" source="media/real-time-tips-ref.png" alt-text="Screenshot showing references for real-time-tips.":::


## View connected record details

With the Copilot for Sales app, you can view and edit the connected CRM record during the meeting in Teams. This helps you access and update the CRM record in the flow of your work.

> [!NOTE]
> You must [save and connect the meeting to a CRM record](save-outlook-activities-crm.md) to view details of the connected record.

1. [Open Copilot for Sales](#open-the-copilot-for-sales-app).

1. In the **Connected to** card, select the record to see its details in the **Copilot for Sales** panel.

You can also open a record in CRM to view its complete details. The record details open in a new tab. Perform either of the following actions to open a record in CRM:

- Hover over the record, select **More actions** (**...**), and then select **Open in (CRM)**.

- Select the record to see its details in the **Copilot for Sales** panel, select **More actions** (**...**), and then select **Open in (CRM)**.

### Copy link to connected record

You can copy a link to the connected record and then share it in a Teams chat or an email message. When you paste the record's link into a Teams chat, it will unfurl into a rich adaptive card. When you paste the record's link in an email message, a link to the record is pasted.

1. [Open Copilot for Sales](#open-the-copilot-for-sales-app).

1. Hover over the record and select **More actions** (**...**) > **Copy link**.

Alternatively, you can select the connected record to open its details, and then select **More actions** (**...**) > **Copy link**.

### Edit connected record

1. [Open the connected record details](#view-connected-record-details).

1. Select **More actions** (**...**) > **Edit record**.
