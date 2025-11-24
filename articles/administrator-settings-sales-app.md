---
title: Administrator settings for Sales in Microsoft 365 Copilot
description: Learn how to use administrator settings to customize the Sales app experience in Outlook and Teams.
ms.date: 11/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/28/2023
  - bap-template
---

# Administrator settings for Sales in Microsoft 365 Copilot

As a tenant administrator or CRM (customer relationship management) administrator, you can use administrator settings to customize how your users experience the Sales app in Outlook and Teams, including who can use AI capabilities, for all environments in your organization.

## Prerequisites

- The Sales app is installed in either [Outlook](install-sales-as-an-integrated-app.md) or [Teams](install-pin-sales-teams.md). 

## Who can access administrator settings?

Administrator settings are visible only when you sign in with administrator credentials to the Sales app in [Outlook](sign-in-crm-outlook.md) or [Teams](sign-in-crm-teams.md). The permissions you need depend on which CRM you use.

- **Dynamics 365:** You must have the **System Administrator** or **System Customizer** role. If you're using a custom security role, you might need [more privileges to use the Sales app](privileges.md#privileges-required-for-dynamics-365-customers).

- **Salesforce:** Your user profile must have the **Modify All Data** or **Manage Data Integrations** permission. Permissions need to be set in your user profile, not in a permission set that's assigned to you.

If you change a user's permissions or security roles in your CRM, ask the user to sign out of the Sales app in Outlook or Teams, and then sign in again for your changes to be reflected. Changes in user permissions or security roles in the CRM can take up to 15 minutes to reflect in the Sales app in Teams.

## Access administrator settings

Teams and Outlook both play a part in how you access the Sales app administrator settings and what you can change.

You can access the administrator settings in the Sales app in Outlook and Teams. The settings apply to the CRM environment that you sign in to. To customize the Sales app for a different environment, [switch to that environment](sales-m365-copilot-faq.md#how-can-i-switch-crm-environments).

1. Open the Sales personal app in [Outlook](personal-app.md#open-the-personal-app-in-outlook) or [Teams](personal-app.md#open-the-personal-app-in-teams).
1. Sign in to [Outlook](sign-in-crm-outlook.md) or [Teams](sign-in-crm-teams.md) with your administrator credentials.  
1. On the left navigation pane, select **Sales**. If **Sales** isn't visible, select **View more apps** (**&hellip;**), and then select **Sales**. If you see the **Sales** window asking you to either add or open the app, select **Add** or **Open** to get the latest features.  
1. Select the **Settings** tab.  
1. Change the settings you need to.  
    **Tenant-level settings**:  
      - **Copilot AI**: [Controls who can use the Sales app AI capabilities in all environments](suggested-replies.md#turn-on-copilot-ai-features-for-your-organization).
      - **Collaboration spaces**: [Controls whether AI-powered tasks should be suggested in collaboration spaces](turn-off-suggested-tasks-collab-space.md)  
    
    **Environment-level settings**:  
      - **Copilot AI**: [Turn on Copilot AI feature](suggested-replies.md#turn-on-copilot-ai-features-in-your-environment) for your environment.      
      - **Save to (CRM)**: [Configure fields that sellers can use to categorize emails and meetings in CRM](save-additional-details-outlook.md).
      - **Forms**: [Determines what information is displayed in the Sales app in Outlook and Teams](customize-forms-and-fields.md). You can also control which records and fields sellers can edit directly in the Sales app.
      
    :::image type="content" source="media/viva-sales-tenant-admin.png" alt-text="Screenshot showing admin settings.":::

## Add the Sales app to Teams

If the Sales app isn't already added to Teams, you can add it from the Teams app store. Note that the app is added only for you, not for your entire organization.

1. Sign in to Microsoft Teams with your administrator credentials.  
1. In the navigation bar on the left, select **Apps**.  
1. Search for **Sales** and select it, and then select **Add**.  

