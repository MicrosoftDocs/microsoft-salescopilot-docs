---
title: View sales insights in Microsoft Teams meeting recap
description: Discover how to use the Sales app in Teams to get sales insights in Teams meeting recaps. 
ms.date: 12/02/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:01/25/2024
---

# View sales insights in Microsoft Teams meeting recap

Sales includes all the capabilities within Microsoft 365 Copilot to provide users with valuable insights to help you support customer engagements. The combined Copilot experience in products like Microsoft Teams combines the power of Copilot in Teams and Sales, offering seamless, role-specific capabilities for improved collaboration. The experience provides summarized meeting insights, and generated meeting recaps to enable sellers to grow customer relationships and close deals.

## Prerequisites

- [Turn on Copilot AI features in your environment](suggested-replies.md).
- Add the Sales app to the meeting either [manually](create-teams-meeting.md#add-the-sales-app-manually-to-a-teams-meeting) or [automatically](create-teams-meeting.md#add-the-sales-app-automatically-to-a-teams-meeting).
- Transcribe the meeting. It's required to generate sales insights.
- Ensure that the meeting is not recurring.
- Ensure that the meeting is not created in Dynamics 365 Sales.

## Supported languages

To see a list of supported languages, go to [supported languages](introduction.md#supported-languages-and-geographies).

## View sales related insights in meeting recap

You can view a meeting recap if you record and transcribe a meeting. With the Sales app added to the Teams meeting, you can view sales related insights in the meeting recap.

To view sales related insights, [open the meeting recap in Teams](https://support.microsoft.com/office/meeting-recap-in-microsoft-teams-c2e3a0fe-504f-4b2c-bf85-504938f110ef), select the down-arrow next to **Transcript**, and then select **Sales**.

The following information is available:

- **Post-meeting actions**: View a list of suggested post-meeting actions such as [creating a summary email for meeting participants](#create-a-post-meeting-summary-email) and [saving AI-generated meeting notes to CRM](#save-ai-generated-meeting-notes-to-crm). This section is not available if you are viewing the meeting recap using the older Sales Copilot license.
- **Suggested follow-ups from the meeting**: View a list of follow-up tasks that are created during the meeting. You can also [create a task in CRM](#create-a-crm-task-from-a-meeting-recap) by selecting **Create task**.
- **Questions**: See questions that were asked during the meeting. It helps you to identify if your sellers are asking the right questions to understand customer needs. Questions are grouped by the person who asked them. When you select a question, the video jumps to the point in the conversation where the question was asked.
- **Keywords mentioned**: View keywords that were mentioned during the meeting. Keywords are grouped as per the following categories:
    - **Brands**: Names of brands that were mentioned during the meeting.
    - **Times**: Time mentioned during the meeting.
    - **People**: Names of people mentioned during the meeting.
    - **Others**: Other keywords mentioned during the meeting.
    
    If you track keywords and competitors in your CRM, they also appear in this section.
- **Key highlights**: View topics discussed during the meeting, including time stamps for each topic and speaker names. The summary is generated using AI and is based on the meeting recording and transcript. It helps you to quickly understand the main topics discussed during the meeting. This section is available only if you are viewing the meeting recap using the older Sales Copilot license.
- **Overall meeting sentiment**: View the overall sentiment of the meeting, which is calculated based on the tone of the conversation. The sentiment is categorized as positive, negative, or neutral. It also shows the trend of the sentiment over time, which helps you to understand how speakers felt during each phase of the meeting. [Learn more about accuracy of sentiment analysis](#accuracy-of-sentiment-analysis).
- **Speaker-level insights**: View insights for each speaker, including their talk time, sentiment distribution, and summary. This helps you to understand how each speaker contributed to the meeting and how they felt during the conversation.

:::image type="content" source="media/sales-insights-recap.png" alt-text="Screenshot showing sales insights in Teams meeting recap.":::

### When sales insights aren't generated

Sales insights aren't generated in the following scenarios:
- The meeting is recurring.
- The meeting was not transcribed.
- The meeting was created in Dynamics 365 Sales.
- The meeting recording was started and stopped multiple times.
- You are not connected to your CRM in the Sales app.
- If the meeting organizer has not provided access to the meeting recording and transcription to everyone.

### Accuracy of sentiment analysis

The sentiment analysis is AI-generated and based on the content and tone of the meeting transcript. While it can provide a helpful high-level view of customer tone and engagement, it's not always perfectly accurate and may misinterpret nuance, sarcasm, or context.

This feature is intended to help you quickly gauge the general sentiment of a meeting—for example, whether the conversation was mostly positive, neutral, or negative—but it should not be used as a definitive assessment of individual participants' intent or satisfaction.

It is strongly recommended that you verify insights using your own judgment and follow up directly with customers as needed. Sentiment insights are best used as a supporting tool, not a replacement for human evaluation.

## Create a CRM task from a meeting recap

1.	[Open a meeting recap in Teams and view sales related insights](#view-sales-related-insights-in-meeting-recap).

1.	Find the follow-up item for which you need to create a task, and then select **Create task**.

1.	Add or update the following information:

    | Item | Description | Required |
    | --- | --- | --- |
    | Subject | Name of the task. | Yes |
    | Owner | Who will complete the task; if it isn't you, you can assign someone else. | Yes |
    | Connected to | A record that provides information about the task; select from accounts and opportunities that are associated with the email's recipients. | No |
    | Due date | The date by which the owner should complete the task. | No |
    | Description | Text snippet of the follow-up item; you can change it if needed. <br> **Note**: A link to the meeting is populated automatically in this field. | No |

    :::image type="content" source="media/create-crm.png" alt-text="Screenshot showing create a task in CRM form.":::

1.	Select **Create**.

    After you create a task, **Create task** changes to **Open task**. Select **Open task** to open the task in your CRM.

## Create a post-meeting summary email

After meeting with your customers, you often send an email with a summary of your interaction, relevant action items or next steps, and a follow-up date. Manually creating a meeting summary and compiling all the notes and action items taken during the meeting takes some amount of time and often gets missed.

With the Sales app, you can quickly draft an email from the meeting recap in Teams. The email includes a summary of the meeting, action items, and follow-up tasks.

To create a post-meeting summary email:

1. [Open a meeting recap in Teams and view sales related insights](#view-sales-related-insights-in-meeting-recap).

1. Under the **Post-meeting actions** section, select **Draft email**. The email is drafted and opened in a pop-up window.

    :::image type="content" source="media/draft-email-recap.png" alt-text="Screenshot showing AI-generated draft email from meeting recap in Teams.":::

1. To copy the email content to your clipboard, select **Copy**.

1. To open the email in Outlook web, select **Open in Outlook web**.

1. Review and update the email content as needed, and then send it to your customers.

## Save AI-generated meeting notes to CRM

With intelligent recap, you can focus on the meeting discussion and not on capturing notes. AI-generated notes allow you to see key points and takeaways after the meeting.

AI-generated meeting notes can be saved to your CRM directly from the Teams meeting recap summary page. Depending on admin configuration, you can save the meeting notes either to a specific record in your CRM, such as an opportunity or account, or to the default appointment description field. This feature helps you maintain a record of meeting notes in your CRM for future reference or for sharing with your team.

By default, this feature is enabled.

> [!NOTE]
> Administrators can configure meeting notes to be saved either to the default appointment or event description field, or directly to a specific CRM record or object. If the default option is selected, saving AI-generated notes will create a new appointment or event and link it to the selected CRM record. If categorization fields have been set up by the admin, these options will appear when saving to a new appointment or event. However, categorization fields will not be shown if the appointment or event has already been created and saved to the CRM.

To save AI-generated meeting notes to CRM:

1. [Open a meeting recap in Teams and view sales related insights](#view-sales-related-insights-in-meeting-recap).
1. Under the **Post-meeting actions** section, select **Save to (CRM)**.
1. In the **Save meeting notes** window, search and select the record from the **CRM record** field. If the meeting is already saved to the CRM, the search bar doesn't appear. 
1. If required, edit the notes before saving them to CRM. 
1. Select **Save**.
    A confirmation message appears indicating that the meeting notes are saved to your CRM. You can view the saved meeting notes in your CRM by selecting **View saved notes**. Once notes are saved, all applicable internal participants will see the URL to the CRM record in place of the "Save to (CRM)" button.

If you don't see the **Save to (CRM)** button, it could be due to one of the following reasons:
- The meeting has multiple recordings.
- The meeting is a part of a recurring series.
- You're not signed in to the CRM.
- You don't have a valid license.
- The meeting transcript is not sufficiently long to generate meeting notes.
- Your administrator has disabled the [Save AI notes to CRM](save-ai-notes-crm.md) feature.
- Your administrator hasn't configured the correct CRM fields for saving notes.

### Related information

- [Meeting recap in Microsoft Teams](https://support.microsoft.com/office/meeting-recap-in-microsoft-teams-c2e3a0fe-504f-4b2c-bf85-504938f110ef)<br>
- [Intelligent productivity with Microsoft Teams Premium](https://support.microsoft.com/office/intelligent-productivity-with-microsoft-teams-premium-d5b02821-b9b1-4687-8c77-2f903ea68ad2)
