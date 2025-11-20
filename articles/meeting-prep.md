---
title: View a meeting preparation card
description: Learn how to view a meeting preparation card in Teams.
ms.date: 11/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom: CXT
---

# Meeting preparation card

The meeting preparation card provides the latest information and out-of-the-box insights about the opportunities derived from your past customer interactions such as emails and meetings as well as CRM. This card helps you stay informed and prepared before walking into a customer meeting. It shows general information about the meeting, opportunity info, recent communication and strategic insights. You can use this information to prepare for the upcoming meeting accordingly and have a productive discussion.

:::image type="content" source="media/meeting-prep-card.png" alt-text="Screenshot showing meeting preparation card.":::

## Prerequisites

- [Connect to a CRM organization in the Sales app](sign-in-crm-outlook.md).
- If you're using Salesforce as your CRM, [turn on the server-to-server connection](connect-agent-datasource.md).
- [Invite at least one external contact that is saved in CRM to the meeting](connect-contact.md).

## View a meeting preparation card

The meeting preparation card is displayed in your personal chat with the **Sales** bot or in the **Chat** tab of the Sales personal app in Teams. The meeting preparation card is sent at a time that is [configured by your administrator](configure-meeting-agent.md#configure-pre-meeting-preparation-notifications). By default, the meeting preparation card is sent one hour before the meeting. If you schedule the meeting less than an hour before the start time, the card appears soon after you send the meeting invite. 

> [!NOTE]
> The meeting preparation card is displayed in the language set for your Microsoft 365 account. To change the language of the meeting preparation card to your preferred language, change the display language in your [Microsoft account settings](https://myaccount.microsoft.com/settingsandprivacy/language).

The meeting preparation card contains the following information: 

- **Matched account**: Title of the card shows the name of the account matched in CRM. 
- **General meeting information**: Information about the meeting such as its name, date, time, number of participants, and their acceptance status.
- **Opportunity**: Name of the matched opportunity, key fields as configured by your administrator, and AI-generated summary of key CRM information such as open and closed dates, current stage, budget, related records, and open tasks retrieved from CRM. If the meeing is saved to a CRM opportunity, the connected opportunity is used to generate the insights. If the meeting is not saved to a CRM opportunity, the most recent opportunity linked to the meeting participants is used to generate the insights. If no opportunity is found, the card displays the matched account summary instead.

    :::image type="content" source="media/meeting-prep-card-oppty.png" alt-text="Screenshot showing opportunity summary in meeting preparation card":::

- **Recent communication**: Displays up to 10 most recent meetings or emails on the opportunity. In addition to the meetings you organized or participated in, it may also include meetings conducted by other team members for the same opportunity. In this way, you can have a complete view of the past customer interactions. It shows AI-generated summary of the past meetings and AI-generated insights per individual meeting such as key discussion points or key objections raised by the customer. Meetings without AI-generated insights may also be shown in the list, such as meetings that were not recorded or the Sales app was not added to the meetings. 

    :::image type="content" source="media/meeting-prep-card-recent-comm.png" alt-text="Screenshot showing recent communications in meeting preparation card":::

- **Strategic insights**: Shows key contacts of the opportunity in CRM among the meeting participants, key risks identified and their summary from all past interactions, and the next follow-up action items agreed with the customer. This section is displayed only if the AI-generated insights are available. 

    :::image type="content" source="media/meeting-prep-card-insights.png" alt-text="Screenshot showing strategic insights in meeting preparation card":::  

## How does the card work?

The AI-generated insights displayed on the meeting preparation card are based on opportunities identified and matched with meeting participants who are recognized as contacts in your CRM. If there are multiple meeting participants who are contacts, the Sales app uses the Microsoft Graph API to determine the order and prioritizes the first contact returned with most recent modification in CRM to locate linked opportunities in CRM. When multiple opportunities are linked with this contact, the most recent one is selected for display on the card. After identifying the relevant opportunity, the Sales app pulls the emails and meetings saved in CRM that are linked to this opportunity, and uses AI-powered soft-linking to scan and match the other unsaved meetings related to this opportunity, including meetings organized by other team members, such as peer sellers. The system then generates a summary of all matched past meetings, providing synthesized insights into key risks and upcoming actions. Insights are presented in your supported local language and your local time zone. 

> [!NOTE]
> You must check the AI-generated content carefully because it can have mistakes. It's your responsibility to review the AI-generated content to make sure it's accurate and appropriate.

## Key fallback scenarios

It might happen that appropriate data is not available to generate the required insights. Here are some common fallback scenarios:

- When an opportunity is matched with the meeting participant as a CRM contact but no past meeting is detected regarding this opportunity, the card displays:
    - General information about the meeting
    - Opportunity summary
    - Up to 10 recent emails or meetings with the contact
- When an opportunity is not available in CRM or no matched opportunity is found, but there's a matched account, the card displays:
    - General information about the meeting
    - Matched account summary
    - Up to 10 recent emails or meetings with the contact
- When the meeting participant is not a CRM contact, the card displays:
    - General information about the meeting
    - Up to 10 recent emails or meetings with the participant

## Limitations

- The meeting preparation card does not appear for recurring meetings.
- The card is sent only after the meeting is initially scheduled. If you make changes to the meeting after it's scheduled, no new card is generated.
- Only past meetings have insights generated. Email insights are not included currently.
- Meeting insights are linked only to one opportunity in CRM. 

## Data storage and retention

Insights generated from the customer meetings such as recap, customer objections, and questions are stored in Dataverse. The meeting preparation card is generated using this data. The data is retained for 90 days and then deleted. Insights of a meeting are accessible to those who attended the meeting and to those who have access to the opportunity in CRM. 

## Meeting sensitivity labels

Currently, meetings with all types of sensitivity labels are included to generate insights. If you have any concerns, contact Microsoft support. Learn more about [sensitivity labels in Teams](https://support.microsoft.com/en-us/office/sensitivity-labels-for-teams-meetings-2b244d1d-72d0-471e-8e58-c41079e190fb).
