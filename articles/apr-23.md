---
title: What's new in Microsoft Viva Sales - April 2023
description: Information about new features, improvements, and bug fixes in Microsoft Viva Sales April 2023 release.
ms.date: 05/15/2023
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# April 2023 update

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes released in April 2023. To see the long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

|Region|Availability|
|------|------------|
|All regions|April 19, 2023|

## Features included in this release

|Feature area|Feature|Description|Client|Resources|Enabled by *|Availability|
|------------|-------|-----------|---------|----------|------------|--------|
|Copilot|Summarized CRM data for meeting preparation |Sellers can generate a summary of the recent notes specific to a selected opportunity mapped to a meeting invite.|Outlook add-in|[Seller guide](view-opportunity-summary.md) |Enabled by default |Public preview|
|Copilot|Summarize email communication and save to CRM |Sellers can generate a summary of internal and external email threads, including CRM data references, and save the summary to the CRM mapped to an opportunity record.|Outlook add-in|[Seller guide](view-save-email-summary-crm.md)|Enabled by default |Public preview|
|Copilot|AI-generated email replies supported for internal emails |Sellers can now use AI-generated email replies and new email drafts threads that don't have any external email recipient preset. In these cases, the AI generated content is solely based on the body of the email and no CRM records.|Outlook add-in|[Admin guide](suggested-replies.md)<br><br> [Seller guide](use-copilot-kickstart-email-messages.md)|Enabled by admin **|General availability|
|CRM customizations |Entity search improvements|Sellers can now see configured and customized key fields when searching for records while editing or creating new records, in the **Save to CRM** flow, and Teams messaging extensions.|Outlook add-in|[Admin guide](customize-forms-and-fields.md)|Enabled by admin|General availability|

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
