---
title: What's new in Microsoft Sales Copilot - August 2023
description: Information about new features, improvements, and bug fixes in Microsoft Sales Copilot August 2023 release.
ms.date: 08/07/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
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
| Teams meeting experiences  | Streamlined access to CRM data during Teams meetings  | Sellers can now seamlessly view and edit the connected CRM record during the meeting in Teams  | Teams app | [Seller guide](https://support.microsoft.com/topic/d111ea37-f5ca-4010-9eb1-89f4dc3e9ebd) | Enabled by default | General availability |
| Collaboration space | CRM customizations applies to accounts and opportunities  | Collaboration spaces now seamlessly integrate with CRM customizations set by admins in the Sales Copilot app. If an admin removes **Account** or **Opportunity** records from showing up in the Sales Copilot app, sellers will no longer see the respective entity in the **Collaborate in Teams** card. However, if either Account or Opportunity entity is available, sellers can continue to create Collaboration spaces for that specific entity. If both these entities are removed by the admin, the **Collaborate in Teams** card is not displayed in the Sales Copilot app.  | Outlook add-in | [Admin guide](customize-forms-and-fields.md#impact-of-crm-customization-on-collaboration-spaces) | Enabled by default | General availability |
| CRM operations  | Support for saving draft e-mails  | Sellers can now save Outlook emails in compose mode to Dynamics 365. | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/save-outlook-activities-to-your-crm-ee4db5e3-91a5-4d29-b9c2-980959d2fdd7) | Enabled by default | General availability |
| CRM operations | Mandatory field enforcement  | Administrators can mark fields as mandatory only in Sales Copilot, even if the fields are not mandatory in the CRM system.  | Outlook add-in | [Admin guide](customize-forms-and-fields.md#mark-fields-as-required-in-sales-copilot) | Enabled by admin | General availability |
| CRM operations | Record type filter for polymorphic fields   | Sellers can now filter search results in polymorphic fields (fields which accept records of more than one type) other than the connected record.   | Outlook add-in | Coming soon | Enabled by default | General availability |
| CRM operations | Support for saving Outlook emails and appointments to Salesforce CRM without enhanced email    | Sellers can save Outlook emails and appointments to Salesforce as task records if enhanced email is not turned on in Salesforce CRM.  | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/save-outlook-activities-to-your-crm-ee4db5e3-91a5-4d29-b9c2-980959d2fdd7) | Enabled by admin (through Microsoft Support) | General availability |
| Administrator settings | Sales Copilot default on   | Copilot features are enabled by default for Dynamics 365 customers in North America and Europe.  | Outlook add-in | [Admin guide](suggested-replies.md) | Enabled by default | General availability |
| Copilot generated emails  | Improving meeting invitation experience  | Sellers will now have enhanced meeting invitation options through their generated emails.  | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/use-copilot-to-kickstart-email-messages-148708be-e1f9-477c-baba-0b4dd4b7abef#bkmk_add_remove_meeting) | Enabled by default | General availability |
| Copilot summarized CRM entities | Data discoverability with references   | Sellers will see the opportunity summary in email context when the mail is tracked to CRM. | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/preview-view-opportunity-summary-373ddcee-10d5-4a14-bfaf-298529ee8fbf) | Enabled by default | General availability |
| Copilot email summaries | Citations and explanations  | Sellers will see citations and explanations of the summary bullets.  | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/view-and-save-email-summary-to-crm-7968335e-5c4d-4faf-a57f-5a4ff97ab6d2#bkmk_data_source_email_summary) | Enabled by default | General availability |


\* Learn more about [administrator settings for Sales Copilot](administrator-settings-for-viva-sales.md).

## Administration update

| Configuration location | Feature | Details | Resources |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Forms tab in Sales Copilot admin settings  | Mandatory field enforcement  | Administrators can now mark fields which are optional in CRM to be mandatory in Sales Copilot. | [Admin guide](customize-forms-and-fields.md#mark-fields-as-required-in-sales-copilot) |
| Copilot tab in Sales Copilot admin settings   | Sales Copilot default on  | Copilot features are enabled by default for Dynamics 365 customers in North America and Europe. | [Admin guide](suggested-replies.md) |


## Outlook add-in and Teams app updates

| Application    | Previous Version | New Version | New Version Change | Description of changes |
|------------------------------------------|------------------|-------------|--------------------|------------------------|
| Microsoft Viva Sales for Outlook add-in  | 1.0.0.12  | No change     | None        | None               |
| Microsoft Viva Sales for Microsoft Teams | 9.4.23177021 | No change  | None        | None               |

## Critical bug fixes

None

## Additional resources

Coming soon

