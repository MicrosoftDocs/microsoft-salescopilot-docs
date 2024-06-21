---
title: View recent communications in Copilot for Sales
description: Explore Copilot for Sales' new feature allowing users to view recent communications, including emails and Teams meetings, with external contacts.
ms.date: 06/21/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:06/13/2024
---

# View recent communications in Copilot for Sales

If you've interacted with a customer recently using Outlook or Teams, you can view your recent email threads and Teams meetings with the customer in the **Recent communications** card in the Copilot for Sales pane in Outlook. You can get AI-based summaries of past email conversations and open the email thread and meeting invitation in Outlook. With this capability, you can quickly catch up on the customer context and move deals forward with informed responses.

Information in the **Recent communications** card is displayed in the context of the email or meeting opened in Outlook. You can see up to three most recent email threads and Teams meetings in the last 30 days with the first external contact in the email or meeting. The first external contact is the first contact in the email or meeting who isn't from your organization. Depending on whether the email or meeting is opened in the read or compose mode, the first external contact is picked from below list of email addresses:

|Outlook item|Read mode|Compose mode|
|---|---|---|
|Emails|Sender + To + Cc|To + Cc|
|Meetings|Organizer + Required + Optional|Required + Optional|

The **Recent communications** card retrieves the following communications from Graph:
- Communications from the external contact to you 
- Communications from you to the external contact 
- Communications from others to the external contact that include you 

> [!NOTE]
> - The **Recent communications** card shows most recent email threads that are different from the current thread. It does not show previous responses in the current email thread.
> - The **Recent communications** card shows meetings that include a Teams meeting link. Meetings without a Teams meeting link aren't shown in the card.
> - If there are no recent email threads or Teams meetings with the first external contact in the last 30 days, the **Recent communications** card is not displayed.
> - Recurring meetings are not shown in the **Recent communications** card. However, the card shows the first instance of the recurring meeting if it's within the last 30 days.

## License requirements

- [Microsoft Copilot for Sales (premium)](https://www.microsoft.com/ai/microsoft-sales-copilot#featuresandpricing)

## Prerequisites

- [Copilot AI features must be turned on in your environment](suggested-replies.md)

## Supported languages and length for email summarization

This feature includes a capability to summarize email threads. The email must be in one of the [supported languages](supported-languages.md#ai-in-copilot-for-sales) to generate the summarized email thread. Email summary is generated only for emails or email threads with more than 1,000 characters, which is about 180 words.

## View recent communications

1. [Open the Copilot for Sales side pane in Outlook](open-app.md#access-copilot-for-sales-in-outlook).

1. Go to the **Recent communications** card.

    By default, the card shows the most recent email thread and Teams meeting involving the first external contact, if any existed in the last 30 days. To see up to three email threads and three Teams meetings in the last 30 days, select **See all**.

    :::image type="content" source="media/recent-comms-card.png" alt-text="Screenshot showing the Recent communications card.":::

1. To open the email thread in Outlook, select **Open email**.

1. To open the meeting invitation in Outlook, select **Open meeting**.

1. To generate a summary of the email thread, select **Summarize**. The email summary is displayed in the **Email summary** card.

    :::image type="content" source="media/recent-comms-email-summary.png" alt-text="Screenshot showing email summary opened from the Recent communications card.":::
    
