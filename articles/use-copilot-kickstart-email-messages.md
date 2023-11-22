---
title: Use Copilot to kickstart email messages
description: Generate an email reply with pre-defined categories or custom prompt using Sales Copilot's AI to save time and effort.
ms.date: 11/22/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/08/2023
---

# Use Copilot to kickstart email messages

When you compose a new email or reply to your customers by email, Sales Copilot uses AI to suggest content, saving you time and effort in composing the perfect message to move a deal forward. Choose from pre-defined response categories or enter your own text, and the AI generates the suggested content. You can use the suggested content as-is or modify to meet your needs.

> [!NOTE]
>
> - This feature is available only when enabled by your administrator. More information: [Configure suggested email content in Outlook](suggested-replies.md)
>
> - The AI-generated content is just a suggestion. It is your responsibility to review and edit the suggested content to make sure it's accurate and appropriate before sending your email.

:::image type="content" source="media/anatomy.png" alt-text="Screenshot showing the numbered anatomy of the suggested content corresponding to the following table.":::

| Annotation | Description |
|------------|-------------|
| 1 | Information from CRM is displayed in blue. More information: [View data source in suggested content](#view-data-source-in-suggested-content) |
| 2 | Meeting time suggested. More information: [Add or remove meeting suggestion](#add-or-remove-meeting-suggestion) |
| 3 | Share feedback using the thumbs-up or thumbs-down arrow. More information: [Share feedback](#share-feedback) |
| 4 | Change the opportunity used in suggested content. More information: [Enhance suggested content with another opportunity](#enhance-suggested-content-with-another-opportunity) |
| 5 | Add the suggested content to email. |
| 6 | Copy the suggested content and paste it in email or Teams chat. |
| 7 | **More options** menu to:<ul><li>Restore suggested content to its previous version. More information: [Restore suggested content](#restore-suggested-content)</li><li>Generate another version of the suggested content.</li><li>Start over and generate a new suggested content.</li></ul> |
| 8 | **Adjust draft** menu to:<ul><li>[Set length of suggested content](#set-length-of-suggested-content)</li><li>[Adjust tone of the suggested content](#adjust-tone-of-the-suggested-content)</li><li>[Add or remove meeting suggestion](#add-or-remove-meeting-suggestion)</li><li>[Set language of suggested content](#set-language-of-suggested-content)</li><li>[Enter text to refine the suggested content](#refine-suggested-content)</li></ul> |

## Supported languages

AI in Sales Copilot is supported in the following languages: English, Spanish, German, and French. The email and custom prompt must be in one of the supported languages to generate the suggested content.

## Create an email reply using pre-defined categories

You can get suggested responses when you reply to a customer email or as you're reading one.

1. In Outlook:

    - Open a customer email and select **Reply**. In the banner message at the top of the draft email, select **Use Copilot now**.

    - When you're reading an email, open the Sales Copilot pane.

1. On the **Highlights** tab, select a pre-defined category.

   :::image type="content" source="media/response-categories.png" alt-text="Screenshot showing the pre-defined response categories.":::

1. Review the suggested content.

    To generate a different suggestion, select **More options**, and then select **Try again**.

    [Refine the suggested content](#refine-suggested-content), if required. You can also [restore the suggested content](#restore-suggested-content) to the previous version.

1. Select **Add to email** to paste the content in the email body.

   > [!NOTE]
   > Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

   :::image type="content" source="media/suggested-content.png" alt-text="Screenshot showing the suggested content.":::

1. Edit the email content as required, and then send it.

## Create an email message using custom prompt

If the pre-defined response categories don't suit your requirements, you can enter custom prompt to generate suggested content.

You can get suggested email content when you reply to a customer email, read an email, or compose a new email.

> [!NOTE]
>
> - Information from CRM is not displayed when using custom prompt to generated suggested email content.
>
> - You can generate suggested content for emails containing internal email addresses also. If all email addresses are internal, you'll only see the option to enter custom prompt. If you add an external email address, pre-defined response categories are made available.

1. In Outlook:

    - When replying to a customer's email or composing a new email, select **Use Copilot now** in the banner message at the top of the draft email.

    - When you're reading an email, open the Sales Copilot pane.

1. On the **Highlights** tab, select **Describe the email you want**.

   :::image type="content" source="media/response-categories.png" alt-text="Screenshot showing the Pre-defined response categories.":::

   > [!NOTE]
   > Pre-defined response categories are not available while composing a new email. You can only enter custom prompt or [create an email to summarize your sales meeting](#create-a-sales-meeting-summary-email-preview).

1. In the textbox, enter a phrase to describe the kind of reply you want to send, and then press **Enter**.

1. Review the suggested content.

    To generate a different suggestion, select **More options**, and then select **Try again**.

    [Refine the suggested content](#refine-suggested-content), if required. You can also [restore the suggested content](#restore-suggested-content) to the previous version.

1. Select **Add to email** to paste the content in the email body.

   > [!NOTE]
   > Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

1. Edit the email content as required, and then send it.

### Custom prompt best practices

Here are some best practices for writing custom prompt:

- **Keep it concise**: Although the AI engine can handle longer prompts, shorter prompts are simpler to use and can help you get targeted replies.

- **Be specific**: The more specific you are in your prompt, the more targeted the response will be. For example, instead of asking "What's your favorite food?" you could ask "What's your favorite type of Mexican food?"

- **Use context**: Be sure to include relevant context in your prompts to help the AI better understand what you're asking.

- **Avoid using personal pronouns**: Don't include personal pronouns (for example, "I," "me," "my") in your prompts.

- **Keep it appropriate**: The AI uses a general-purpose language model and can generate responses to a wide variety of prompts. It's always a good idea to keep your prompts appropriate for a general audience.

## Save and reuse custom prompts

When you create an email message using custom prompt, you can save the prompt for future use. This helps you save time and effort when you need to send similar messages to multiple recipients. You can save up to three prompts and reuse them as and when required.

### Save a custom prompt

1.  [Generate suggested content using custom prompt](#create-an-email-message-using-custom-text).

2.  At the top of the suggested content, hover over the prompt, and then select the star icon :::image type="icon" source="media/save-prompt-icon.png" border="false":::.

    :::image type="content" source="media/save-prompt.png" alt-text="Screenshot showing icon to save a prompt.":::

    The prompt is saved and displayed under the **Favorites** section when you create a new email message using custom prompt.

    :::image type="content" source="media/saved-prompt.png" alt-text="Screenshot showing a saved prompt.":::

### Use a saved prompt

1.  Open Sales Copilot.

2.  On the **Highlights** tab, select **Describe the email you want**.

3.  Under the **Favorites** section, select the prompt you want to use.

    :::image type="content" source="media/select-prompt.png" alt-text="Screenshot showing saved prompts.":::

### Remove a saved prompt

You can save a maximum of three prompts. If you want to save more prompts, you must remove an existing prompt.

1.  Open Sales Copilot.

2.  On the **Highlights** tab, select **Describe the email you want**.

3.  Under the **Favorites** section, select the star icon :::image type="icon" source="media/remove-prompt-icon1.png" border="false"::: for the prompt you want to remove.

    Alternately, you can generate suggested content using the saved prompt, and then select the star icon :::image type="icon" source="media/remove-prompt-icon2.png" border="false"::: beside the prompt.

    :::image type="content" source="media/remove-prompt.png" alt-text="Screenshot showing icon to remove a saved prompt":::


## Enhance suggested content with another opportunity

If you've used a response category (Make a proposal or Address a concern) that uses an opportunity record to generate the suggested content, a message is displayed that the generated content is based on the opportunity. If there are multiple opportunities related to the contact, you'll get an option to select another opportunity to regenerate content.

If there are multiple opportunities related to contact, the most relevant opportunity is selected by AI. You'll get an option to select another opportunity, if the previously selected opportunity is not correct, and then regenerate the suggested content.

If there are no additional open opportunities identified by the AI model, no option is displayed to select an opportunity.

1. Generate the suggested reply using an appropriate response category. In the message at the bottom of the suggested reply, select **Change**.

   :::image type="content" source="media/change-suggested.png" alt-text="Screenshot showing how to select another opportunity to generate a new reply.":::

1. Under **Relevant opportunity**, select the opportunity that you want the generated content to refer to.

   :::image type="content" source="media/select-relevant.png" alt-text="Screenshot showing where to select a new opportunity.":::

   > [!NOTE]
   >
   > - Sales Copilot displays opportunities that are related to the contacts in the email.
   >
   > - The information displayed below the opportunities is displayed as customized by your administrator. More information: [Select key fields for the mini view](customize-forms-and-fields.md#select-key-fields-for-the-mini-view)

1. Select **Create a new draft**.

    A new reply is generated based on the selected opportunity.

## View data source in suggested content

View information about data pulled from your CRM and Office 365, such as contact, opportunities, account, and email in the suggested content.

CRM data used in the suggested content is displayed in blue color. Select the content to see information about the CRM data. You can also open a record in CRM to view its complete details by selecting :::image type="icon" source="media/open-record.png" border="false"::: on the CRM record card.

Email data used in the suggested content is displayed with citation numbers. Select the citation number to see information about the email content used.

The following information is displayed in the suggested content:

- From CRM:

  - Contact

  - Account

  - Opportunity

  - Product

  - Activity

- From Office 365:

  - Availability

  - Email

:::image type="content" source="media/crm-data.png" alt-text="Screenshot showing the CRM data in suggested content.":::

## Refine suggested content

After you've generated the suggested content, you can refine the results further by providing a new prompt that builds upon the previous suggestion. This allows you to fine-tune your email replies according to the needs and preferences. For example: Make it formal, make it shorter, or suggest a meeting next week.

1. Generate the suggested reply using an appropriate response category.

1. Select **Adjust draft**.

1. Under **Add details**, enter the changes you want to be made in the content, and then select **Update**. For example, provide a 10% discount on the next purchase.

1. Review the suggested content.

    To generate a different suggestion, select **More options**, and then select **Try again**.

    Refine the suggested content further, if required. You can also [restore the suggested content](#restore-suggested-content) to the previous version.

1. Select **Add to email** to paste the content in the email body.

   > [!NOTE]
   > Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

1. Edit the email content as required, and then send it.

## Set length of suggested content

You can set the length of the suggested content to be short, medium, or long. The default length is medium. 

1. Generate the suggested reply using an appropriate response category.

1. Select **Adjust draft**.

1. Under **Length**, select the content length you want to use and then select **Update**.

1. Review the suggested content.

    To generate a different suggestion, select **More options**, and then select **Try again**.

    [Refine the suggested content](#refine-suggested-content), if required. You can also [restore the suggested content](#restore-suggested-content) to the previous version.

1. Select **Add to email** to paste the content in the email body or **Copy content** when you are reading an email.

   > [!NOTE]
   > Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

1. Edit the email content as required, and then send it.

## Adjust tone of the suggested content

After you've generated the suggested content, you can adjust the tone of the content according to the relationship with the customer or whatever feels comfortable. It helps you to be more productive and write better emails. For example, you can change the tone from professional to formal.

1. Generate the suggested reply using an appropriate response category.

1. Select **Adjust draft**.

1. Under **Adjust tone**, select the tone you want to use and then select **Update**.

1. Review the suggested content.

    To generate a different suggestion, select **More options**, and then select **Try again**.

    [Refine the suggested content](#refine-suggested-content), if required. You can also [restore the suggested content](#restore-suggested-content) to the previous version.

1. Select **Add to email** to paste the content in the email body or **Copy content** when you are reading an email.

   > [!NOTE]
   > Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

1. Edit the email content as required, and then send it.

## Restore suggested content

You can restore the suggested content to the previous version when you generate a new suggested content either by selecting **Try again** or [refining it](#refine-suggested-content).

You can't restore suggested content to the previous version in the following scenarios:

- You [change the opportunity](#enhance-suggested-content-with-another-opportunity) and create a new draft.

- You [change the meeting](#change-the-meeting-used-to-create-a-summary-preview) and create a new draft.

- When only the first draft is generated.

You can only restore to the previous draft. For example, you can restore draft #2 from draft #3, but not to draft #1.

To restore suggested content to its previous version, select **More options**, and then select **Restore last version**.

## Add or remove meeting suggestion

By default, a meeting time is not included in the suggested content. If a customer has requested a meeting at a certain time and mentioned the same in an email, the meeting time is included in the suggested content. The meeting time displayed in the suggested content is in your time zone.

### Add a meeting time suggestion

If you want to have a meeting with a customer, you can include a meeting time in the suggested content. The meeting time suggested is the first available slot in your calendar.

1. Generate the suggested content using an appropriate response category.

1. Select **Adjust draft**.

1. Under **Suggest a meeting time**, select the meeting time displayed.

   :::image type="content" source="media/meeting-time.png" alt-text="Screenshot showing the meeting time selected.":::

1. Select **Update**.

### Remove the meeting time suggestion

1. Generate the suggested content using an appropriate response category.

1. Select **Adjust draft**.

1. Under **Suggest a meeting time**, clear the meeting time selected.

   :::image type="content" source="media/remove-suggestion.png" alt-text="Screenshot showing where to remove a meeting time suggestion.":::

1. Select **Update**.

## Set language of suggested content

The language of the suggested content is determined as follows:
- If you're replying to an email, the language of the suggested content is the same as the language of the email. 
- If you're composing a new email and using custom prompt to generate the suggested content, the language of the suggested content is the same as the language of the custom prompt. 

In some cases, you may want to generate the suggested content in a different language. For example, you may want to generate the suggested content in the language of the customer.

You can set the language of the suggested content to be one of the supported languages. The default language is set to English.

1. Generate the suggested reply using an appropriate response category.

1. Select **Adjust draft**.

1. Under **Draft language**, select the language you want to use and then select **Update**.

1. Review the suggested content.

    To generate a different suggestion, select **More options**, and then select **Try again**.

    [Refine the suggested content](#refine-suggested-content), if required. You can also [restore the suggested content](#restore-suggested-content) to the previous version.

1. Select **Add to email** to paste the content in the email body or **Copy content** when you are reading an email.

   > [!NOTE]
   > Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

1. Edit the email content as required, and then send it.

## Create a sales meeting summary email (preview)

> [!IMPORTANT]
> This feature is currently available only for public preview and is subject to change.

After meeting with your customers, you often send an email with a summary of your interaction, relevant action items or next steps, and a follow-up date. Manually creating a meeting summary and compiling all the notes and action items taken during the meeting takes some amount of time and often gets missed.

With Sales Copilot, you can summarize your most recent transcribed Teams meeting with your sales contacts and send it over email whenever you compose a new email or reply to your customer's email.

> [!IMPORTANT]
> Ensure that Sales Copilot app is installed, and meeting is transcribed to generate a meeting summary. More information: [Generate a meeting summary](generate-meeting-summary.md)

1. In Outlook:

    - Open the meeting in Outlook and select **Contact Attendees** > **Reply to All with Email** under the **Meetings** tab. In the message at the top of the draft email, select **Use Copilot now**.

    - When you're composing a new email, open the Sales Copilot pane or select **Use Copilot now** in the banner message at the top of the email.

1. On the **Highlights** tab, details such as meeting name and time of the most recent transcribed Teams meeting are displayed in the **Summarize a sales meeting** button. Select the button to create a summary.

   :::image type="content" source="media/summarize-meeting.png" alt-text="Screenshot showing the Summarize meeting option.":::

   To select another meeting to summarize, select the down arrow to see up to five recently transcribed meetings. Select a meeting to create a summary.

   :::image type="content" source="media/select-meeting.png" alt-text="Screenshot showing where to select a meeting to summarize.":::

1. Review the suggested content.

    To generate a different suggestion, select **More options**, and then select **Try again**.

    If required, [change the meeting that is used to create the summary](#change-the-meeting-used-to-create-a-summary-preview).

1. Select **Add to email** to paste the content in the email body.

   :::image type="content" source="media/summary.png" alt-text="Screenshot showing the summarized meeting content.":::

   > [!NOTE]
   > Existing content in the email body is not replaced. The suggested content is prepended to any existing content in the email body.

1. Edit the email content as required, and then send it.

## Change the meeting used to create a summary (preview)

> [!IMPORTANT]
> This feature is currently available only for public preview and is subject to change.

You can choose from the recent recorded Teams meetings that you had with sales contacts on an email.

1. In the message at the bottom of the suggested content, select **Change**.

   :::image type="content" source="media/change-meeting.png" alt-text="Screenshot showing the Change meeting option.":::

1. Under **Select a meeting to summarize**, select the meeting that you want to summarize in the generated content.

   > [!TIP]
   > You can hover over a meeting and select :::image type="icon" source="media/open-record.png" border="false"::: to open the meeting summary in Teams.

   :::image type="content" source="media/summarize.png" alt-text="Screenshot showing the Select a meeting to summarize pane.":::

1. Select **Create a new draft**.

   New content is generated based on the selected meeting.

## Share feedback

If you have any feedback about the suggested content, you can share it by selecting the appropriate icon at the bottom of each suggestion. Your feedback is valuable, and we use it to improve the functionality.

> [!NOTE]
> Ensure that you don't enter any personal information while sharing feedback.

1. At the bottom of the suggested content, select :::image type="icon" source="media/thumbs-up.png" border="false"::: or :::image type="icon" source="media/thumbs-down.png" border="false":::.

   After you select an icon, you'll get a **Tell us more** link.

1. Select the link to open the feedback form.

1. Enter your responses in the feedback form and then select **Send**.

## Text moderation

Text moderation uses machine-assisted classification to help detect potentially inappropriate   content  and reject it when you use custom prompt to generated suggested content or refine the already generated suggested content. It conveys the likelihood of each category. The feature uses a trained model to identify possible abusive, derogatory, or discriminatory language. This includes slang, abbreviated words, offensive, and intentionally misspelled words.

If you enter text that contains undesired or inappropriate content (potential presence of language that may be considered sexually explicit, suggestive, adult, or offensive), the suggested content is not generated, and an error message is displayed.

## How is suggested content generated?

Sales Copilot uses AI to generate suggested email content. Trained on a vast number of text samples from the Internet, Copilot generates new content that looks and sounds like it was written by a person.

Original content is generated every time, but it isn't always factual. In addition, the underlying technology uses AI that has been trained on a wide range of internet sources. Some suggestions may include questionable or inappropriate content. It's your responsibility to edit generated suggestions so that your reply is accurate and appropriate.

## What data is collected to suggest email replies?

When you open the Sales Copilot pane while you're reading or replying to an email, the AI considers the following information to generate a response:

- The contacts, subject, and body of the email

- CRM data connected through Sales Copilot

- The response category you selected or custom prompt you entered

If the email contact doesn't match a contact in the CRM, no CRM data is sent to the AI engine.
