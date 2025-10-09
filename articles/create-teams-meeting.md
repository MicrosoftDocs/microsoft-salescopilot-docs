---
title: Create a Teams meeting and generate meeting insights
description: Learn how to create a Teams meeting and generate meeting insights using Sales app.
ms.date: 06/30/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Create a Teams meeting and generate meeting insights

Scheduling and managing Microsoft Teams meetings effectively is essential for leveraging the full potential of the Sales app. This article walks you through the steps to create a Teams meeting, ensure the Sales app is added, and generate insightful meeting summaries.

## Create a Teams meeting

Your journey starts when you schedule a Microsoft Teams meeting and invite at least one external participant. The Sales app is added automatically to the meeting. If the app is not added automatically, you can manually add it to the meeting.

### Add the Sales app automatically to a Teams meeting

The Sales app is added automatically to a Teams meeting when the following conditions are met:

- You must invite at least one external participant to the meeting.  
- You must transcribe the meeting for Sales app to generate insights.  

If you create a recurring meeting, the Sales app is added to all occurrences of the meeting if the above conditions are met.

> [!NOTE]
> If your administrator has enabled the [auto recording capability](configure-meeting-agent.md#enable-or-disable-auto-recording-for-sales-meetings), the meeting is recorded automatically when the Sales app is added to the meeting.

## Add the Sales app manually to a Teams meeting

If the Sales app is not added automatically to a Teams meeting, a meeting organizer can manually add the app to the meeting. The app is visible only to the participants who are in the same tenant as the meeting organizer.  
Once the app is added to a recurring meeting, it's added to all occurrences of the meeting.  
For steps to manually add the Sales app to a Teams meeting, see [How can I add the Sales app manually to a Teams meeting?](sales-copilot-faq.md#how-can-i-add-the-copilot-for-sales-app-manually-to-a-teams-meeting)

> [!NOTE]
> If you try to add the app without signing in to the app from Outlook, a message is displayed to sign in to the app from Outlook. You must sign in to the app from Outlook and then select **Refresh** in the message to add the app to the meeting.

## Generate a meeting summary

When Sales app is added to a Teams meeting, it generates a meeting summary automatically if the meeting is recorded with transcription on.

1. [Join the meeting](https://support.microsoft.com/office/join-a-meeting-in-teams-1613bb53-f3fa-431e-85a9-d6a91e3468c9) with your customer. You can use the link in the Outlook calendar event or join from Teams.

1. [Start the recording and transcription](https://support.microsoft.com/office/record-a-meeting-in-teams-34dfbe7f-b07d-4a27-b4c6-de62f1348c24).

When you start recording the meeting, [live transcription](https://support.microsoft.com/office/view-live-transcription-in-a-teams-meeting-dc1a8f23-2e20-4684-885e-2152e06a4a8b) also starts if your Teams admin has [allowed transcription](/microsoftteams/cloud-recording#turn-on-or-turn-off-recording-transcription). If the recording starts but transcription doesn't, ask your admin to turn on recording transcription.

Transcription helps to make your meeting productive and inclusive for participants. By default, the transcript is available in English. You can change the transcript language to be the same as the language being spoken in the meeting. For details, see the **Change the transcript language** section in [View live transcription in a Teams meeting](https://support.microsoft.com/office/view-live-transcription-in-a-teams-meeting-dc1a8f23-2e20-4684-885e-2152e06a4a8b).

> [!NOTE]
> The spoken language is not detected automatically. If the transcript language is not same as the language spoken in the meeting, the generated transcript will be unusable.

When you end the meeting, Sales app uses the recorded call and transcript to generate and summarize rich meeting insights. The meeting summary provides an overview of how the conversation went. It includes action items and relevant keywords, a breakdown of customer sentiments during the call, and more. For information about how to view the meeting summary, see [View sales related insights in Microsoft Teams meeting recap](view-meeting-summary-recap.md).

> [!IMPORTANT]
>
> - You must transcribe the meeting to generate meeting insights.  
> - Version of the Sales app in Microsoft Teams must be 1.0.9 or higher to generate meeting insights. For more information, click [here](sales-copilot-faq.md#why-are-meeting-insights-not-getting-generated-even-if-meeting-is-transcribed).

Use the meeting summary to review past conversations with customers, understand historical needs and sentiments, and highlight your commitments.

Only you and any other sellers you invited to the meeting can view the meeting summary. It isn't visible to the customers who participated in the call.