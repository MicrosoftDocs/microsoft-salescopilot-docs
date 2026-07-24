---
title: View opportunity insights (preview)
description: Learn how to view opportunity insights in the Sales agent.
ms.date: 07/24/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# View opportunity insights (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

The **Opportunity insights** card provides a consolidated view of opportunity-related emails and meetings. It highlights risks and upcoming actions to help you stay updated without leaving Outlook. The card offers a detailed perspective on the opportunity by analyzing all related emails and meetings. It helps you understand potential risks and progress. For an opportunity, the Sales agent provides AI-generated insights to indicate how the opportunity is evolving.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

When you work on opportunities, you often juggle multiple activities, making it challenging to keep track of key insights from each interaction. The **Opportunity insights** card brings together all these events and surfaces opportunity-level insights directly within Outlook. If you have access to an opportunity in CRM, you can see insights from all relevant emails and meetings, even those you didn't attend. This feature helps you stay updated and informed without leaving your workflow.

## Where to see the Opportunity insights card

You can see the **Opportunity insights** card in the **Sales** pane in Outlook when you open an email or a meeting.

> [!NOTE]
> - When you view an email, the **Opportunity insights** card appears only when the email is connected to an opportunity. Once the opportunity is connected, the card displays insights from all relevant emails and meetings.
> - When you're viewing a meeting in Outlook calendar, the **Opportunity insights** card is displayed only when the meeting is connected to an opportunity.
> - Email insights are available for up to 90 days and appear only when the email meets the following criteria:
>   - The email has at least one external contact that is a CRM contact.
>   - [Server-to-server (S2S) connection is turned on](connect-agent-datasource.md#set-up-server-to-server-connection-to-salesforce).
>   - [Email insights are turned on](access-settings.md#email-insights-preview).
>   - The email's sensitivity label matches the labels configured by your administrator.

## Prerequisites

- [Meeting insights must be turned on in Access settings](access-settings.md#meeting-insights).
- [Email insights must be turned on in Access settings](access-settings.md#email-insights-preview).
- [Email insights sharing must be turned on](email-insights-settings.md#configure-email-insights-sharing-settings).

## Access the Opportunity insights card

1. In Outlook, open an email or a meeting.
1. [Open the Sales side pane](open-app.md#access-sales-agent-in-outlook).
1. Go to the **Opportunity insights** card.
1. Select **See all risks and insights for this opportunity** to view detailed information.

    :::image type="content" source="media/opportunity-insights.png" alt-text="Screenshot of the Opportunity insights card":::

## Related information

- [Save Outlook activities to your CRM](save-outlook-activities-crm.md)
- [Configure access settings for features in the Sales agent](access-settings.md)