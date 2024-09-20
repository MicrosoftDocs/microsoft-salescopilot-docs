---
title: View recent communication in Copilot for Sales
description: Explore the new Copilot for Sales feature that you can use to view recent communication (emails and Teams meetings) with external contacts.
ms.date: 08/19/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:06/13/2024
---

# View recent communication in Copilot for Sales

If you recently used Outlook or Teams to interact with a customer, the **Recent communication** card in the Copilot for Sales pane in Outlook shows your recent email threads and Teams meetings with that customer. From the card, you can get AI-generated summaries of the email threads and navigate to AI-generated meeting recaps in Teams. You can also open the email threads and meeting invitations in Outlook. Therefore, you can quickly catch up on the customer context and move deals forward through informed responses.

Information on the **Recent communication** card is shown in the context of the email or meeting that is opened in Outlook. You can view up to the three most recent email threads and the three most recent Teams meetings that you had with the first external contact in the open email or meeting during the last 30 days. (The first external contact is the first contact in the email or meeting who isn't from your organization.) Depending on whether the email or meeting was opened in read or compose mode, the first external contact is selected from the following email addresses.

| Outlook item | Read mode | Compose mode |
|---|---|---|
| Email | Sender + To + Cc | To + Cc |
| Meeting | Organizer + Required + Optional | Required + Optional |

The **Recent communications** card retrieves the following communications from Microsoft Graph:

- Communications from the external contact to you
- Communications from you to the external contact
- Communications from others to the external contact that include you

> [!NOTE]
> - The **Recent communication** card shows the most recent email threads that differ from the current thread. It doesn't show previous responses from the current email thread.
> - The **Recent communication** card shows only meetings that include a Teams meeting link.
> - If there were no email threads or Teams meetings with the first external contact during the last 30 days, the **Recent communication** card isn't shown.
> - The option to see a meeting recap is available only if the Teams meeting was recorded and you have access to the recording.

## License requirements

- [Microsoft 365 Copilot for Sales](https://www.microsoft.com/en-us/microsoft-365/copilot/copilot-for-sales#Pricing)

## Prerequisites

- [Copilot AI features must be turned on in your environment.](suggested-replies.md)

## Supported languages and length for email summarization

This feature includes the capability to summarize email threads. A summary of an email thread can be generated only if the email is in one of the [supported languages](supported-languages.md#ai-in-copilot-for-sales). A summary is generated only for emails or email threads that have more than 1,000 characters (that is, more than about 180 words).

## View recent communication

1. In Outlook, [open the Copilot for Sales side pane](open-app.md#access-copilot-for-sales-in-outlook).
1. Go to the **Recent communication** card.

    By default, the card shows the most recent email thread and Teams meeting that involve the first external contact, if there were any during the last 30 days. To view up to three email threads and three Teams meetings from the last 30 days, select **See all**.

    :::image type="content" source="media/recent-comms-card.png" alt-text="Screenshot showing the most recent email thread and Teams meeting on the Recent communication card.":::

1. Follow these steps to work with the email threads and Teams meetings on the **Recent communication** card: 

    - To open an email thread or a meeting invitation in Outlook, select its name.
    - To generate a summary of the email thread, select **Summarize**. The email summary is shown on the **Email summary** card.

        :::image type="content" source="media/recent-comms-email-summary.png" alt-text="Screenshot showing email summary opened from the Recent communication card.":::

    - To view the recap of a Teams meeting, select **View recap**. You are navigated to the [meeting recap in Teams](view-meeting-summary-recap.md).
