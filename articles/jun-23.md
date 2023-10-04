---
title: What's new in Microsoft Viva Sales - June 2023
description: Information about new features, improvements, and bug fixes in Microsoft Viva Sales June 2023 release.
ms.date: 06/26/2023
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# What's new in the June 2023 update

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes. To see the long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

| Region      | Availability  |
|-------------|---------------|
| All regions | June 19, 2023 |

## Features included in this release

| Feature area | Feature | Details | Client | Resources | Enabled by * | Availability |
|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|
| Collaboration | Collaboration spaces | Sellers can create preconfigured teams and channels in Microsoft Teams using Viva Sales add-in in Outlook, enabling seamless and secure conversations with colleagues and customers, using one of two templates: account team and deal room.</br><br>The account team template allows collaboration on account-related activities. It's applied at a team level, is linked to a CRM account, and includes a set of default channels.</br><br>The deal room template enables collaboration on opportunity-related activities. It's applied at a channel level and linked to a CRM opportunity.</br><br>Both templates also come with a set of prepinned apps, including Files with starter folders, CRM record, and OneNote. | Outlook add-in</br><br>Microsoft Teams app | [Seller guide](collaboration-space.md) | Enabled by default | General availability |
| Save Outlook emails and appointments to CRM | Remove saved e-mails and appointments in CRM | Sellers can delete e-mails and appointments that are saved in the CRM from within the Viva Sales add-in in Outlook. | Outlook add-in | [Seller guide](save-outlook-activities-crm.md#remove-saved-email-from-crm) | Enabled by default | General availability<br /></br>Dynamics 365 CRM only. |
| Core experiences | Outlook information architecture and navigation enhancements | Sellers can now reliably find their contact record information in one place on the CRM tab, and receive intelligent recommendations for actions to take on new contacts through action cards on the **Highlights** tab. Furthermore, sellers can quickly navigate to the top level of the Outlook side pane using the **Home** button. | Outlook add-in | [Seller guide](use-sales-copilot-outlook.md) | Enabled by default | General availability |
| Copilot | AI-generated e-mails | Sellers get improved meeting time recommendations based on their calendar availability and customer provided information, such as intent and time zone. | Outlook add-in | [Seller guide](use-copilot-kickstart-email-messages.md) | Enabled by default for Dynamics 365 Sales tenants in North America and Europe.</br><br>Enabled by admin for tenants in all other regions. | General availability |
| Copilot | AI-generated e-mails | Sellers can review explanations about data sources behind the generated content, such as CRM data, office availability and email context for better RAI and explanations | Outlook add-in | [Seller guide](use-copilot-kickstart-email-messages.md#view-data-source-in-suggested-content) | Enabled by default for Dynamics 365 Sales tenants in North America and Europe.</br><br>Enabled by admin for tenants in all other regions. | General availability |
| Copilot | AI-generated e-mail summaries | Sellers can now save an e-mail summary to the account record and the opportunity record. | Outlook add-in | [Seller guide](view-save-email-summary-crm.md) | Enabled by default for tenants in North America and Europe.</br><br>Enabled by admin for tenants in all other regions. | General availability |
| Copilot | AI-generated meeting preparation | Sellers get additional out-of-box fields and changes to tracked fields in the AI-generated opportunity summary for meeting preparation. | Outlook add-in | [Seller guide](view-opportunity-summary.md) | Enabled by default for tenants in North America and Europe.</br><br>Enabled by admin for tenants in all other regions. | Public preview |
| Copilot | Conversational Intelligence – meeting summaries | Sellers can convert action items into tasks tracked in CRM directly from Microsoft Teams. | Microsoft Teams app | [Seller guide](create-crm-tasks-meeting-summary.md) | Enabled by default | General availability |


\* Learn more about [administrator settings for Viva Sales](administrator-settings-for-viva-sales.md).

## Administration update

| Configuration location | Feature | Details | Resources |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Copilot tab in Viva Sales admin settings | Support to enable and disable all Copilot features in a single location | Admins can enable all Copilot features in a single location.</br>Copilot features are enabled by default for tenants in North America and Europe but disabled for tenants in all other regions. | [Admin guide](suggested-replies.md) |


## Outlook add-in and Teams app updates

| Application                              | Previous Version | New Version | New Version Change | Description of changes |
|------------------------------------------|------------------|-------------|--------------------|------------------------|
| Microsoft Viva Sales for Outlook add-in  | 1.0.0.12         | TBD         | None               | None                   |
| Microsoft Viva Sales for Microsoft Teams | 1.0.9            | TBD         | None               | None                   |

## Critical bug fixes

None

## Additional resources

- [What's New in Viva Sales – June 2023 - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales-blog/what-s-new-in-viva-sales-june-2023/ba-p/3846496)
- [Purpose built Collaboration spaces in Viva Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales-blog/purpose-built-collaboration-spaces-in-viva-sales/ba-p/3844021)

