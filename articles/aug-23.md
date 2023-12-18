---
title: What's new in Microsoft Sales Copilot - August 2023
description: Information about new features, improvements, and bug fixes in Microsoft Sales Copilot August 2023 release.
ms.date: 08/07/2023
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# What's new in the August 2023 update

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes. To see the long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

| Region      | Availability  |
|-------------|---------------|
| All regions | August 07, 2023 |

## Features included in this release

| Feature area | Feature | Details | Client | Resources | Enabled by * | Availability |
|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|
| Teams meeting experiences  | Streamlined access to CRM data during Teams meetings  | Sellers can now seamlessly view and edit the connected CRM record during the meeting in Teams  | Teams app | [Seller guide](use-sales-copilot-app-during-meeting.md) | Enabled by default | General availability |
| Collaboration space | CRM customizations applies to accounts and opportunities  | Collaboration spaces now seamlessly integrate with CRM customizations set by admins in the Sales Copilot app. If an admin removes **Account** or **Opportunity** records from showing up in the Sales Copilot app, sellers will no longer see the respective entity in the **Collaborate in Teams** card. However, if either Account or Opportunity entity is available, sellers can continue to create Collaboration spaces for that specific entity. If both these entities are removed by the admin, the **Collaborate in Teams** card isn't displayed in the Sales Copilot app.  | Outlook add-in | [Admin guide](customize-forms-and-fields.md#impact-of-crm-customization-on-collaboration-spaces) | Enabled by default | General availability |
| CRM operations  | Support for saving draft e-mails  | Sellers can now save Outlook emails in compose mode to Dynamics 365. | Outlook add-in | [Seller guide](save-outlook-activities-crm.md) | Enabled by default | General availability |
| CRM operations | Mandatory field enforcement  | Administrators can mark fields as mandatory only in Sales Copilot, even if the fields aren't mandatory in the CRM system.  | Outlook add-in | [Admin guide](customize-forms-and-fields.md#mark-fields-as-required-in-sales-copilot) | Enabled by admin | General availability |
| CRM operations | Record type filter for polymorphic fields   | Sellers can now filter search results in polymorphic fields (fields that accept records of more than one type) other than the connected record.   | Outlook add-in | NA | Enabled by default | General availability |
| CRM operations | Support for saving Outlook emails and appointments to Salesforce CRM without enhanced email    | Sellers can save Outlook emails and appointments to Salesforce as task records if enhanced email isn't turned on in Salesforce CRM.  | Outlook add-in | [Seller guide](save-outlook-activities-crm.md) | Enabled by admin (through Microsoft Support) | General availability |
| Administrator settings | Sales Copilot default on   | Copilot features are enabled by default for Dynamics 365 customers in North America and Europe.  | Outlook add-in | [Admin guide](suggested-replies.md) | Enabled by default | General availability |
| Copilot generated emails  | Improving meeting invitation experience  | Sellers now have enhanced meeting invitation options through their generated emails.  | Outlook add-in | [Seller guide](use-copilot-kickstart-email-messages.md#add-or-remove-meeting-suggestions) | Enabled by default | General availability |
| Copilot summarized CRM entities | Data discoverability with references   | Sellers see the opportunity summary in email context when the mail is tracked to CRM. | Outlook add-in | [Seller guide](view-opportunity-summary.md) | Enabled by default | General availability |
| Copilot email summaries | Citations and explanations  | Sellers see citations and explanations of the summary bullets.  | Outlook add-in | [Seller guide](view-opportunity-summary.md#view-data-source-in-opportunity-summary) | Enabled by default | General availability |


\* Learn more about [administrator settings for Sales Copilot](administrator-settings-for-viva-sales.md).

## Administration update

| Configuration location | Feature | Details | Resources |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Forms tab in Sales Copilot admin settings  | Mandatory field enforcement  | Administrators can now mark fields that are optional in CRM to be mandatory in Sales Copilot. | [Admin guide](customize-forms-and-fields.md#mark-fields-as-required-in-sales-copilot) |
| Copilot tab in Sales Copilot admin settings   | Sales Copilot default on  | Copilot features are enabled by default for Dynamics 365 customers in North America and Europe. | [Admin guide](suggested-replies.md) |


## Outlook add-in and Teams app updates

| Application    | Previous Version | New Version | New Version Change | Description of changes |
|------------------------------------------|------------------|-------------|--------------------|------------------------|
| Microsoft Viva Sales for Outlook add-in  | 1.0.0.12  | No change     | None        | None               |
| Microsoft Viva Sales for Microsoft Teams | 9.4.23177021 | No change  | None        | None               |

## Critical bug fixes

None

## Additional resources

[What's New in Sales Copilot – August 2023](https://techcommunity.microsoft.com/t5/microsoft-sales-copilot-blog/what-s-new-in-sales-copilot-august-2023/ba-p/3893099)

