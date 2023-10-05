---
title: Sales Copilot FAQ
description: Sales Copilot Frequently Asked Questions
ms.date: 09/12/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Sales Copilot FAQ

We've compiled a list of frequently asked questions and provided brief answers to help you get the required information quickly.

## In which regions is Sales Copilot supported?

Sales Copilot is available globally except in these countries: Myanmar, Cabo Verde, China, Cuba, Curaçao, Timor-Leste, Iran, Côte d'Ivoire, North Korea, Palestinian Authority, Russia, St Helena, Ascension, Tristan da Cunha, and Syria.

## In which languages is Sales Copilot supported?

Sales Copilot user interface is supported in Arabic, Chinese (simplified), Chinese (traditional), Czech, Danish, Dutch, English, Finnish, French, German, Greek, Hebrew, Indonesian, Italian, Japanese, Korean, Norwegian, Polish, Portuguese (Brazil), Portuguese (Portugal), Spanish, Swedish, Thai, and Turkish.

> [!NOTE]
> Extracting contact details from email signature is available only for emails in English.

## In which languages is Sales Copilot conversation intelligence supported?

Conversation intelligence is supported in the following languages: Chinese Simplified (PRC), Dutch, English, French, German, Italian, Japanese, Portuguese, Portuguese (Brazil), Spanish, Hebrew, Danish, Swedish, Finnish, Norwegian, and Arabic.

## Who can install Sales Copilot?

Microsoft 365 administrators can install Sales Copilot and assign users/security groups to use it.

## Is there any license required to use Sales Copilot?

Sales Copilot may be subject to an additional free or paid license. For more details, see [Microsoft Viva plans and pricing](https://www.microsoft.com/microsoft-viva/pricing) and [Dynamics 365 Sale pricing](https://dynamics.microsoft.com/pricing/#Sales), or contact your Microsoft representative.

## Does Sales Copilot require CRM connectivity?

Yes, Sales Copilot requires connectivity to a CRM.

## Which CRMs work with Sales Copilot?

Currently, Sales Copilot will work with Dynamics 365 Sales and Salesforce CRMs.

## What privileges are required to use Sales Copilot?

Sales Copilot applies your organization's existing CRM access controls and user permissions. More information: [Privileges required to use Sales Copilot](install-viva-sales.md#privileges-required-to-use-sales-copilot).

## I don't see the Add to email button and instead only the Copy text button in the suggested content feature.

The Sales Copilot for Outlook add-in must be updated to the latest version (10.0.0.11 or newer) to use the copy to email functionality of the suggested reply feature. Ask you administrator to update the Sales Copilot for Outlook add-in. More information: [Update the Sales Copilot add-in](install-viva-sales-as-an-integrated-app.md#update-the-sales-copilot-add-in).

## I don't see an email summary when opening an email conversation.

Email summary is generated only for emails or email threads with more than 1000 characters, which is about 180 words.

## I don't see the Summarize a sales meeting button when creating a sales meeting summary email.

The **Summarize a sales meeting** button is not available in the following scenarios:

- There are no meetings transcribed.

- Meetings are filtered as per the recipients entered in the **To** list. If there are no meetings transcribed with the people in the **To** list, a message is displayed conveying the same.

- Due to network or connection error. Try closing and reopening the Sales Copilot pane.

For information on how to transcribe a meeting, see [Generate a meeting summary.](generate-meeting-summary.md)

## With which Salesforce Editions does Sales Copilot work?

Sales Copilot works with Professional (with API access enabled), Enterprise, Performance, Unlimited, and Developer Editions.

## Is Sales Copilot available for Dynamics 365 or Microsoft Exchange on premise?

Sales Copilot is not available for Dynamics 365 or Microsoft Exchange on premise.

## Does Sales Copilot work for Power Apps or Dataverse customers without Dynamics 365 licenses?

Sales Copilot works for Microsoft 365 customers with an eligible license and a CRM login (Dynamics 365 or Salesforce).

## Does Sales Copilot work in incognito mode?

When you use the Sales Copilot app in incognito mode or you have disabled third-party cookies, the following message is displayed:

:::image type="content" source="media/incognito.png" alt-text="Screenshot showing message in incognito mode.":::

When you search for a record in Sales Copilot pane in Outlook, the record type filter might not work properly.

This is normal behavior. The reason for this is that Sales Copilot uses cookies to save data to local storage. In incognito mode or when third-party cookies are disabled, access to local storage is blocked.

To get full benefit of all features in Sales Copilot, browse in normal mode and allow Microsoft domain in third-party cookie settings.

For information about how to allow third-party cookies, see:

- [Enable cookies in Edge](https://support.microsoft.com/office/enable-cookies-6b018d22-1d24-43d9-8543-3d35ddb2cb52)

- [Clear, allow & manage cookies in Chrome](https://support.google.com/chrome/answer/95647)

- [Enable cookies in Safari](https://support.apple.com/guide/safari/ibrw850f6c51/mac)

## How can I add the Sales Copilot app manually to a Teams meeting?

You can add the Sales Copilot app manually to a Teams meeting to test it internally before scheduling a call with your customer.

- To add an app before a meeting, first send the meeting invite then open the meeting. Select **Add a tab **(**+**), search for Sales Copilot, and then select it.

    :::image type="content" source="media/add-before-meeting.png" alt-text="Screenshot showing add Viva Sales app before meeting.":::

- To add an app during a meeting, after the meeting starts select **Add an app** (**+**), search for Sales Copilot, and then select it.

    :::image type="content" source="media/add-during-meeting.png" alt-text="Screenshot showing add Viva Sales app during meeting.":::

## What's the minimum version of Outlook required for Sales Copilot?

The minimum required version for Outlook is:

- **Outlook for Windows**: version 2206 (Build 15330.20196)

- **Outlook for Mac**: 16.78

## Why are meeting insights not getting generated even if meeting is transcribed?

Meeting insights are generated only if version of the Sales Copilot app in Microsoft Teams is 1.0.9 or higher. To check your app's version:

1. Open Microsoft Teams and select **Sales Copilot** in the navigation bar on the left.

1. In the Sales Copilot app, go to the **About** tab and check the version.

If the Sales Copilot app for Teams is installed by your administrator, you must contact your administrator to update the app to the latest version.

If you've installed Sales Copilot app for Teams by yourself, you can update it to the latest version by following the instructions [here](https://support.microsoft.com/office/update-an-app-3d53d136-5c5d-4dfa-9602-01e6fdd8015b).

## How many hours of conversation intelligence are available with Sales Copilot?

You get unlimited call recording and processing hours with Sales Copilot.

## How can I provide feedback about Sales Copilot?

You can go to the [feedback portal](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) to suggest a feature. You can also join the [Tech Community](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) forum to interact with the product team and other users of Sales Copilot.
