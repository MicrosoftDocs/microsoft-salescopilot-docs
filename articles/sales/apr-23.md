---
title: What's new in Microsoft Viva Sales - April 2023
description: Information about new features, improvements, and bug fixes in Microsoft Viva Sales April 2023 release.
ms.date: 04/24/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# April 2023 update

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes. To see the long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

|Region|Availability|
|------|------------|
|All regions|April 19, 2023|

## Features included in this release

|Feature area|Feature|Description|Resources|Enabled by *|Availability|
|------------|-------|-----------|---------|----------|------------|
|Copilot|Summarized CRM data for meeting preparation |Sellers can generate a summary of the recent notes specific to a selected opportunity mapped to a meeting invite.|[Documentation](https://support.microsoft.com/topic/preview-view-opportunity-summary-373ddcee-10d5-4a14-bfaf-298529ee8fbf) |Enabled by default |Public preview|
|Copilot|Summarize email communication and save to CRM |Sellers can generate a summary of internal and external e-mail threads, including CRM data references, and save the summary to the CRM mapped to an opportunity record.|[Documentation](https://support.microsoft.com/topic/preview-view-and-update-crm-with-email-conversation-summary-7968335e-5c4d-4faf-a57f-5a4ff97ab6d2)|Enabled by default |Public preview|
|Copilot|AI-generated email replies supported for internal e-mails |Sellers can now leverage AI generated e-mail replies and new e-mail drafts threads that do not have any external e-mail recipient preset. In these cases, the AI generated content is solely based on the body of the e-mail and no CRM records.|[Admin guide](suggested-replies.md)<br><br> [Seller guide](https://support.microsoft.com/topic/use-copilot-to-kickstart-email-messages-148708be-e1f9-477c-baba-0b4dd4b7abef)|Enabled by admin **|General availability|
|CRM customizations |Entity search improvements|Sellers can now see configurable and customized key fields when searching for records when editing or creating new records, in the **Save to CRM** flow, and Teams messaging extensions.|[Documentation](customize-forms-and-fields.md)|Enabled by admin|General availability|

\* Learn more about [administrator settings for Viva Sales](administrator-settings-for-viva-sales.md).  

** Enabled by default in North America with the ability for Admins to enable or disable.

## Outlook add-in and Teams app update

|Application|Previous version|New version change|Description of changes|
|-----------|----------------|------------------|----------------------|
|Viva Sales for Microsoft Outlook |1.0.0.12|Removed OnAppointmentSend launch event.|This launch event was previously used to add the Viva Sales app to meetings with external CRM recipients to enable Sales Conversational Intelligence. However, this change was causing timeouts for certain users when scheduling meetings in Microsoft Outlook.<br><br>We have since moved the logic to add the Viva Sales app to meetings to a different flow to address the reliability issue. |
|Viva Sales for Microsoft Teams|1.0.9|None|None|

## Critical bug fixes

|Application|Title|Symptom|
|-----------|-----|-------|
|Viva Sales for Microsoft Outlook|Long delays and errors when sending meeting invites |Users would experience long delays when sending meeting invites through Microsoft Outlook and would see an error message "Viva Sales is unavailable and can’t process your meeting at this time.".|

## Additional resources

[What's New in Viva Sales – April 2023 - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales-blog/what-s-new-in-viva-sales-april-2023/ba-p/3800203)