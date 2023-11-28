---
title: Administrator settings for Sales Copilot
description: Learn how to use administrator settings to customize the Microsoft Sales Copilot experience in Outlook and Teams.
ms.date: 11/13/2023
ms.topic: how-to
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:11/28/2023
  - bap-template
---

# Administrator settings for Sales Copilot

As a tenant administrator or CRM (customer relationship management) administrator, you can use administrator settings to customize how your users experience Sales Copilot in Outlook and Teams, including who can use AI capabilities, for all environments in your organization.

## Prerequisites

- [The Sales Copilot app is added to Teams](#add-the-sales-copilot-app-to-teams).
- You have the latest version of the Sales Copilot app in Teams. [Learn how to update an app in Teams](https://support.microsoft.com/office/update-an-app-in-teams-3d53d136-5c5d-4dfa-9602-01e6fdd8015b).

## Who can access administrator settings?

Administrator settings are visible only when you sign in with administrator credentials to Sales Copilot in Outlook. The permissions you need depend on which CRM you use.

- **Dynamics 365:** You must have the System Administrator or System Customizer role. If you're using a custom security role, you might need [more privileges to use Sales Copilot](install-viva-sales.md#additional-privileges-required-for-dynamics-365-customers).

- **Salesforce:** Your user profile must have the Modify All Data or Manage Data Integrations permission. Permissions need to be set in your user profile, not in a permission set that's assigned to you.

If you change a user's permissions or security roles in your CRM, ask the user to sign out of Sales Copilot in Outlook and sign in again for your changes to be reflected. Changes in user permissions or security roles in the CRM can take up to 15 minutes to reflect in the Sales Copilot app in Teams.

## Access administrator settings

Teams and Outlook both play a part in how you access the Sales Copilot administrator settings and what you can change.

- You can access the administrator settings only in the Sales Copilot app in Teams.
- The settings apply to the CRM environment that you sign in to in Sales Copilot in Outlook. To customize Sales Copilot for a different environment, [switch to that environment in Outlook](#how-can-i-switch-crm-environments).

1. [Sign in to Sales Copilot in Outlook](use-sales-copilot-outlook.md) with your administrator credentials.

1. On the **Welcome to Sales Copilot!** page, select **Sign in to get started**, and then select your CRM and environment.

1. Sign in to Teams with your administrator credentials.

1. In the Teams navigation bar, select **Sales Copilot**. If **Sales Copilot** isn't visible, select **View more apps** (**&hellip;**), and then select **Sales Copilot**.

1. Select the **Settings** tab.

1. Change the settings you need to.

    **Tenant-level settings**:

      - **Copilot**: [Controls who can use Sales Copilot AI capabilities in all environments](suggested-replies.md#tenant-administrator-settings).

    **Environment-level settings**:

      - **Copilot**: [Helps sellers write better emails and stay on top of their deals with AI-driven insights](suggested-replies.md#crm-administrator-settings).
      - **Forms**: [Determines what information is displayed in Sales Copilot in Outlook and Teams](customize-forms-and-fields.md). You can also control which records and fields sellers can edit directly in Sales Copilot.
      - **Extensions**: [Integrates Sales Copilot with other applications](use-extensions.md) to enhance its functionality and provide more insights for your sellers.

    :::image type="content" source="./media/viva-sales-admin.png" alt-text="Screenshot of the Sales Copilot Settings tab in Teams.":::

## Add the Sales Copilot app to Teams
<!-- EDITOR'S NOTE: 1. There's a separate article about installing the Sales Copilot app in Teams. Am I correct in thinking that article covers installing Sales Copilot for everyone, and this section covers installing it just for the admin? If that's true, can you please add a sentence here to make that clear? 2. If the admin settings aren't available outside of the Sales Copilot app in Teams, shouldn't this section come before you talk about the admin settings?-->

1. Sign in to Microsoft Teams with your administrator credentials.

2. In the navigation bar on the left, select **Apps**.

3. Search for **Sales Copilot** and select it, and then select **Add**.

## FAQ

### Can I access Sales Copilot administrator settings if I don't have Microsoft Teams?

Administrator settings are accessible only in the Sales Copilot app in Teams.

### Which CRM environment do the administrator settings apply to?

The settings are specific to the environment you're signed in to in Sales Copilot in Outlook. If you want to customize Sales Copilot for another environment, you must [switch to that environment in Outlook](#how-can-i-switch-crm-environments).

### How can I switch CRM environments?

If your organization provides multiple environments for you and your sellers to work in, make sure you're signed in to the right one in Outlook before you change any Sales Copilot settings in Teams. If you need to change a setting in a different environment, switch to that environment first.

1. [Sign out of Sales Copilot in Outlook](sign-out-sales-copilot.md).

1. On the **Welcome to Sales Copilot!** page, select **Sign in to get started**, and then select your CRM and the environment you want to customize.

1. Come back to the Sales Copilot app in Teams and refresh the **Settings** tab to confirm you're working in the correct environment.

### Why do I see the message "Sign in to Sales Copilot in Outlook first"?

You need to sign in to a CRM environment in Sales Copilot in Outlook before you can open the Sales Copilot **Settings** tab in Teams.

1. [Sign in to Sales Copilot in Outlook](use-sales-copilot-outlook.md) with your administrator credentials.

1. On the **Welcome to Sales Copilot!** page, select **Sign in to get started**, and then select your CRM and environment.

1. Come back to the Sales Copilot app in Teams and refresh the **Settings** tab.

### Why do I see the message "Settings are coming soon"?

You signed in to Sales Copilot in Outlook or Teams with an account that doesn't have admin rights. Personal settings for Sales Copilot will be accessible in the **Settings** tab soon.

If you're signed in with tenant administrator or CRM administrator credentials, you shouldn't see the "Settings are coming soon" message. You should see the administrator settings page. If you do see this message, make sure you have the [right permissions or security roles](#who-can-access-administrator-settings).

### Can I change the administrator settings on my mobile device?

Access to Sales Copilot administrator settings on a mobile device isn't supported. Work with administrator settings in the Teams desktop app.<!-- EDITOR'S NOTE: What about Teams on the web? -->

### Why can't I view the administrator settings in the Teams dark or high contrast theme?

The Teams dark and high contrast themes aren't supported.
