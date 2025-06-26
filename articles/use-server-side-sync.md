---
title: Use server-side synchronization with Copilot for Sales
description: Learn how to use server-side synchronization with Copilot for Sales.
ms.date: 06/26/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Use server-side synchronization with Copilot for Sales

> [!NOTE]
> This article is relevant only if you've connected Copilot for Sales to your Dynamics 365 environment.

[Server-side synchronization](/power-platform/admin/server-side-synchronization) provides direct synchronization of emails, appointments, contacts, and tasks between Dynamics 365 applications and Exchange email server. Turning on server-side synchronization is a prerequisite for saving Outlook emails and appointments to Dynamics 365. Enabling server-side synchronization has the following benefits:

- All participants in an email or appointments who are Copilot for Sales users will see the same status (saved or unsaved) of the Outlook activity.  
- Remove saved emails and appointments.  
- Automatically save replies to emails that were saved to CRM.

## Turn on server-side synchronization

If you're a CRM administrator, you can simplify seller experience by setting up server-side synchronization of emails and appointments for all Copilot for Sales users. For information about enabling server-side synchronization, see [Connect to Exchange Online](/power-platform/admin/connect-exchange-online).  
If you're a seller and if server-side synchronization isn't enabled for you by your administrator, you're prompted to enable server-side synchronization for your mailbox when you save Outlook activities to Dynamics 365 using Copilot for Sales for the first time.

> [!NOTE]
> If you don't turn on server-side synchronization, a message is displayed when you save an email or a meeting for the first time to your CRM.

## Mailbox configuration for saving Outlook activities to Dynamics 365

Dynamics 365 users will have their mailboxes configured based on the settings provided as part of turning on server-side synchronization.  
For a Copilot for Sales user to save Outlook emails and appointments to Dynamics 365 from Copilot for Sales, their mailboxes need to be:

- Configured to use server-side synchronization for incoming email, outgoing email, and appointments.  
- Approved  
- (configuration) Tested and enabled

In addition to the above configuration, sellers can have replies to a saved email saved to CRM automatically if any option other than **No email messages** is selected under the [Email tab in Personalization Settings](/power-apps/user/set-personal-options#email-tab-options) in Dynamics 365.  

## Troubleshooting errors

If you get error due to server-side synchronization, see the following troubleshooting guides for the resolution:

- [Unable to save email to CRM due to invalid mailbox settings](tsg-mailbox-settings.md)  
- [Fix mailbox errors in Dynamics 365](tsg-mailbox-errors.md)
