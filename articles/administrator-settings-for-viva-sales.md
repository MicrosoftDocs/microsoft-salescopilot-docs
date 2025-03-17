---
title: Administrator settings for Copilot for Sales
description: Learn how to use administrator settings to customize the Microsoft 365 Copilot for Sales experience in Outlook and Teams.
ms.date: 12/10/2024
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

# Microsoft 365 Copilot for Sales admin settings

As a tenant administrator or CRM (customer relationship management) administrator, you can use administrator settings to customize how your users experience Copilot for Sales in Outlook and Teams, including who can use AI capabilities, for all environments in your organization.

## Prerequisites

- The Copilot for Sales app is installed in either [Outlook](install-viva-sales-as-an-integrated-app.md) or [Teams](install-pin-viva-sales-teams.md). 

## Who can access administrator settings?

Administrator settings are visible only when you sign in with administrator credentials to the Copilot for Sales app in [Outlook](sign-in-crm-outlook.md) or [Teams](sign-in-crm-teams.md). The permissions you need depend on which CRM you use.

- **Dynamics 365:** You must have the **System Administrator** or **System Customizer** role. If you're using a custom security role, you might need [more privileges to use Copilot for Sales](privileges.md#privileges-required-for-dynamics-365-customers).

- **Salesforce:** Your user profile must have the **Modify All Data** or **Manage Data Integrations** permission. Permissions need to be set in your user profile, not in a permission set that's assigned to you.

If you change a user's permissions or security roles in your CRM, ask the user to sign out of Copilot for Sales in Outlook or Teams, and then sign in again for your changes to be reflected. Changes in user permissions or security roles in the CRM can take up to 15 minutes to reflect in the Copilot for Sales app in Teams.

## Access administrator settings

Teams and Outlook both play a part in how you access the Copilot for Sales administrator settings and what you can change.

You can access the administrator settings in the Copilot for Sales app in Outlook and Teams. The settings apply to the CRM environment that you sign in to. To customize Copilot for Sales for a different environment, [switch to that environment](sales-copilot-faq.md#how-can-i-switch-crm-environments).

1. Open the Copilot for Sales personal app in [Outlook](personal-app.md#open-the-personal-app-in-outlook) or [Teams](personal-app.md#open-the-personal-app-in-teams).
1. Sign in to [Outlook](sign-in-crm-outlook.md) or [Teams](sign-in-crm-teams.md) with your administrator credentials.  
1. On the left navigation pane, select **Copilot for Sales**. If **Copilot for Sales** isn't visible, select **View more apps** (**&hellip;**), and then select **Copilot for Sales**. If you see the **Copilot for Sales** window asking you to either add or open the app, select **Add** or **Open** to get the latest features.  
1. Select the **Settings** tab.  
1. Change the settings you need to.  
    **Tenant-level settings**:  
      - **Copilot AI**: [Controls who can use Copilot for Sales AI capabilities in all environments](suggested-replies.md#turn-on-copilot-ai-features-for-your-organization).
      - **Collaboration spaces**: [Controls whether AI-powered tasks should be suggested in collaboration spaces](turn-off-suggested-tasks-collab-space.md)  
    
    **Environment-level settings**:  
      - **Copilot AI**: [Turn on Copilot AI feature](suggested-replies.md#turn-on-copilot-ai-features-in-your-environment) for your environment.      
      - **Save to (CRM)**: [Configure fields that sellers can use to categorize emails and meetings in CRM](save-additional-details-outlook.md).
      - **Forms**: [Determines what information is displayed in Copilot for Sales in Outlook and Teams](customize-forms-and-fields.md). You can also control which records and fields sellers can edit directly in Copilot for Sales.
      - **Extensions**: [Integrates Copilot for Sales with other applications](use-extensions.md) to enhance its functionality and provide more insights for your sellers.
      
    :::image type="content" source="media/viva-sales-tenant-admin.png" alt-text="Screenshot showing admin settings.":::

## Add the Copilot for Sales app to Teams

If the Copilot for Sales app isn't already added to Teams, you can add it from the Teams app store. Note that the app is added only for you, not for your entire organization.

1. Sign in to Microsoft Teams with your administrator credentials.  
1. In the navigation bar on the left, select **Apps**.  
1. Search for **Copilot for Sales** and select it, and then select **Add**.  

