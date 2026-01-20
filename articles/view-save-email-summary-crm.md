---
title: View and save email summaries to your CRM
description: Learn how to use the Sales app to save summaries of sales-related emails to your Dynamics 365 or Salesforce CRM.
ms.date: 11/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:12/18/2023
---

# View and save email summaries to your CRM

Save time by letting the Sales app summarize and save important email information to your CRM in seconds. Share summaries to Microsoft Teams or copy them for other uses. 

When available, the summary includes information whether budget, stakeholders, need, and timing are mentioned in the email or not. This information is displayed only for external emails and when detected with a high probability by AI.

Email summaries are available when:

- The email is to or from a contact outside your company, and the contact exists in your CRM.
- The email content is more than 1,000 characters, or about 150&ndash;200 words in English. If the email is too short, Copilot doesn't have enough information to generate a summary.
- The email is in one of the supported languages. Learn more in [Supported languages in the Sales app for Outlook and Teams](introduction.md#supported-languages-and-geographies).
- The email isn't encrypted.

> [!NOTE]
> Based on the license you have, you can see the email summary either [within Outlook](email-summary-premium.md) or in the **Sales** app in Outlook.

## Anatomy of an email summary

:::image type="content" source="media/email-summary-replying.png" alt-text="Screenshot of an email summary card in the Sales app pane in Outlook when replying to an email, with numbered callouts.":::

Legend:

1. Card title
1. Citation number
1. Draft an email with Copilot
1. Share to Teams or the clipboard
1. Save the summary to your CRM or change the language
1. Share feedback on the email summary

## View an email summary

You can add the summary to your CRM, share it to Teams, or copy it to the clipboard from this view.

> [!IMPORTANT]
> Always check AI-generated content carefully for accuracy and appropriateness before you share it.

1. In Outlook, open an email in the reading pane or in a separate window and start drafting a reply.

1. Open the **Sales** pane if it isn't already open. After a moment or two, the email summary is displayed in the **Key email info** card.

    > [!NOTE]
    > If the contact isn't in your CRM, the **Key email info** card isn't displayed. [Add the contact to your CRM](create-contact-crm.md). The email summary should appear a few moments later.

In the **Key email info** card, you can perform the following tasks:

- To check where Copilot got the information for the summary, select a citation number. The exact quote from the email and the name of the person who said it are displayed.

    :::image type="content" source="media/summary-citation.png" alt-text="Screenshot of a citation in the Sales app pane in Outlook.":::

    To view basic information about the contact, account, or opportunity, select the link in blue. To view complete details in your CRM, select :::image type="icon" source="media/open-record.png" border="false"::: on the summary card.

    :::image type="content" source="media/summary-source.png" alt-text="Screenshot of contact details in the Sales app pane in Outlook.":::

- To draft a reply from scratch with Copilot's help, select **Draft an email**. To start with some context, select the arrow next to **Draft an email**, and then select either **Reply to an inquiry**, **Make a proposal**, or **Address a concern**. Learn more in [Draft an email message in the Sales app](./use-copilot-kickstart-email-messages.md).

- To share the summary to Microsoft Teams, select **Share** > **Share to Teams**. In the search box under **Share to:**, start typing the name of a person, channel, or chat, and then select it from the list. Add a message if you like, edit the summary if needed, and then select **Share**. Learn more in [Share email summaries to Microsoft Teams](./share-insights-from-outlook-to-teams.md).

- To copy the summary for use in other applications, select **Share** > **Copy summary**.

- To change the language of the email summary, select **...** > **Change language**, select the language from the list, and then select **Change**. View the [list of supported languages](introduction.md#supported-languages-and-geographies).

- To provide feedback on the email summary, select the thumbs-up or thumbs-down icon. Be sure not to share personal information in your feedback.

### Save an email summary to your CRM

With the Sales app, save an email summary to one record only. If you try to save it again, the option is no longer available.

1. In the [**Key email info** card](#view-an-email-summary), select **...** > **Save summary to CRM**, where *CRM* is the name of your CRM system.

1. Under **Select a record**, select or search for a contact, account, or opportunity record to add the email summary to. Your search results are added to the suggested records list, so you can safely search and try again.

    If there are multiple opportunities related to contact, the Sales app displays a list of suggested opportunities, ranked by AI, to save the summary. In this case, the first opportunity is selected by default.
    
    If the email is already connected to an opportunity, it's selected by default.

    If no opportunity is connected, the top ranked opportunity, which is determined by the open opportunities available for the account or contact, and the content of the email, will be selected by default.

1. Select **Save**.

    > [!NOTE]
    > - When you search for a record to connect to, the search results show the record name and the key fields that your administrator selected.
    > - You can connect to all record types that your administrator enabled for activities and added to the Sales app.

    :::image type="content" source="media/select-record.png" alt-text="Screenshot of suggested records in the Sales pane in Outlook, with numbered callouts.":::

Legend:

1. Records suggested by the Sales app
1. Record added from the search box

The email summary is saved to your CRM as a note on the selected record. The subject is the same for all the Sales app notes: "[AI generated] Email summary from Sales Copilot." The note includes the email subject and the timestamp when the note was saved. After you save the summary to the record, you can edit it in your CRM system.

:::image type="content" source="media/timeline.png" alt-text="Screenshot of a note added to a timeline in Dynamics 365 Sales Hub.":::

> [!NOTE]
> Salesforce has two types of note objects: "Notes and Attachments" and "Notes," also known as "Content Notes." You can use either of these objects to attach notes to a CRM record. The Sales app only supports the "Notes and Attachments" object out of the box. If you want it to support the "Notes" object, ask your Salesforce administrator to contact Microsoft Support.

## Related information

- [Save Outlook activities to your CRM](./save-outlook-activities-crm.md)
- [Create a contact in your CRM from the Sales app](./create-contact-crm.md)
- [Draft an email message in the Sales app](./use-copilot-kickstart-email-messages.md)
