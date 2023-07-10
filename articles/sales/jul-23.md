---
title: What's new in Microsoft Viva Sales - July 2023
description: Information about new features, improvements, and bug fixes in Microsoft Viva Sales July 2023 release.
ms.date: 07/07/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# July 2023 update

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes. To see the long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

| Region      | Availability  |
|-------------|---------------|
| All regions | July 12, 2023 |

## Features included in this release

| Feature area | Feature | Details | Client | Resources | Enabled by * | Availability |
|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|-------------------------|
| Core experiences | Automatically sign in Dynamics 365 users with multiple environments | Sellers (Dynamics 365 only) with access to multiple environments with the Viva Sales solution are automatically signed in from the Viva Sales Outlook add-in. When launching Viva Sales in Outlook for the first time, the Highlights tab is displayed, skipping the sign in steps and instead seeing a **Switch environment** dialog. This dialog is also available to all signed in Dynamics 365 sellers from **Options** (**…**). It enables easily switching environment or CRM without signing out. | Outlook add-in | Coming soon | Enabled by default | General availability |
| Core experiences | Show application diagnostics and troubleshooting data in Outlook side pane | Sellers can view diagnostics and troubleshooting data, including application versions, session IDs, and other relevant application metadata. This data is helpful when working with technical support. | Outlook add-in | Coming soon | Enabled by default | General availability |
| Core experiences | New actionable message banner in Outlook e-mails | Sellers can easily discover the Viva Sales for Microsoft Outlook through a new and more prominent actionable message banner for selected e-mails that include senders or recipients external to the organization.| Outlook add-in | Coming soon | Enabled by default<br><br>Can be disabled by admins from Microsoft 365 admin center. | General availability |
| CRM operations | Enable server-side sync when saving emails or appointments to Dynamics 365 | Sellers connected to Dynamics 365 are required to turn on [server-side-synchronization](/power-platform/admin/server-side-synchronization), which ensures all participants see a consistent save or not-saved status. It also enables autosaving of replies in email threads already saved to CRM. | Outlook add-in | Coming soon | Enabled by default | General availability |
| CRM operations | Truncate large emails saved to Salesforce | Emails larger than the maximum allowed characters by Salesforce are truncated automatically when saved to CRM. | Outlook add-in | Coming soon | Enabled by default | General availability |
| Copilot | Real-time tips in Teams meeting side panel | Sellers on a Teams meeting with Viva Sales Teams panel open, receive real-time information cards, prompted by competitors or brands mentioned by the customer. | Teams app | NA | Enabled by Microsoft on demand for preview customers | Preview |
| Copilot | AI-generated e-mails | Sellers see the addition of tone knobs to their generated email suggestions, offering to select formal or informal email style. In addition, sellers experience an improved user interface design. | Outlook add-in | Coming soon | Enabled by default for tenants in North America and Europe.</br><br>Enabled by admin for tenants in all other regions. | General availability |
| Copilot | AI-generated e-mail summaries | Sellers can now see summaries in French, Spanish and German for French, Spanish and German emails. Quality improvements, including specific treatment for short emails. | Outlook add-in | Coming soon | Enabled by default | General availability |


\* Learn more about [administrator settings for Viva Sales](administrator-settings-for-viva-sales.md).

## Administration update

| Configuration location | Feature | Details | Resources |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Microsoft 365 admin center  | New actionable message banner in Outlook e-mails | Enable or disable whether Viva Sales content in general and the actionable messages are shown to users in the tenant using the **Allow users to see Viva Sales content in Microsoft 365 apps** setting. | Coming soon |


## Outlook add-in and Teams app updates

| Application    | Previous Version | New Version | New Version Change | Description of changes |
|------------------------------------------|------------------|-------------|--------------------|------------------------|
| Microsoft Viva Sales for Outlook add-in  | 1.0.0.12  | None     | None        | None               |
| Microsoft Viva Sales for Microsoft Teams | 9.4.23177021         | None         | None               | None                   |

## Critical bug fixes

None

## Additional resources

Coming soon

