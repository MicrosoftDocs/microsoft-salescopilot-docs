---
title: What's new in Microsoft Sales Copilot - September 2023
description: Learn about new features, improvements, and bug fixes in the Microsoft Sales Copilot September 2023 release.
ms.date: 09/20/2023
ms.topic: overview
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# What's new in Microsoft Sales Copilot - September 2023

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes. To see long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

| Region      | Availability  |
|-------------|---------------|
| All regions | September 05, 2023 |

## Features included in this release

| Feature area | Feature | Details | Client | Resources | Turned on by * | Availability |
|------------|------------|-------------|------------|----------|-----------|----------|
| Collaboration space | AI-generated opportunity summary in deal room channels | The opportunity summary is a concise overview of key CRM opportunity details, including sales stage, budget, close date, account, contact, and important notes. The opportunity summary is available in the first-run experience welcome post in a deal room channel in Microsoft Teams. To view it again later, sellers can post the command `@Sales Copilot show summary`. If copilot AI features are turned off, a non-AI summary is provided. | Teams | [Seller guide](collaborate-teams-newly-created-existing-team.md#view-an-ai-generated-opportunity-summary-in-the-deal-room-channel) | Turned on by default for Dynamics 365 Sales tenants in North America and Europe. Must be turned on by admin for tenants in all other regions. | General availability |
| Onboarding | Welcome email to users after the Sales Copilot add-in is installed in Outlook | When the Sales Copilot add-in is installed in Outlook, a welcome email is sent to users during business hours in their time zone. The email contains links to product demo videos, documentation, and training to help new users get started. | Outlook add-in | NA | Turned on by default for sellers | General availability |
| CRM operations | Show Salesforce hyperlink formula fields as clickable links in Sales Copilot | In Salesforce, formula fields can be defined as HTML and rendered as rich text in Salesforce Lightning UI. In Sales Copilot, these fields used to appear as raw HTML. With the September 2023 update, formula fields that contain URLs (but no images) are rendered as hyperlinks in Sales Copilot. | Outlook add-in and Teams app | [Admin guide](customize-forms-and-fields.md#how-are-hyperlink-formula-fields-from-salesforce-crm-displayed-in-sales-copilot) | Turned on by default for sellers | General availability |
| Save-to-CRM  | Save draft appointments to Dynamics 365 | Before, sellers had to send appointments first before saving them to Dynamics 365, involving 8 to 15 extra clicks. With the September 2023 update, sellers can save draft appointments in compose mode to Dynamics 365. | Outlook add-in | [Seller guide](save-outlook-activities-crm.md) | Turned on by default for sellers | General availability |
| Email summaries | CRM context on external emails and citations available to users | CRM contact and account information are highlighted in the email summary. Sellers can quickly view the summary bullets by selecting the numbers. | Outlook add-in | [Seller guide](save-outlook-activities-crm.md) | Turned on by default for sellers | General availability |

\* [Learn more about administrator settings for Sales Copilot](administrator-settings-for-viva-sales.md).

## Outlook add-in and Teams app updates

| Application | Previous version | New version | New version change | Description of changes |
| --- | --- | --- | --- | --- |
| Microsoft Viva Sales for Outlook add-in | 1.0.0.12 | 1.0.0.12 | Sales Copilot rebranding | The new Outlook add-in manifest contains rebranding changes from Viva Sales to Sales Copilot. |
| Microsoft Viva Sales for Microsoft Teams | 9.4.23177021 | 9.7.23249007 | Sales Copilot rebranding and description changes | The new Teams app manifest contains rebranding changes from Viva Sales to Sales Copilot. It also includes a new description to inform users and admins about the fact that Sales Copilot has permission to collect Teams meeting data such as meeting recordings and transcripts. |

## Critical bug fixes

None

## Additional resources

[What's New in Sales Copilot – September 2023](https://techcommunity.microsoft.com/t5/microsoft-sales-copilot-blog/what-s-new-in-sales-copilot-september-2023/ba-p/3918815)
