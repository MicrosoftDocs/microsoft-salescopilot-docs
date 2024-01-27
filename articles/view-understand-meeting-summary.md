---
title: View and understand the meeting summary
description: Learn how to view and understand the meeting summary.
ms.date: 01/09/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# View and understand the meeting summary

Sellers and their managers need an easy way to review the conversations they've had with their customers and quickly find relevant talking points, keywords, and insights.

The meeting summary page provides a high-level view of how the conversation with a customer went, and includes follow-up action items and relevant keywords, a timeline, a transcript of the call, and more.

## License requirements

Capabilities mentioned in this article are available only to users with the Copilot for Sales standard license. If you have the Copilot for Sales premium license, see [View sales related insights in Microsoft Teams meeting recap](view-meeting-summary-recap.md).

## View the meeting summary

When the meeting summary is ready, you'll receive a message from the **Copilot for Sales** bot in your personal chat. The message includes meeting details such as the title, date, time, and attendees, and a link to the summary. You can use the link in the message to view the summary or go to the **Copilot for Sales** tab in the meeting.

- Go to the **Copilot for Sales** bot in your chat list and select **Open summary**.

  :::image type="content" source="media/meeting-summary.png" alt-text="Screenshot showing the Copilot for Sales meeting summary card.":::

- Go to the meeting chat in your chat list, or open the event on your calendar in Teams, and select the **Copilot for Sales** tab.

If there are multiple recordings of a single meeting (happens when you stop and restart the recording), or recordings of a recurring meeting, you can view the meeting summary of an individual meeting by selecting the date from the drop-down list in the meeting summary.

:::image type="content" source="media/recurring.png" alt-text="Screenshot showing the Copilot for Sales meeting summary for a recurring meeting.":::

## Understand the meeting summary

The meeting summary page includes the following sections:

- Recap, mentions, and Details

- Call transcript and translation

- Call playback timeline and segmentation

### Recap

The **Recap** tab displays call highlights and follow-up action items that Copilot for Sales identified during the call.

> [!NOTE]
> Call highlights won't be generated if the meeting recording duration exceeds 70 minutes.

:::image type="content" source="media/recap-tab.png" alt-text="Screenshot showing the Recap tab in Copilot for Sales meeting summary.":::

To share the call highlights and follow-up action items, select **Copy to clipboard**, and then paste the data into an email, Teams chat, or any other medium you like. The summary appears in the following format:

- **Meeting title**: Displays the title of the meeting

- **Participants**: Lists the people who participated in the meeting

- **Meeting date and time**: Displays the date and time of the meeting

- **Highlights**: Displays sentences in a bulleted list that summarize each section of the conversation

- **Follow-ups**: Displays action items in a bulleted list

:::image type="content" source="media/recap.png" alt-text="Screenshot showing how to copy and paste content from Recap tab in Copilot for Sales meeting summary.":::

You can create CRM tasks from the follow-up action items. More information: [Create CRM tasks from meeting summary](create-crm-tasks-meeting-summary.md)

### Mentions

The **Mentions** tab displays keywords, stakeholders, products, and competitors that were mentioned during the call. When you select a word in the following sections, the transcript indicates at what point it was mentioned.

- **People**: Displays the names of people mentioned during the call; for example, Sarah calling from Contoso.

- **Products**: Displays the names of the products mentioned during the call; for example, "I only know how to use a Fabrikam LED TV".

- **Keywords**: Displays keywords that can be used as best practices during the call. If topics are identified in the transcript, they are displayed first and then rest of the keywords are displayed. More information: [View Viva Topics in meeting summary](#view-viva-topics-in-meeting-summary-preview)

- **Other brands and organizations**: Displays brand and organization names (other than your own) that the customer mentioned during the call.

- **Questions asked by sellers**: Displays questions asked by sellers on the call. For example, What do you think about the demo?

- **Questions asked by others**: Displays questions asked by the other participants during the call.

- **Times**: Displays the time periods mentioned during the call.

#### View Viva Topics in meeting summary (preview)

[!INCLUDE [preview-banner-section](includes/preview-banner-section.md)]

**Prerequisites**: 

- The Viva Topics integration must be [enabled by your administrator](use-extensions.md#integrate-with-viva-topics). 
- You must have a license for Viva Topics.

Viva Topics helps you access information when you need it so you can be more productive and work smarter. It uses AI to automatically search for and identify topics in your organization. It compiles information about them, such as a short description, people working on the topic, and sites, files, and pages that are related to it. For more information about Viva Topics, go to [Understanding Viva Topics](https://support.microsoft.com/office/understanding-viva-topics-5bef3020-2679-4045-81cb-bcbc37218332).

Topics are scanned from the meeting transcript, and displayed along with other keywords. If a keyword with a category such as brand, people, or times was found, it is displayed under that category. Keywords that are also topics are indicated with the # symbol. Topics and their contents are not stored in Dataverse.

To view details of a topic, hover over the keyword to open its card. By default, it is opened in its default view. To open the extended view, select **More** under topic description.



### Details

The **Details** tab displays the names of the people who participated in the meeting.

:::image type="content" source="media/details-tab.png" alt-text="Screenshot showing the Details tab in Copilot for Sales meeting summary.":::

### Call transcript and translation

The **Transcript** section displays a written record of the call that you can read and translate, along with a timeline of the call.

If the transcript is in a language other than English, and it's a supported language, select **Translate** to read the transcript in English.

### Call playback, timeline, and segmentation

Use the call playback feature to listen to the recorded call. You can listen to the entire call or drag the progress bar to skip to specific points on the timeline. The call transcript automatically scrolls to the point you select. You can also pause, rewind, and move forward through the call, and adjust the playback volume.

The timeline displays the sentiments detected in the conversation: positive, neutral, or negative. You can drag the progress bar to a specific point on the timeline. The call transcript automatically scrolls to the point you select.

When you select a word on the **Mentions** tab, a diamond icon on the playback timeline indicates the point at which the word was mentioned. If you hover over a word on the **Mentions** tab, gray diamond icons on the timeline indicate all the points at which the word was mentioned.

To quickly go to a comment in the transcript, select its icon on the timeline.

The timeline also indicates the conversation segments, such as introduction, solution, price quote, and call close. Select a segment to view insights that are relevant to it. The transcript scrolls to the start of the segment, and the segment is highlighted on the timeline. If the selected segment contains any action items or keywords, they're displayed on their respective tabs.

> [!NOTE]
> The playback capability is available only to the meeting organizer and call recorder.

:::image type="content" source="media/playback.png" alt-text="Screenshot showing the timeline playback in Copilot for Sales meeting summary.":::
