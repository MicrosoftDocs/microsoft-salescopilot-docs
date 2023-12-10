---
title: Microsoft Copilot for Sales FAQ
description: Copilot for Sales Frequently Asked Questions
ms.date: 12/11/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Microsoft Copilot for Sales FAQ

We've compiled a list of frequently asked questions and provided brief answers to help you get the required information quickly.

## In which regions is Copilot for Sales supported?

Region availability of Copilot for Sales is listed [here](introduction.md#region-availability).

## In which languages is Copilot for Sales supported?

You can find the list of supported languages for Copilot for Sales in Outlook and Teams [here](supported-languages.md).

## Who can install Copilot for Sales?

Microsoft 365 administrators can install Copilot for Sales and assign users/security groups to use it.

## Is there any license required to use Copilot for Sales?

Copilot for Sales may be subject to an additional free or paid license. For more information, see [Microsoft Copilot for Sales pricing](https://www.microsoft.com/ai/microsoft-sales-copilot#featuresandpricing) and [Dynamics 365 Sales pricing](https://dynamics.microsoft.com/pricing/#Sales), or contact your Microsoft representative.

## Does Copilot for Sales require CRM connectivity?

Yes, Copilot for Sales requires connectivity to a CRM.

## Which CRMs work with Copilot for Sales?

Currently, Copilot for Sales will work with Dynamics 365 Sales and Salesforce CRMs.

## What privileges are required to use Copilot for Sales?

Copilot for Sales applies your organization's existing CRM access controls and user permissions. More information: [Privileges required to use Copilot for Sales](install-viva-sales.md#privileges-required-to-use-copilot-for-sales).

## I don't see the Add to email button and instead only the Copy content button in the suggested content feature.

The Copilot for Sales for Outlook add-in must be updated to the latest version (10.0.0.11 or newer) to use the add to email functionality of the suggested content feature. Ask your administrator to update the Copilot for Sales for Outlook add-in. More information: [Update the Copilot for Sales add-in](install-viva-sales-as-an-integrated-app.md#update-the-copilot-for-sales-add-in).

Note that the **Add to email** button is displayed only when you use copilot while composing an email. When you use copilot while reading an email, the **Copy content** button is displayed.

## I don't see an email summary when opening an email conversation.

Email summary is generated only for emails or email threads with more than 1000 characters, which is about 180 words.

## I don't see the Summarize a sales meeting button when creating a sales meeting summary email.

The **Summarize a sales meeting** button is not available in the following scenarios:

- There are no meetings transcribed.

- Meetings are filtered as per the recipients entered in the **To** list. If there are no meetings transcribed with the people in the **To** list, a message is displayed conveying the same.

- Due to network or connection error. Try closing and reopening the Copilot for Sales pane.

For information on how to transcribe a meeting, see [Generate a meeting summary.](generate-meeting-summary.md)

## With which Salesforce Editions does Copilot for Sales work?

Copilot for Sales works with Professional (with API access enabled), Enterprise, Performance, Unlimited, and Developer Editions.

## Is Copilot for Sales available for Dynamics 365 or Microsoft Exchange on premise?

Copilot for Sales is not available for Dynamics 365 or Microsoft Exchange on premise.

## Does Copilot for Sales work for Power Apps or Dataverse customers without Dynamics 365 licenses?

Copilot for Sales works for Microsoft 365 customers with an eligible license and a CRM login (Dynamics 365 or Salesforce).

## Does Copilot for Sales work in incognito mode?

When you use the Copilot for Sales app in incognito mode or you have disabled third-party cookies, the following message is displayed:

:::image type="content" source="media/incognito.png" alt-text="Screenshot showing message in incognito mode.":::

When you search for a record in Copilot for Sales pane in Outlook, the record type filter might not work properly.

This is normal behavior. The reason for this is that Copilot for Sales uses cookies to save data to local storage. In incognito mode or when third-party cookies are disabled, access to local storage is blocked.

To get full benefit of all features in Copilot for Sales, browse in normal mode and allow Microsoft domain in third-party cookie settings.

For information about how to allow third-party cookies, see:

- [Enable cookies in Edge](https://support.microsoft.com/office/enable-cookies-6b018d22-1d24-43d9-8543-3d35ddb2cb52)

- [Clear, allow & manage cookies in Chrome](https://support.google.com/chrome/answer/95647)

- [Enable cookies in Safari](https://support.apple.com/guide/safari/ibrw850f6c51/mac)

## How can I add the Copilot for Sales app manually to a Teams meeting?

You can add the Copilot for Sales app manually to a Teams meeting to test it internally before scheduling a call with your customer.

- To add an app before a meeting, first send the meeting invite then open the meeting. Select **Add a tab **(**+**), search for Copilot for Sales, and then select it.

    :::image type="content" source="media/add-before-meeting.png" alt-text="Screenshot showing add Copilot for Sales app before meeting.":::

- To add an app during a meeting, after the meeting starts select **Add an app** (**+**), search for Copilot for Sales, and then select it.

    :::image type="content" source="media/add-during-meeting.png" alt-text="Screenshot showing add Copilot for Sales app during meeting.":::

## What's the minimum version of Outlook required for Copilot for Sales?

The minimum required version for Outlook is:

- **Outlook for Windows**: version 2206 (Build 15330.20196)

- **Outlook for Mac**: 16.78

## Why are meeting insights not getting generated even if meeting is transcribed?

Meeting insights are generated only if version of the Copilot for Sales app in Microsoft Teams is 1.0.9 or higher. To check your app's version:

1. Open Microsoft Teams and select **Copilot for Sales** in the navigation bar on the left.

1. In the Copilot for Sales app, go to the **About** tab and check the version.

If the Copilot for Sales app for Teams is installed by your administrator, you must contact your administrator to update the app to the latest version.

If you've installed Copilot for Sales app for Teams by yourself, you can update it to the latest version by following the instructions [here](https://support.microsoft.com/office/update-an-app-3d53d136-5c5d-4dfa-9602-01e6fdd8015b).

## How many hours of conversation intelligence are available with Copilot for Sales?

You get unlimited call recording and processing hours with Copilot for Sales.

## How can I provide feedback about Copilot for Sales?

You can go to the [feedback portal](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) to suggest a feature. You can also join the [Tech Community](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) forum to interact with the product team and other users of Copilot for Sales.
