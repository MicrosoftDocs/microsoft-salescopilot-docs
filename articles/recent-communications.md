---
title: View recent communications in Copilot for Sales
description: Explore Copilot for Sales' new feature allowing users to view recent communications, including emails and Teams meetings, with external contacts.
ms.date: 06/17/2024
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

If you've interacted with a customer recently using Outlook or Teams, you can view your recent email threads and Teams meetings with the first external contact in the **Recent communications** card in the Copilot for Sales pane in Outlook. You can get AI-based summaries of past email conversations, open the email thread in Outlook, and open the meeting chat in Teams. With this capability, you can quickly catch up on the the customer context and move deals forward with informed responses.

You can see up to three email threads and three Teams meetings in the last 30 days with the first external contact. The first external contact is the first contact in the email thread who isn't from your organization. It is determined based on the email address as follows:

|Outlook item|Read mode|Compose mode|
|---|---|---|
|Emails|Sender + To + Cc|To + Cc|
|Meetings|Organizer + Required + Optional|Required + Optional|

The **Recent communications** card retrieves the following communications from Graph:
- Communications from the external contact to you 
- Communications from you to the external contact 
- Communications from others to the external contact that include you 

> [!NOTE]
> - The **Recent communications** card shows previous email threads, not the previous responses in the current email thread.
> - The **Recent communications** card shows meetings that include a Teams meeting link. Meetings without a Teams meeting link aren't shown in the card.

## License requirements

- [Microsoft Copilot for Sales (premium)](https://www.microsoft.com/ai/microsoft-sales-copilot#featuresandpricing)

## Email summary - supported languages

The email must be in one of the [supported languages](supported-languages.md#ai-in-copilot-for-sales) to generate the summarized email thread.

## Email summary – supported length 

Email summary will be generated only for emails or email threads with more than 1000 characters, which is about 180 words.

## View recent communications

1. [Open the Copilot for Sales side pane in Outlook](open-app.md#access-copilot-for-sales-in-outlook).

1. Go to the **Recent communications** card.

    By default, the card shows one previous email thread and one Teams meeting related to the first external contact, if any existed in the last 30 days. To see up to three email threads and three Teams meetings in the last 30 days, select **See all**.

    `image with see all button`

1. To generate a summary of the email thread, select **Summarize**.

    `image with email summary`

1. To open the email thread in Outlook, select **Open email**.

1. To open the meeting chat in Teams, select **Open meeting chat**.

    
