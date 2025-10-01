---
title: View an opportunity summary
description: Learn how to view an AI-powered opportunity summary in Microsoft Copilot for Sales to help you interact more productively with customers and boost sales.
ms.date: 09/29/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:10/12/2023
---

# View an opportunity summary

When you're preparing for a meeting with a customer, context from your customer relationship management (CRM) system, such as the customer's questions and concerns and notes you and your colleagues took, can help you feel more confident and in control when the meeting starts. Copilot for Sales gives you that context. It uses AI to generate a summary of your opportunities that includes key information, helping make your interactions with customers more productive, boosting sales, and leaving your customers satisfied.

An opportunity summary can include the following kinds of information:

- If notes are added to the opportunity, they're summarized and displayed in the **Latest activity** section of the opportunity summary. The notes summary highlights any issues or concerns that are mentioned in the notes, making it easy to catch up on the latest updates and quickly prepare for meetings with potential buyers.

- If you [saved an email summary to your CRM and it's connected to the opportunity](view-save-email-summary-crm.md#save-an-email-summary-to-your-crm), it's included in the summarized notes. The notes summary highlights any issues or concerns addressed within notes. It makes it easy to catch up on the latest updates and quickly prepare for meetings with potential buyers.

If the opportunity isn't connected to a meeting, the opportunity summary is based on the most relevant opportunity the AI can find. You can [select a different opportunity](#change-the-opportunity-used-to-generate-summary) and generate another summary if needed.

You can view the opportunity summary in the following places:

- When you [set up a channel in Microsoft Teams using the deal room template](set-up-team-deal-room-template.md) and then [open it in Teams for the first time](collaborate-teams-newly-created-existing-team.md), the opportunity summary is displayed as part of the welcome post in the standard channel.

- When you [share CRM records in Teams](share-crm-record-teams-conversation.md).

> [!NOTE]
> Salesforce has two types of notes objects: "Notes and Attachments" and Notes (also known as Content Notes). You can use either of these objects to take notes and attach to the CRM records. However, Copilot for Sales only supports the "Notes and Attachments" object out of the box. If you want Copilot for Sales to support the Notes object, ask your administrator to contact Microsoft support.

:::image type="content" source="media/opportunity-annotations.png" alt-text="Screenshot showing the Opportunity summary with numbered annotations.":::

| Annotation | Description |
|------------|-------------|
| 1 | Summary about the opportunity. |
| 2 | Summarized notes added to the opportunity with citation numbers to show note text used to generate summary. More information: [View data source in opportunity summary](#view-data-source-in-summary) |
| 3 | Copy the opportunity summary to clipboard. You can then paste the content as per your preferences. |
| 4 | Change the opportunity used to generate the summary. More information: [Change the opportunity used to generate summary](#change-the-opportunity-used-to-generate-summary) |
| 5 | Name of the opportunity for which summary is generated. |
| 6 | Share feedback or wrong content using the thumbs-up or thumbs-down arrow. More information: [Share feedback](#share-feedback) |

Here's the video that shows how to view the opportunity summary and [update the CRM based on suggested updates](suggested-crm-updates.md):

> [!VIDEO 8f9ab913-0eec-48f5-a4ad-a1e3236482bd]

## Supported languages

To see a list of supported languages, see [supported languages](introduction.md#supported-languages-and-geographies).

## View the summary

1. In Outlook, open an email or the scheduled meeting.  
1. Open the **Copilot for Sales** pane.
1. In the **Opportunities** card, select the opportunity to view its details.
    The opportunity summary is displayed at the top of the pane.

## View data source in summary

Summarized notes in the opportunity summary are displayed with citation numbers. Select the citation number to see the following details:

- Author of the original note  
- Date and time when the note was captured  
- Original content of the note

:::image type="content" source="media/opportunity-summary.png" alt-text="Screenshot showing the Opportunity summary data source.":::

## Change the opportunity used to generate summary

1. In the message at the bottom of the summary, select **Change**.  
1. Under **Select opportunity to summary**, select the opportunity that you want to summarize.  

   :::image type="content" source="media/select-opportunity.png" alt-text="Screenshot showing the Select an opportunity to summarize pane.":::

1. Select **Create a summary**.  
    A new summary is generated based on the selected opportunity.

## Share feedback

If you have any feedback about the opportunity summary or its AI-generated content, share it by selecting the appropriate icon at the bottom of the summary. Your feedback is valuable, and we use it to improve the functionality.

> [!NOTE]
> Ensure that you don't enter any personal information while sharing feedback.

1. At the bottom of the opportunity summary, select :::image type="icon" source="media/thumbs-up.png" border="false"::: or :::image type="icon" source="media/thumbs-down.png" border="false":::.  
   After you select an icon, you'll get a **Tell us more** link.  
1. Select the link to open the feedback form.  
1. Enter your responses in the feedback form and then select **Send**.

### Related information

[Enrich CRM record summary with insights from your application](extend-record-summary.md)
