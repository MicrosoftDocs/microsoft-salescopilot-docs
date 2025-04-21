---
title: View sales insights in Microsoft Teams meeting recap
description: Discover how to use Copilot for Sales in Teams to get sales insights in Teams meeting recaps. 
ms.date: 04/15/2025
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:01/25/2024
---

# View sales insights in Microsoft Teams meeting recap

Microsoft 365 Copilot for Sales includes all the capabilities within Microsoft 365 Copilot to provide users with valuable insights to help you support customer engagements. The combined Copilot experience in products like Microsoft Teams combines the power of Copilot in Teams and Sales, offering seamless, role-specific capabilities for improved collaboration. The experience provides summarized meeting insights, and generated meeting recaps to enable sellers to grow customer relationships and close deals.

Here's the video that shows a [meeting preparation card in Teams](meeting-prep.md) and how to view sales insights using Teams meeting recap:

> [!VIDEO 159e3203-7996-4193-9037-e45cf0744dbf]

## License requirements

- [Microsoft 365 Copilot for Sales](https://www.microsoft.com/en-us/microsoft-365/copilot/copilot-for-sales#Pricing)

> [!NOTE]
> If you have existing Sales Copilot license, go to [View and understand the meeting summary](view-understand-meeting-summary.md).

## Prerequisites

- [Turn on Copilot AI features in your environment](suggested-replies.md).
- Add Copilot for Sales app to the meeting.
- Transcribe the meeting.

## Supported languages

To see a list of supported languages, go to [supported languages](supported-languages.md#ai-in-copilot-for-sales).

## View sales related insights in meeting recap

You can view a meeting recap if you record and transcribe a meeting. With Copilot for Sales added to the Teams meeting, you can view sales related insights in the meeting recap.

To view sales related insights, [open the meeting recap in Teams](https://support.microsoft.com/office/meeting-recap-in-microsoft-teams-c2e3a0fe-504f-4b2c-bf85-504938f110ef), select the down-arrow next to **Transcript**, and then select **Sales**.

The following information is available:

- **Post-meeting actions**: View a list of suggested post-meeting actions such as [creating a summary email for meeting participants](#create-a-post-meeting-summary-email) and [Save AI-generated meeting notes to CRM](#save-ai-generated-meeting-notes-to-crm).
- **Suggested follow-ups from the meeting**: View a list of follow-up tasks that are created during the meeting. You can also [create a task in CRM](#create-a-crm-task-from-a-meeting-recap) by selecting **Create task**.
- **Questions**: See questions that were asked during the meeting. It helps you to identify if your sellers are asking the right questions to understand customer needs. Questions are grouped by the person who asked them. When you select a question, the video jumps to the point in the conversation where the question was asked.
- **Participant statistics**: View a list of participants (from inside and outside your organization) and the following statistics:
    - **Talk to listen ratio**: See the average ratio of talk time to listen time. It helps you to identify if your sellers are talking too much or too little during customer calls. It also helps you to identify if your sellers are listening to customers and understanding their needs.
    - **Switches per conversation**: View the average number of switches between a sales rep and a customer in a conversation, meaning the number of times the conversation switched from one person to another. It helps you to identify if your sellers are engaging with customers during conversations.
    - **Avg. pause**: View the average pause time before a sales rep speaks during a conversation. It helps you to identify if your sellers are interrupting their customers before they finish talking or do they have enough patience.
    - **Longest monologue**: View the longest time a customer spoke during a conversation. It helps you to identify if your sellers are giving enough time to customers to speak and express their needs.
- **Keywords mentioned**: View keywords that were mentioned during the meeting. Keywords are grouped as per the following categories:
    - **Brands**: Names of brands that were mentioned during the meeting.
    - **Times**: Time mentioned during the meeting.
    - **People**: Names of people mentioned during the meeting.
    - **Others**: Other keywords mentioned during the meeting.
    
    If you track keywords and competitors in your CRM, they also appear in this section.

> [!NOTE]
> If you start and stop a meeting recording multiple times, sales insights aren't generated.

:::image type="content" source="media/sales-insights-recap.png" alt-text="Screenshot showing sales insights in Teams meeting recap.":::

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

With Copilot for Sales, you can quickly draft an email from the meeting recap in Teams. The email includes a summary of the meeting, action items, and follow-up tasks.

To create a post-meeting summary email:

1. [Open a meeting recap in Teams and view sales related insights](#view-sales-related-insights-in-meeting-recap).

1. Under the **Post-meeting actions** section, select **Draft email**. The email is drafted and opened in a pop-up window.

    :::image type="content" source="media/draft-email-recap.png" alt-text="Screenshot showing AI-generated draft email from meeting recap in Teams.":::

1. To copy the email content to your clipboard, select **Copy**.

1. To open the email in Outlook web, select **Open in Outlook web**.

1. Review and update the email content as needed, and then send it to your customers.

## Save AI-generated meeting notes to CRM

With intelligent recap, you can focus on the meeting discussion and not on capturing notes. AI-generated notes allow you to see key points and takeaways after the meeting.

You can save AI-generated notes to your CRM directly from the Teams meeting recap summary page. This allows you to save the meeting notes to a specific record in your CRM, such as an opportunity or account, or to the appointment description field by default. This is useful if you want to keep a record of the meeting notes in your CRM for future reference or to share with other team members.

> [!NOTE]
> This feature is enabled by default, but [administrators can revoke access](save-ai-notes-crm.md).

To save AI-generated meeting notes to CRM:

1. [Open a meeting recap in Teams and view sales related insights](#view-sales-related-insights-in-meeting-recap).
1. Under the **Post-meeting actions** section, select **Save to (CRM)**.
1. In the **Save meeting notes** window, search and select the record from the **CRM record** field. If the meeting is already saved to the CRM, the search bar doesn't appear. 
1. If required, edit the notes before saving them to CRM. 
1. Select **Save**.
    A confirmation message appears indicating that the meeting notes are saved to your CRM. You can view the saved meeting notes in your CRM by selecting **View saved notes**. Once notes are saved, all applicable internal participants will see the URL to the CRM record in place of the "Save to (CRM)" button.

### Related information

- [Meeting recap in Microsoft Teams](https://support.microsoft.com/office/meeting-recap-in-microsoft-teams-c2e3a0fe-504f-4b2c-bf85-504938f110ef)<br>
- [Intelligent productivity with Microsoft Teams Premium](https://support.microsoft.com/office/intelligent-productivity-with-microsoft-teams-premium-d5b02821-b9b1-4687-8c77-2f903ea68ad2)
