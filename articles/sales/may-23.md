---
title: What's new in Microsoft Viva Sales - May 2023
description: Information about new features, improvements, and bug fixes in Microsoft Viva Sales May 2023 release.
ms.date: 05/24/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# May 2023 update

We're excited to announce our newest updates! This article summarizes general availability features, preview features, monthly enhancements, and bug fixes. To see the long-term feature plans, take a look at the [Dynamics 365 release plans](/dynamics365/release-plans/).

## Availability

|Region|Availability|
|------|------------|
|All regions|May 23, 2023|

## Features included in this release

| Feature area | Feature | Description | Client | Resources | Enabled by * | Availability |
|--------------|-----------|-------------|--------------|---------------|--------------|------------|
| Copilot | AI-generated summarized views for meeting preparation | Sellers can see opportunity timeline summary that reflects summarized emails and contextual references within the summarized bullets. | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/preview-view-opportunity-summary-373ddcee-10d5-4a14-bfaf-298529ee8fbf) | Enabled by default<br /></br><br /></br>Can be disabled through Viva Sales admin settings | Public preview |
| Copilot | Email conversation summary and save to CRM | Sellers will see improved error messages when seeing protected emails, unsupported languages, or when the email contains inappropriate content.</br> The summary quality is also improved, disregarding disclaimers and irrelevant signature information, improved profanity detection and redaction, and gender neutralization (they/their instead of she/he). | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/view-and-update-crm-with-email-conversation-summary-7968335e-5c4d-4faf-a57f-5a4ff97ab6d2) | Enabled by default | General availability |
| CRM customizations | Support to view Out-of-box (OOB) and custom entities | Administrators can add and remove OOB and custom entities and their corresponding fields through Viva Sales admin settings. They can also control the filtering and sorting behavior for CRM lists in the Outlook side pane.<br> Sellers can see the newly added OOB and custom entities in the Outlook side pane, share OOB and custom entities in Teams via adaptive cards, and search for OOB and custom entities in the Teams messaging extensions with the new **Advanced Search** functionality. | Outlook add-in<br /></br><br /></br>Microsoft Teams app | [Admin guide](customize-forms-and-fields.md#add-a-new-record-type) <br><br> [Seller guide](https://support.microsoft.com/topic/share-a-crm-record-in-a-teams-conversation-e07cc6b4-9cc7-43ef-905e-b8ff0c8526ed#bkmk_advsearch) | Enabled by admin | General availability |
| CRM Customizations | Support to save Outlook emails and appointments to out-of-box and custom entities | Administrators can enable custom entities and corresponding fields through Viva Sales admin settings and remove the existing OOB entities.</br> Sellers can search for and connect Outlook emails and meeting activities to OOB and custom entity records supported by their CRMs and configured by their administrators. | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/save-outlook-activities-to-your-crm-ee4db5e3-91a5-4d29-b9c2-980959d2fdd7) | Enabled by admin | General availability |
| Core Experiences | Search improvements to lookup any records by its name and key fields | Administrators can enable up to two key fields for OOB and custom entities.</br>Sellers will see the newly added key fields when search results are displayed in the Outlook side pane when connecting activities to CRM records or setting a related entity. | Outlook add-in | [Admin guide](customize-forms-and-fields.md#search-behavior-in-viva-sales-add-in-for-outlook) | Enabled by admin | General availability |
| Core Experiences | Outlook information architecture and navigation | Sellers will see a number of improvements to the information architecture and navigation of the Outlook side pane.</br> The changes include a contextual header to inform the user of reference records, action cards to surface key actions, improved styling and consistent button locations, and account and opportunity detail views to help streamline seller workflows. | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/use-viva-sales-in-outlook-ec3605f9-fdb0-4593-9c5b-b43a76c07081) | Enabled by default | General availability |
| Core Experiences | Automatically sign in Dynamics 365 users with single environment | Sellers (Dynamics 365 only) with access to a single environment with the Viva Sales solution or single production environment with the Viva Sales solution will be automatically signed in. They'll land straight on the **Highlights** tab when launching the Outlook side pane for the first time, skipping all the sign in steps, and will see a dismissible message bar on the top. | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/use-viva-sales-in-outlook-ec3605f9-fdb0-4593-9c5b-b43a76c07081#bkmk_vivasales_autosignin) | Enabled by default | General availability |
| Core Experiences | First-run experience improvements | Sellers can access the Copilot capabilities, such as suggested email replies and summaries, without signing into the CRM.</br>Sellers will see a sign-in prompt encouraging them to sign in to the CRM to get enriched capabilities. | Outlook add-in | [Seller guide](https://support.microsoft.com/topic/use-viva-sales-in-outlook-ec3605f9-fdb0-4593-9c5b-b43a76c07081#bkmk_vivasales-no-signin) | Enabled by default | General availability |![image](https://github.com/MicrosoftDocs/viva-docs-pr/assets/26568592/36b914d7-2547-4a4f-a346-83c613a8d214)


\* Learn more about [administrator settings for Viva Sales](administrator-settings-for-viva-sales.md).  

** Enabled by default in North America with the ability for Administrators to enable or disable.

## Administration update

|Configuration location|Feature|Description|Resources|
|----------------------|-------|-----------|---------|
|Forms tab in Viva Sales admin settings|Support to view out-of-box (OOB) and custom entities|Enable and disable OOB and custom entities to surface across all Viva Sales experiences.|[Admin guide](customize-forms-and-fields.md#add-a-new-record-type)|

## Outlook add-in and Teams app update

|Application|Previous version|New version|New version change|Description of changes|
|-----------|----------------|------------------|----------------------|-------|
|Viva Sales for Microsoft Outlook |1.0.0.12|TBD|None|None |
|Viva Sales for Microsoft Teams|1.0.9|TBD|New service infrastructure|New manifest changes are published to point the Viva Sales App for Teams towards a new service infrastructure layer for improved performance and reliability.|

## Critical bug fixes

None

## Additional resources

Coming soon
