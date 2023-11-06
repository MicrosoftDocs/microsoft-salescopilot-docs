---
title: View opportunity summary
description: Generate an opportunity summary with AI to help you interact better with customers and boost sales.
ms.date: 11/13/2023
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

Sales Copilot uses AI to generate a summary of each opportunity with key information like sales stage, budget, and close date. This helps you interact better with customers and boost sales and customer satisfaction.

If you have a license for People.ai and the capability to display insights from People.ai is [enabled by your administrator](use-extensions.md#integrate-with-peopleai), insights from People.ai are displayed in the opportunity summary under the **Insights from People.ai** section. 

If there are notes added to the opportunity, they are also summarized and displayed under the **Latest activity** section. If you've [saved an email summary to the opportunity](view-save-email-summary-crm.md#save-email-summary-to-crm), it's included in the summarized notes. The notes summary highlights any issues or concerns addressed within notes. It makes it easy to catch up on the latest updates and quickly prepare for meetings with potential buyers.

> [!NOTE]
> - The opportunity summary for an email is displayed only if the email is saved to CRM and connected to an opportunity.
> - If a meeting is not connected to an opportunity, the opportunity summary for the meeting is displayed based on the most relevant opportunity selected by AI. You'll get an option to select another opportunity and regenerate the suggested content.
> - When you when you [set up a channel in Microsoft Teams using the deal room template](set-up-team-deal-room-template.md) and then [open it in Teams for the first time](collaborate-teams-newly-created-existing-team.md), the opportunity summary is displayed in the standard channel as   part of the welcome post.
> - You can view opportunity summary when [viewing details of an opportunity](view-record-details.md) in the Sales Copilot pane in Outlook.

:::image type="content" source="media/opportunity-annotations.png" alt-text="Screenshot showing the Opportunity summary with numbered annotations.":::

| Annotation | Description |
|------------|-------------|
| 1 | Summary about the opportunity. |
| 2 | Summarized notes added to the opportunity with citation numbers to show note text used to generate summary. More information: [View data source in opportunity summary](#view-data-source-in-opportunity-summary) |
| 3 | Copy the opportunity summary to clipboard. You can then paste the content as per your preferences. |
| 4 | Change the opportunity used to generate the summary. More information: [Change the opportunity used to generate summary](#change-the-opportunity-used-to-generate-summary) |
| 5 | Name of the opportunity for which summary is generated. |
| 6 | Share feedback or wrong content using the thumbs-up or thumbs-down arrow. More information: [Share feedback](#share-feedback) |

## View opportunity summary

1. In Outlook, open an email or the scheduled meeting.

1. Open the **Sales Copilot** pane.

    On the **Highlights** tab, the opportunity summary is displayed in the **Opportunity summary** card.

    If you have a license for People.ai, insights from People.ai are also displayed. More information: [View People.ai insights](#view-peopleai-insights-in-opportunity-summary-preview)

## View People.ai insights in opportunity summary (preview)

[!INCLUDE [preview-banner-section](includes/preview-banner-section.md)]

**Prerequisites**: 

- The People.ai integration must be [enabled by your administrator](use-extensions.md#integrate-with-peopleai).  
- You must have a license for People.ai.

Insights from People.ai are displayed under the **Insights from People.ai** section. Insights are displayed with citation numbers. Select the citation number to drill down and see detailed information. To open metrics in People.ai, select :::image type="icon" source="media/open-record.png" border="false"::: at the bottom-right of the card.

:::image type="content" source="media/people-ai-oppty-insights.png" alt-text="Screenshot showing People.ai insights in opportunity summary.":::

The following insights are displayed:

- **Engagement level and trend**: This is the overall engagement level and trend. The engagement level number is calculated by People.ai based on interactions (emails and meetings) that have happened with the customer. The engagement level is displayed as follows:
   
    |Engagement level number  |Engagement level  |
    |---------|---------|
    |0 to 30     | Low        |
    |31 to 70     | Medium        |
    |71 to 100     | High        |
    
    The engagement trend is calculated by comparing the current week’s engagement level number with that of the previous week. The engagement trend is displayed as trending up or down based on the increase or decrease of the engagement level respectively.
    
    When you drill down into the engagement level and trend, you can see the total number of activities, along with the breakdown of the number of meetings and emails that have been exchanged with the customer.

- **Connections**: This insight suggests the names of your colleagues who have interacted with the customer through emails or meetings. It helps you quickly email your colleagues to request an introduction. When you drill down, you can see the names of the people. By default, the top three connections are displayed. 

    To quickly start an email with one of the top connections, hover over the name, and then select :::image type="icon" source="media/mail-icon.png" border="false":::.

    To see all connections or more metrics, you must open People.ai.

## View latest activities from partner applications (preview)

[!INCLUDE [production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

[!INCLUDE [preview-banner-section](includes/preview-banner-section.md)]

You can view activities that are related to CRM opportunities or deals from partner applications within Sales Copilot. To view activities from partner applications, you must:

1. Get the feature enabled, as it is not enabled by default.
2. Create a connection using Power Apps connectors.
3. View latest activities from partner applications.

### Get the feature enabled

This feature is not enabled by default. To enable this feature, ask your administrator to [sign up for the preview feature](https://aka.ms/SalesCopilotExtensibilityPreview). The Microsoft team will get in touch to validate the request and enable the feature for your organization.

### Create a connection

After the feature is enabled, you must create a connection between Sales Copilot and the partner application using the partner's certified Power Apps connector. For information about how to create a connection, see [Create a new connection](/power-apps/maker/canvas-apps/add-manage-connections#create-a-new-connection).

> [!NOTE]
> - All Power Apps connectors are not certified to work with Sales Copilot. Sales Copilot displays activities from partner applications that have implemented specific APIs and made them available through their Power Apps connectors.
> - If you are a partner application maker and would like to integrate with Sales Copilot, see Extend Sales Copilot. Currently, DocuSign can be integrated with Sales Copilot. 

### View latest activities

Latest activities from partner applications are displayed under the **Latest activities from (parter app)** section. For example, in the following image, the activities from the partner application **DocuSign** are displayed in the opportunity summary.

`image`

All the information about activities comes from the partner applications. Sales Copilot renders the activity information retrieved from the partner application through the Power Apps connector. Sales Copilot does not edit or filter the information.

Activities are displayed with citation numbers. Select the citation number to drill down and see detailed information. To view more details in the partner application, select :::image type="icon" source="media/open-record.png" border="false"::: at the bottom-right of the card. 

## View data source in opportunity summary

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

