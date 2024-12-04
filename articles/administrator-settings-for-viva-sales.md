---
title: Administrator settings for Copilot for Sales
description: Learn how to use administrator settings to customize the Microsoft 365 Copilot for Sales experience in Outlook and Teams.
ms.date: 12/04/2024
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

- [The Copilot for Sales app is added to Teams](#add-the-copilot-for-sales-app-to-teams).
- You have the latest version of the Copilot for Sales app in Teams. [Learn how to update an app in Teams](https://support.microsoft.com/office/update-an-app-in-teams-3d53d136-5c5d-4dfa-9602-01e6fdd8015b).

## Who can access administrator settings?

Administrator settings are visible only when you sign in with administrator credentials to Copilot for Sales in Outlook. The permissions you need depend on which CRM you use.

- **Dynamics 365:** You must have the **System Administrator** or **System Customizer** role. If you're using a custom security role, you might need [more privileges to use Copilot for Sales](install-viva-sales.md#privileges-required-for-dynamics-365-customers).

- **Salesforce:** Your user profile must have the **Modify All Data** or **Manage Data Integrations** permission. Permissions need to be set in your user profile, not in a permission set that's assigned to you.

If you change a user's permissions or security roles in your CRM, ask the user to sign out of Copilot for Sales in Outlook and sign in again for your changes to be reflected. Changes in user permissions or security roles in the CRM can take up to 15 minutes to reflect in the Copilot for Sales app in Teams.

## Access administrator settings

Teams and Outlook both play a part in how you access the Copilot for Sales administrator settings and what you can change.

You can access the administrator settings only in the Copilot for Sales app in Teams. The settings apply to the CRM environment that you sign in to in Copilot for Sales in Outlook. To customize Copilot for Sales for a different environment, [switch to that environment in Outlook](#how-can-i-switch-crm-environments).

1. [Open the Copilot for Sales app in Outlook](open-app.md#access-copilot-for-sales-in-outlook) and [sign in](sign-in-crm-outlook.md) with your administrator credentials.  
1. Sign in to Teams with your administrator credentials.  
1. In the Teams navigation bar, select **Copilot for Sales**. If **Copilot for Sales** isn't visible, select **View more apps** (**&hellip;**), and then select **Copilot for Sales**. If you see the **Copilot for Sales** window asking you to either add or open the app, select **Add** or **Open** to get the latest features.  
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

    :::image type="content" source="./media/viva-sales-admin.png" alt-text="Screenshot of the Copilot for Sales Settings tab in Teams.":::

## Add the Copilot for Sales app to Teams

If the Copilot for Sales app isn't already added to Teams, you can add it from the Teams app store. Note that the app is added only for you, not for your entire organization.

1. Sign in to Microsoft Teams with your administrator credentials.  
1. In the navigation bar on the left, select **Apps**.  
1. Search for **Copilot for Sales** and select it, and then select **Add**.  

