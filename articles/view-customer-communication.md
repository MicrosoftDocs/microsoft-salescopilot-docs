---
title: View customer communication (preview)
description: Learn how to work with the Customer communication card in the Sales agent
ms.date: 07/24/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# View customer communication (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

The **Customer communication** card shows a chronological view of your interactions with a customer, including emails and meetings. This card helps you catch up and gain insights into all the activities that happened for a given opportunity. You can see all the emails and meetings related to the opportunity. For each email and meeting, the Sales agent provides AI-generated insights such as the summary, sentiment, objections, and next steps.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

When working on opportunities, you often manage numerous activities, such as emails and meetings, making it difficult to keep track of every interaction and discussion. The **Customer communication** card consolidates all these events and provides insights for each one directly within Outlook. If you have access to an opportunity in CRM, you can view insights from related emails and meetings, even if you didn't attend the meetings. This feature helps you stay updated and informed without leaving your workflow.

## Where to see the Customer communication card

You can see **Customer communication** card in the following places:

- **Sales** pane in Outlook when you open an email or a meeting.
- Detailed meeting preparation view in [Sales agent in Microsoft 365 Copilot](use-sales-chat.md#prepare-for-and-follow-up-on-your-sales-meetings).

> [!NOTE]
> - When you're viewing an email, the **Customer communication** card appears only when the email is connected to an opportunity. Once the opportunity is connected, the **Customer communication** card displays the emails and meetings related to that opportunity.
> - When you're viewing a meeting in Outlook calendar, the **Customer communication** card is displayed only when the meeting is connected to an opportunity.
> - Email insights are available for up to 90 days and appear only when the email meets the following criteria:
>   - The email has at least one external contact that is a CRM contact.
>   - [Server-to-server (S2S) connection is turned on](connect-agent-datasource.md#set-up-server-to-server-connection-to-salesforce).
>   - [Email insights are turned on](access-settings.md#email-insights-preview).
>   - The email's sensitivity label matches the labels configured by your administrator.

## Prerequisites

- [Turn on meeting insights in Access settings](access-settings.md#meeting-insights).
- [Turn on email insights in Access settings](access-settings.md#email-insights-preview).
- If you're a Salesforce user, [server-to-server connection must be set up](connect-agent-datasource.md#set-up-server-to-server-connection-to-salesforce).

## Access the Customer communication card in Outlook

1. In Outlook, open an email or a meeting.
1. [Open the Sales agent](open-app.md#access-sales-agent-in-outlook).
1. Go to the **Customer communication** card.
1. To view insights for an email, select **View email insights**.
1. To view insights for a meeting, select **View meeting insights**.

    :::image type="content" source="media/customer-communication.png" alt-text="Screenshot of the Customer communication card":::

## Access the Customer communication card in Sales agent in Microsoft 365 Copilot

1. [Access Sales agent in Microsoft 365 Copilot](use-sales-chat.md#access-sales-agent).
1. In the [meeting preparation card](use-sales-chat.md#prepare-for-and-follow-up-on-your-sales-meetings), select **Prepare with insights**, and then go to the **Customer communication** section.

## Related information

- [Save Outlook activities to your CRM](save-outlook-activities-crm.md)
- [Configure access settings for features in the Sales agent](access-settings.md)