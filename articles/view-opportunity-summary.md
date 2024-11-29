---
title: View opportunity summary
description: Generate an opportunity summary with AI to help you interact better with customers and boost sales.
ms.date: 11/29/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:10/12/2023
---

# View opportunity summary

When reading an email or preparing for a meeting with a customer, you want to have relevant information from CRM, such as the customer asks, concerns, and notes, to help you get better context before the meeting.  
Copilot for Sales uses AI to generate a summary of each opportunity with key information like sales stage, budget, and close date. This helps you interact better with customers and boost sales and customer satisfaction.  
If you have a license for People.ai and the capability to display insights from People.ai is [enabled by your administrator](use-extensions.md#integrate-with-peopleai), insights from People.ai are displayed in the opportunity summary under the **Insights from People.ai** section.  
If there are notes added to the opportunity, they are also summarized and displayed under the **Latest activity** section. If you've [saved an email summary to the opportunity](view-save-email-summary-crm.md#save-email-summary-to-crm), it's included in the summarized notes. The notes summary highlights any issues or concerns addressed within notes. It makes it easy to catch up on the latest updates and quickly prepare for meetings with potential buyers.

> [!NOTE]
> - The opportunity summary for an email is displayed only if the email is saved to CRM and connected to an opportunity.
> - If a meeting is not connected to an opportunity, the opportunity summary for the meeting is displayed based on the most relevant opportunity selected by AI. You'll get an option to select another opportunity and regenerate the suggested content.
> - When you [set up a channel in Microsoft Teams using the deal room template](set-up-team-deal-room-template.md) and then [open it in Teams for the first time](collaborate-teams-newly-created-existing-team.md), the opportunity summary is displayed in the standard channel as   part of the welcome post.
> - You can view opportunity summary when [viewing details of an opportunity](view-record-details.md) in the Copilot for Sales pane in Outlook.
> - You can view the opportunity summary when [sharing CRM records in Teams](share-crm-record-teams-conversation.md).
> - Salesforce has two types of notes objects: "Notes and Attachments" and Notes (also known as Content Notes). You can use either of these objects to take notes and attach to the CRM records. However, Copilot for Sales only supports the "Notes and Attachments" object out of the box. If you want Copilot for Sales to support the Notes object, ask your administrator to contact Microsoft support.

:::image type="content" source="media/opportunity-annotations.png" alt-text="Screenshot showing the Opportunity summary with numbered annotations.":::

| Annotation | Description |
|------------|-------------|
| 1 | Summary about the opportunity. |
| 2 | Summarized notes added to the opportunity with citation numbers to show note text used to generate summary. More information: [View data source in opportunity summary](#view-data-source-in-opportunity-summary) |
| 3 | Copy the opportunity summary to clipboard. You can then paste the content as per your preferences. |
| 4 | Change the opportunity used to generate the summary. More information: [Change the opportunity used to generate summary](#change-the-opportunity-used-to-generate-summary) |
| 5 | Name of the opportunity for which summary is generated. |
| 6 | Share feedback or wrong content using the thumbs-up or thumbs-down arrow. More information: [Share feedback](#share-feedback) |

## Supported languages

To see a list of supported languages, see [supported languages](supported-languages.md#ai-in-copilot-for-sales).

## View the summary

1. In Outlook, open an email or the scheduled meeting.  
1. Open the **Copilot for Sales** pane.  
    The opportunity summary is displayed in the **Opportunity summary** card.  
If you have a license for People.ai, insights from People.ai are also displayed. More information: [View People.ai insights](people-ai-insights.md)

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

If you have any feedback about the opportunity summary, you can share it by selecting the appropriate icon at the bottom of the summary. Your feedback is valuable, and we use it to improve the functionality.

> [!NOTE]
> Ensure that you don't enter any personal information while sharing feedback.

1. At the bottom of the opportunity summary, select :::image type="icon" source="media/thumbs-up.png" border="false"::: or :::image type="icon" source="media/thumbs-down.png" border="false":::.  
   After you select an icon, you'll get a **Tell us more** link.  
1. Select the link to open the feedback form.  
1. Enter your responses in the feedback form and then select **Send**.

### Related information

[Enrich CRM record summary with insights from your application](extend-record-summary.md)
