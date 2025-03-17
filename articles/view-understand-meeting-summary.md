---
title: View and understand the meeting summary
description: Learn how to view and understand the meeting summary.
ms.date: 02/11/2025
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# View and understand the meeting summary

Sellers and their managers need an easy way to review the conversations they have with their customers and quickly find relevant talking points, keywords, and insights. The meeting summary page in Copilot for Sales provides a high-level view of a customer conversation, including follow-up action items, relevant keywords, a timeline, a transcript of the call, and other useful information.

## License requirements

The experience covered within this article is only displayed to Dynamics 365 Sales customers who are accessing the [included capabilities available with their existing Sales Copilot license](features-d365-users.md). Organizations that have purchased Copilot for Sales will see the fully integrated experience within Teams meeting recap. For more information, see [View sales related insights in Microsoft Teams meeting recap](view-meeting-summary-recap.md).

## View the meeting summary

When the meeting summary is ready, you'll receive a message from the **Copilot for Sales** bot in your personal chat. The message includes meeting details such as the title, date, time, and attendees, and a link to the summary. You can use the link in the message to view the summary or go to the **Copilot for Sales** tab in the meeting.

- Go to the **Copilot for Sales** bot in your chat list and select **Open recap**. The notification provides a summary of the meeting and follow-up action items.    

  :::image type="content" source="media/meeting-summary.png" alt-text="Screenshot showing the Copilot for Sales meeting summary card.":::

- Go to the meeting chat in your chat list, or open the event on your calendar in Teams, and select the **Copilot for Sales** tab.

If there are multiple recordings of a single meeting (happens when you stop and restart the recording), or recordings of a recurring meeting, you can view the meeting summary of an individual meeting by selecting the date from the drop-down list in the meeting summary.

:::image type="content" source="media/recurring.png" alt-text="Screenshot showing the Copilot for Sales meeting summary for a recurring meeting.":::

## Understand the meeting summary

The meeting summary page includes the following sections:

- Recap, mentions, and details

- Call transcript and translation

- Call playback timeline and segmentation

### Recap

The **Recap** tab displays call highlights and follow-up action items that Copilot for Sales identified during the call.

> [!NOTE]
> Call highlights and follow-ups won't be generated if the meeting recording duration exceeds 70 minutes. In North Ameraica and Europe regions, the supported meeting recording duration is 100 minutes.

:::image type="content" source="media/recap-tab.png" alt-text="Screenshot of the Recap tab in the Copilot for Sales meeting summary.":::

To share the call highlights and follow-up action items, select **Copy to clipboard**, and then paste the data into an email, Teams chat, or any other medium you like. The summary appears in the following format:

- **Meeting title**: Displays the title of the meeting.

- **Participants**: Lists the people who participated in the meeting.

- **Meeting date and time**: Displays the date and time of the meeting.

- **Highlights**: Summarizes each section of the conversation in the form of a bulleted list.

- **Follow-ups**: Displays a bulleted list of action items, from which you can create tasks in your customer relationship management (CRM) system. [Learn how to turn meeting summary action items into CRM tasks](#create-crm-tasks-from-meeting-summary)

:::image type="content" source="media/recap.png" alt-text="Screenshot of a Copilot for Sales meeting summary pasted in an email.":::

### Mentions

The **Mentions** tab displays keywords, stakeholders, products, and competitors that were mentioned during the call. When you select a word in the following sections, the transcript indicates at what point it was mentioned.

- **People**: Displays the names of people mentioned during the call; for example, Sarah calling from Contoso.

- **Products**: Displays the names of the products mentioned during the call; for example, "I only know how to use a Fabrikam LED TV".

- **Keywords**: Displays keywords that can be used as best practices during the call.

- **Other brands and organizations**: Displays brand and organization names (other than your own) that the customer mentioned during the call.

- **Questions asked by sellers**: Displays questions the seller asked during the call; for example, "What do you think about the demo?"

- **Questions asked by others**: Displays questions other participants asked during the call.

- **Times**: Displays the time periods mentioned during the call.

### Details

The **Details** tab displays the names of the people who participated in the meeting.

:::image type="content" source="media/details-tab.png" alt-text="Screenshot of the Details tab in the Copilot for Sales meeting summary.":::

### Call transcript and translation

The **Transcript** section displays a written record of the call that you can read and translate, along with a timeline of the call.

If the transcript is in a language other than English, and it's a supported language, select **Translate** to read the transcript in English.

### Call playback, timeline, and segmentation

If you're the meeting organizer or the person who recorded the call, you can use the call playback feature to listen to the recorded call. You can listen to the entire call or drag the progress bar to skip to specific points on the timeline. The call transcript automatically scrolls to the point you select. You can also pause, rewind, and move forward through the call and adjust the playback volume.

The timeline displays the sentiments (positive, neutral, or negative) detected in the conversation. You can drag the progress bar to a specific point on the timeline. The call transcript automatically scrolls to the point you select.

When you select a word on the **Mentions** tab, a diamond icon on the playback timeline indicates the point at which the word was mentioned. If you hover over a word on the **Mentions** tab, gray diamond icons on the timeline indicate all the points at which the word was mentioned.

To quickly go to a comment in the transcript, select its icon on the timeline.

The timeline also indicates the conversation segments, such as introduction, solution, price quote, and call close. Select a segment to view insights that are relevant to it. The transcript scrolls to the start of the segment, and the segment is highlighted on the timeline. If the selected segment contains any action items or keywords, they're displayed on their respective tabs.

:::image type="content" source="media/playback.png" alt-text="Screenshot of the timeline playback in the Copilot for Sales meeting summary.":::

## Create CRM tasks from meeting summary

You can convert the suggested action items in a meeting summary to a task and save it in CRM directly from Teams.

1. [Open a meeting summary](view-understand-meeting-summary.md) and go to the **Recap** tab.

1. Find the follow-up item for which you need to create a task, and then select **Create task**.

   :::image type="content" source="media/create-task.png" alt-text="Screenshot showing the Create task link.":::

1. Add or update the following information:

   | Item | Description | Required |
   |------|-------------|----------|
   | Subject | Name of the task | Yes |
   | Owner | Who will complete the task; if it isn't you, you can assign someone else | Yes |
   | Connected to | A record that provides information about the task; select from accounts and opportunities that are associated with the email's recipients | No |
   | Due date | The date by which the owner should complete the task | No |
   | Description | Text snippet of the follow-up item; you can change it if needed. <br><br> **Note**: A link to the meeting is populated automatically in this field. | No |

   :::image type="content" source="media/create-crm.png" alt-text="Screenshot showing the Create CRM task in Dynamics 365.":::

1. Select **Create**.

    After you've created a task, **Create task** changes to **Open task**. Select **Open task** to open the task in your CRM.

   :::image type="content" source="media/open-task.png" alt-text="Screenshot showing the Open task link.":::