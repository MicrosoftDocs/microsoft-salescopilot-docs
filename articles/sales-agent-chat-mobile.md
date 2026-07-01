---
title: Sales agent chat on mobile
description: Learn about using Sales agent chat on mobile. Launch the app, capture voice notes, update opportunities with voice commands, save to CRM records, and prepare for meetings on your mobile device.
ms.date: 07/01/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# Sales agent chat on mobile

Sales agent chat is available on mobile through Outlook mobile and the standalone Microsoft 365 Copilot app. Use it to search and update CRM records, summarize emails, draft responses, and capture notes—all from your mobile device.

## Launch Sales agent on mobile

You can open Sales agent from either Outlook mobile or the Microsoft 365 Copilot app.

### From Outlook mobile

1. Open Outlook on your mobile device and tap the **Copilot** icon.
1. Tap the hamburger menu on the top left, and then select **Sales**.

### From the Microsoft 365 Copilot app

1. Open the Microsoft 365 Copilot app on your mobile device.
1. Tap the hamburger menu on the top left, and then select **Sales**.

## Capture voice notes and save to CRM records

Capture voice notes in Sales agent and save them directly to your CRM records. This is useful when you want to log call notes, meeting takeaways, or account updates while on the go without typing.

You can capture voice notes using your device's keyboard dictation in Outlook mobile or the built-in mic icon in the Microsoft 365 Copilot app. When dictating, tell the Sales agent that you want to add a note as part of your message—for example, start with "I want to add a note to my Fabrikam opportunity" and then dictate your note.

> [!NOTE]
> This feature is available on both iOS and Android.

### Capture voice notes in Outlook mobile and Microsoft 365 Copilot app

1. Open the Sales agent in [Outlook mobile](#from-outlook-mobile) or the [Microsoft 365 Copilot app](#from-the-microsoft-365-copilot-app) and tap the message input box to bring up the keyboard.
1. On your keyboard, select the microphone key and speak your note. Start by stating your intent—for example, "I want to add a note to my Fabrikam opportunity"—followed by the note details.
   The dictated text appears in the message input box as you speak.
1. Review the transcribed text and make any edits if needed.
1. Send the message to the Sales agent.
1. When prompted, select the CRM record where you want to save the note, and then confirm.

## Summarize emails with CRM insights

Use Sales agent chat to summarize emails and view related CRM insights in one place. This helps you quickly understand conversation context, account activity, and next best actions without switching apps. You can also ask follow-up questions in chat to get more details from Sales agent and your CRM data.

1. In Outlook mobile, open an email, and then [open Sales agent](#from-outlook-mobile).
1. Enter a prompt in the Sales agent chat to summarize the email. For example, "Summarize this email and show me related CRM insights."

    The Sales agent generates a summary of the email and related sales insights.

1. Ask follow-up questions in chat to get more detail from Sales agent and your CRM data.

## Prepare for your meetings on the go

You can prepare for upcoming meetings and review recaps from past meetings directly in Sales agent on mobile.

On the Sales agent home screen, swipe left to open your meetings list.

- Under **Prepare for upcoming meetings**, tap any meeting to open the [detailed meeting preparation view](meeting-prep.md#detailed-meeting-preparation-view) with details such as highlights, CRM record summary, and AI-generated insights.
- Under **Recap past meetings**, tap any meeting to open its recap. The recap includes meeting information such as the meeting title, time, and a direct link to open the recap in Teams. It also displays **Key takeaways** that summarize the most important meeting outcomes.

## Update opportunities with voice

Update your opportunities directly from the Sales agent using voice commands. Simply state the specific update you want to make in an opportunity, and the Sales agent will identify the target opportunity, confirm the change with you, and save the update to your CRM.

> [!NOTE]
> Voice commands can update Opportunity fields of the following data types only: String, DateTime, Money, Integer, Decimal, Double, and Picklist.

### How it works

1. State your update clearly—for example, "Update the closing date for Contoso to next Friday" or "Change the deal amount for Fabrikam to $50,000".
1. The Sales agent identifies the opportunity based on your context. If multiple opportunities match your input, the Sales agent asks you to clarify which one.
1. The Sales agent proposes the change and displays the details for your review.
1. Review the proposed update, including the field name and new value.
1. Approve the change to save it to your CRM, or make corrections if needed.

### Capabilities

- **Single-field updates**: Update one field at a time, such as opportunity closing date or deal amount.
- **Multi-field updates**: Update multiple fields in a single conversation.
- **Mid-flow correction**: Correct or revise your input at any point before confirming the change.
- **Opportunity and field disambiguation**: Resolve ambiguity when your input matches multiple opportunities or fields through a guided clarification flow.

> [!IMPORTANT]
> Confirmation is required before any update is saved to your CRM.

## Related information

- [Prepare for meetings](meeting-prep.md)
- [Use Sales agent chat capabilities](use-sales-chat.md)