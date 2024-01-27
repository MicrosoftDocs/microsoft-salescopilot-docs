---
title: View and save email summary to CRM
description: Learn how to view and save an email summary to CRM.
ms.date: 01/09/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:12/18/2023
---

# View and save email summary to CRM

When interacting with your customers over email, you often need to update your CRM system with the latest information. Manually updating the CRM system every time you interact with customers via email can be time-consuming and error prone. Additionally, it could potentially add noise to the CRM system, by overloading records with email exchanges.

Copilot for Sales uses AI to summarize email conversations and provides you with options to copy the summary and to add the summary to your CRM system as a note to a record.

When available, the summary includes information whether budget, stakeholders, need, and timing are mentioned in the email or not. This information is displayed only for external emails and when detected with a high probability by AI.

## License requirements

Capabilities mentioned in this article are available only to users with the Copilot for Sales standard license. If you have the Copilot for Sales premium license, see [Summarize an email thread using sales information in Outlook](email-summary-premium.md)

## Anatomy of email summary

:::image type="content" source="media/email-summary.png" alt-text="Screenshot showing the Email summary with annotations.":::

| Annotation | Description |
|------------|-------------|
| 1 | Citation number to show email text used to generate summary. More information: [View data source](#view-data-source-in-email-summary) |
| 2 | **More options** menu to: <ul><li>[Save the email summary to your CRM system as a note to a record](#save-email-summary-to-crm)</li><li>Copy the email summary to clipboard. You can then paste the content as per your preferences.</li></ul> |
| 3 | Share feedback or wrong content using the thumbs-up or thumbs-down arrow. More information: [Share feedback](#share-feedback) |

> [!NOTE]
>
> - Email summary will be generated only for emails or email threads with more than 1000 characters, which is about 180 words.
>
> - The email summary will contain up to 400 characters.
>
> - After adding the summary to your CRM system, you can edit it as needed.
>
> - You must check the AI-generated content carefully, as it can have mistakes. It is your responsibility to review and edit the AI-generated summaries to make sure it's accurate and appropriate.

## Supported languages

The generation of email summary is supported in the following languages: English, Spanish, German, and French.

## View email summary

1. In Outlook, open or reply to a customer email.

1. Open the **Copilot for Sales** pane.

1. On the **Highlights** tab, the email summary is displayed in the **Key info** card.

> [!NOTE]
> If the email content is less than 1000 characters, the email summary is not generated.

## Save email summary to CRM

1. [View the email summary](#view-email-summary).

1. In the **Key info** card, select **More options** (**...**), and then select **Save summary to (CRM)**.

1. Under **Select a record**, select one of the suggested records or use the search box to find another record.

   If there are multiple opportunities related to contact, Copilot for Sales displays a list of suggested opportunities, ranked by AI, to save the summary. In this case, the first opportunity is selected by default.

   > [!NOTE]
   > - If the email is already connected to an opportunity, it's selected by default.
   > - If no opportunity is connected, the top ranked opportunity, which is determined by the open opportunities available for the account or contact, and the content of the email, will be selected by default.
   > - When you search for a record, the search results display the record name and the key fields selected by your administrator. For more information about key fields, see [Select key fields for mini view](customize-forms-and-fields.md#select-key-fields-for-the-mini-view).
   > - Your search results will be added to the suggested records list, so you can safely search and try again.
   > - Currently, you can save the summary to one record using Copilot for Sales.
   > - You can connect to all record types that are enabled for activities and added to Copilot for Sales by your administrator. For more information about adding record types, see [Add a new record type (or a Salesforce object)](customize-forms-and-fields.md#add-a-new-record-type-or-a-salesforce-object).

   :::image type="content" source="media/select-record.png" alt-text="Screenshot showing how to select an opportunity to save the email summary.":::

1. Select **Save**.

    The email summary is saved to CRM as a note to the selected record. All Copilot for Sales notes share the same subject: "[AI generated] Email summary from Copilot for Sales" and include the subject of the email itself, as well as the timestamp when the note was saved.

   :::image type="content" source="media/timeline.png" alt-text="Screenshot showing the Email summary saved as a note in CRM.":::

## View data source in email summary
Information identified from the CRM, such as contact and account records, is displayed as a data source within the email summary for quick reference.

CRM data in the email summary is displayed in blue color. Select the content to see information about the CRM data. You can also open a record in CRM to view its complete details by selecting :::image type="icon" source="media/open-record.png" border="false"::: on the CRM record card.

Email data used in the email summary is displayed with citation numbers. Select the citation number to see exact quote text from the email and the name of the person quoting it.

:::image type="content" source="media/summary-source.png" alt-text="Screenshot showing the Email summary data source.":::

## Share feedback

If you have any feedback about the email summary, you can share it by selecting the appropriate icon at the bottom of the email summary. Your feedback is valuable, and we use it to improve the functionality.

> [!NOTE]
> Ensure that you don't enter any personal information while sharing feedback.

1. At the bottom of the email summary, select :::image type="icon" source="media/thumbs-up.png" border="false"::: or :::image type="icon" source="media/thumbs-down.png" border="false":::.

   After you select an icon, you'll get a **Tell us more** link.

1. Select the link to open the feedback form.

1. Enter your responses in the feedback form and then select **Send**.
