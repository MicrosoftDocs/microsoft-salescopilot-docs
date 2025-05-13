---
title: View a meeting preparation card
description: Learn how to view a meeting preparation card in Teams.
ms.date: 05/14/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Meeting preparation card

The meeting preparation card gives you the latest information related to the meeting from CRM. This card helps you stay informed and up to date. It shows information about the meeting, participants, recent communication, opportunity info, notes from CRM, open tasks, and related records. You can use this information to prepare for the meeting and have a productive discussion.

Here's the video that shows a meeting preparation card in Teams and [how to view sales insights using Teams meeting recap](view-meeting-summary-recap.md):

> [!VIDEO 159e3203-7996-4193-9037-e45cf0744dbf]

## Prerequisites

- [Turn on Copilot AI features in your environment](suggested-replies.md).
- [Connect to a CRM organization in the Copilot for Sales app](sign-in-crm-outlook.md).
- [Invite at least one external contact that is saved in CRM to the meeting](connect-contact.md).

## View a meeting preparation card

The meeting preparation card is displayed in your personal chat with the **Copilot for Sales** bot in Teams. The meeting preparation card is sent at a time that is [configured by your administrator](configure-meeting-agent.md#configure-pre-meeting-preparation-notifications). By default, the meeting preparation card is sent one hour before the meeting. If you schedule the meeting less than an hour before the start time, the card appears when you send the meeting invite. 

This card helps you prepare for the meeting and get context about the attendees and the connected record. The content of the card is based on the connected opportunity.

> [!NOTE]
> - If the meeting isn't connected to an opportunity, the card shows general meeting information, meeting participants, and recent communication.
> - The meeting preparation card doesn't appear for recurring meetings.

The meeting preparation card contains the following information when a meeting is connected to an opportunity in CRM: 

- **General meeting information**: Information about the meeting such as its name, date, time, connected account, and connected opportunity.
- **Meeting participants**: Information about the external participants and their role in the opportunity.
- **Recent communication**: Displays up to two most recent email and meeting communications with the external participants (must be a CRM contact) in the last three months. You can select an email to open it in the browser. You can also select a meeting to open its meeting recap in Teams. 
- **Opportunity info**: A summary of the key information about the related opportunity.
- **Notes from CRM**: Two recent notes from the opportunity timeline.
- **Open tasks**: The total number of open tasks and count of high-priority tasks.
- **Related records**: The number of related opportunities and number of related cases for the account.

:::image type="content" source="media/meeting-prep-card.png" alt-text="Screenshot showing meeting preparation card.":::

> [!NOTE]
> You must check the AI-generated content carefully because it can have mistakes. It's your responsibility to review the AI-generated content to make sure it's accurate and appropriate.

