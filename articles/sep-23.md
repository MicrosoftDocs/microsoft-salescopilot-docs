---
title: What's new in Microsoft Sales Copilot - September 2023
description: Information about new features, improvements, and bug fixes in Microsoft Sales Copilot September 2023 release.
ms.date: 09/20/2023
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# What's new in the September 2023 update

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes. To see the long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

| Region      | Availability  |
|-------------|---------------|
| All regions | September 05, 2023 |

## Features included in this release

| Feature area | Feature | Details | Client | Resources | Enabled by * | Availability |
|------------|------------|-------------|------------|----------|-----------|----------|
| Collaboration space |AI powered opportunity summary in deal rooms   | Opportunity summary provides a concise overview of key CRM opportunity details, including sales stage, budget, close date, account, contact, and important notes. Opportunity summary is instantly available as a first run experience post in a deal room in Microsoft Teams. To view opportunity summary beyond the first run experience, sellers can use the command: @Sales Copilot show summary. If Copilot admin configuration is disabled, a non-AI summary is provided.  | Teams | [Seller guide](collaborate-teams-newly-created-existing-team.md#view-ai-generated-opportunity-summary-in-deal-room) | Enabled by default for Dynamics 365 Sales tenants in North America and Europe. <br><br>Enabled by admin for tenants in all other regions.  | General availability |
| Onboarding  | Welcome email to users after Sales Copilot Outlook add-in is installed  | Welcome emails are sent to each new user when Sales Copilot add-in is installed in Outlook. The email contains links to product demo videos, documentation, and training to help new users get started. Email is sent to each user in their time zone during business hours.  | Outlook add-in | NA | Enabled by default for sellers | General availability |
| CRM operations | Show Salesforce hyperlink formula fields as clickable links in Sales Copilot | Salesforce allows formula fields to be defined as HTML and renders them as rich-text in Salesforce Lightning UI. In Sales Copilot, such fields used to appear as raw HTML. With the September 2023 update, formula fields containing URLs (but no images) are rendered as hyperlinks in Sales Copilot.   | Outlook add-in and Teams app | [Admin guide](customize-forms-and-fields.md#how-are-hyperlink-formula-fields-from-salesforce-crm-displayed-in-sales-copilot) | Enabled by default for sellers | General availability |
| Save-to-CRM  | Save draft appointments to Dynamics 365  | Today, sellers are forced to send appointments first before saving them to Dynamics 365 – involving 8 to 15 extra clicks. With the September 2023 update, sellers can save draft appointments in compose mode to Dynamics 365.  | Outlook add-in | [Seller guide](save-outlook-activities-crm.md) | Enabled by default for sellers | General availability |
| Email summaries  | CRM context on external emails and citations available to end-users   | CRM contact and account information are highlighted within the email summary. Sellers can quickly understand the summary bullets by selecting the citations numbers.   | Outlook add-in | [Seller guide](save-outlook-activities-crm.md) | Enabled by default for sellers | General availability |



\* Learn more about [administrator settings for Sales Copilot](administrator-settings-for-viva-sales.md).


## Outlook add-in and Teams app updates

| Application    | Previous Version | New Version | New Version Change | Description of changes |
|------------------------------------------|------------------|-------------|--------------------|------------------------|
| Microsoft Viva Sales for Outlook add-in  | 1.0.0.12  | 1.0.0.12  | Sales Copilot rebranding  | The new Outlook Add-In manifest contains rebranding changes from Viva Sales to Sales Copilot.   |
| Microsoft Viva Sales for Microsoft Teams | 9.4.23177021 | 9.7.23249007   | Sales Copilot rebranding and description changes    | The new Teams app manifest contains rebranding changes from Viva Sales to Sales Copilot. <br><br>It also includes a new description to inform users and admins about the fact that Sales Copilot has permission to collect Teams meeting data such as meeting recordings and transcripts.  |

## Critical bug fixes

None

## Additional resources

[What's New in Sales Copilot – September 2023](https://techcommunity.microsoft.com/t5/microsoft-sales-copilot-blog/what-s-new-in-sales-copilot-september-2023/ba-p/3918815)
