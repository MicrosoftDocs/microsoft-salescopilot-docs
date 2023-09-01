---
title: Use Sales Copilot in Microsoft Outlook
description: Learn how to use Sales Copilot in Outlook.
ms.date: 07/20/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Use Sales Copilot in Outlook

As a seller, you communicate with a lot of potential customers by email. Sales Copilot helps you prepare for your engagements. It gathers information from your CRM system and Microsoft Office and enriches it with actionable insights, so you can be more effective right where you spend most of your day. 

You can get related information from CRM at your fingertips, save activities (such as emails and meetings) to CRM, and get an overview of recent interactions with your customers.

If you don’t have access to Sales Copilot, ask your administrator to install it.

## Use Sales Copilot without signing in

You can use Sales Copilot and AI capabilities in Outlook without signing in to your CRM. You can use basic capabilities like [email drafting](use-copilot-kickstart-email-messages.md#create-an-email-reply-using-pre-defined-categories) and [email summarization](view-save-email-summary-crm.md) without signing in to your CRM. For a more enriched experience with CRM data, you must sign in to your Dynamics 365 or Salesforce CRM account. [Open Sales Copilot](#open-sales-copilot) to get started.

> [!NOTE]
> This feature is available only for customers in United States and Europe.

## Open Sales Copilot

You can open Sales Copilot using any of the following options:

### Outlook desktop

- While drafting an email or creating a meeting

    - Select **Sales Copilot** on the ribbon (in Classic ribbon)
     
        :::image type="content" source="media/sales-copilot-icon-desktop.png" alt-text="Screenshot showing Sales Copilot icon in Outlook desktop.":::
    
    - Select **More commands** (**...**) and then select **Sales Copilot** (in Simplified ribbon)
    
    - Select **Use Copilot now** in the banner message (for emails)
    
        :::image type="content" source="media/banner-message.png" alt-text="Screenshot showing Sales Copilot banner message.":::
    
    - Select **Show details** in the banner message (for meetings)

- While reading an email or opening a meeting

    - Select **Sales Copilot** on the ribbon (in Classic ribbon)
     
    - Select **More commands** (**...**) and then select **Sales Copilot** (in Simplified ribbon)

### Outlook on the web

- While drafting an email or creating a meeting

    - Select **Sales Copilot** on the ribbon (in Classic ribbon)
    
    - Select **More commands** (**...**) and then select **Sales Copilot** (in Simplified ribbon)
    
    - Select **Use Copilot now** in the banner message (for emails)
    
    - Select **Show summary** in the banner message (for meetings)
    
- While reading an email

    - Select **More commands** (**...**) and then select **Sales Copilot**.

- While opening a meeting

    - Select **Sales Copilot** on the ribbon (in Classic ribbon)
    
    - Select **More commands** (**...**) and then select **Sales Copilot** (in Simplified ribbon)

## Sign in to CRM

After you open Sales Copilot, you can sign in to Sales Copilot and connect your CRM account to get a more enriched experience with CRM data.

### Automatically sign in

If you have any Dynamics 365 environment (production or non-production) that has the Sales Copilot solution, you are signed in automatically to your environment the first time you open the Sales Copilot pane. The environment you are signed in to is selected per the following rules:


|Scenario  |Auto sign-in rule  |You will see  |
|---------|---------|---------|
|Single environment (production or non-production)     |  Signed in to the available environment       | Message at the top of Sales Copilot pane        |
|Single production environment and multiple non-production environments     |Signed in to the production environment         |  Message at the top of Sales Copilot pane       |
|Multiple production and non-production environments     |  Signed in to the first production environment       |  Dialog box to confirm or change the signed in environment       |
|Multiple non-production environments but no production environment     |  Signed in to the first non-production environment       |  Dialog box to confirm or change the signed in environment       |

> [!NOTE]
> Sales Copilot does not have access to data on your most frequently accessed or most recently accessed environment to automatically sign in. Sales Copilot fetches a list of environments having the Sales Copilot solution, and then selects the first environment in the list to automatically sign in to.

#### Single environment or single production environment

For first and second scenarios, a message is displayed at the top of the Sales Copilot pane showing the environment the user was signed in to automatically. It includes a link to change the environment or CRM.

:::image type="content" source="media/single-env.png" alt-text="Screenshot showing signed in to a single environment.":::

To change the environment or CRM, select **Switch environment**. In the **Signed in to Dynamics 365** dialog box, select another environment from the **Environment** list, and then select **OK**. The **Environment** list displays the friendly name, type (Production/Sandbox), and URL for each environment.

:::image type="content" source="media/single-env-switch.png" alt-text="Screenshot showing environment switcher for a when signed in to a single environment.":::

To sign in to Salesforce CRM, select **Sign in to Salesforce® CRM** and then follow the steps shown in the wizard.

#### Multiple environments

For third and fourth scenarios, a dialog box is displayed to confirm the environment the user has been signed in to, or to select another environment. Select **OK** to confirm the environment or select another environment from the **Environment** list. 

:::image type="content" source="media/multiple-env-switch.png" alt-text="Screenshot showing environment confirmation a when there are multiple environments.":::

To sign in to Salesforce CRM, select **Sign in to Salesforce® CRM** and then follow the steps shown in the wizard.

The **Environment** list displays the friendly name, type (Production/Sandbox), and URL for each environment.

:::image type="content" source="media/env-list.png" alt-text="Screenshot showing the environment list.":::

### Manually sign in

You must manually sign in to your CRM in the following cases:

- If you are using Dynamics 365 environment and have signed out of your CRM from Sales Copilot

- If you are using Salesforce CRM

You can use basic capabilities of Sales Copilot without signing in to your CRM. However, to use all the advanced capabilities of Sales Copilot, you must sign in to your CRM.

1. In the **Sales Copilot** pane, select **Sign in** in the banner at the top or card at the bottom.

    :::image type="content" source="media/manual-sign-in.png" alt-text="Screenshot showing sign in button.":::

2. Select **Sign in to your CRM** and sign in to your CRM using one of the following options:

    - **Salesforce CRM**: Select your Salesforce environment, and then select **Sign in**. In the confirmation message, select **Allow**. Enter your Salesforce credentials, and then select **Log In**. Select **Allow**, and then select **Allow access**.
    
    - **Dynamics 365**: You’re signed in automatically using your Office credentials. Select your Dynamics 365 environment, and then select **Get started**.

        Your Dynamics 365 environment matches the URL your browser shows when you sign in to Dynamics 365. For example, if the URL is `salesorg.crm.dynamics.com`, select **salesorg.crm.dynamics.com** in the list.
        
        :::image type="content" source="media/sign-in-crm.png" alt-text="Screenshot showing sign in to your CRM button.":::

    Once you are signed in, the Sales Copilot pane is populated with personalized action items and relevant CRM information to help you work more efficiently. 

## Pin the Sales Copilot app

To keep Sales Copilot in view as you move through your emails and meetings, pin it so that the app pane stays open.

To pin the app, select the pushpin :::image type="icon" source="media/pin-app.png" border="false":::. To unpin it, select the pushpin :::image type="icon" source="media/unpin-app.png" border="false"::: again.

## Anatomy of the Sales Copilot pane

### Highlights tab

:::image type="content" source="media/anatomy-highlights-tab.png" alt-text="Screenshot showing anatomy of the Highlights tab.":::

|Annotation| Description|
|----------|------------|
|1|Sender name and timestamp of received email.|
|2|Indication that the email is saved to CRM. More information: [Save Outlook activities to your CRM](save-outlook-activities-crm.md)|
|3|Generate email content using Copilot capabilities in Sales Copilot. More information: [Use Copilot to kickstart email messages](use-copilot-kickstart-email-messages.md)|
|4|Add external contacts to your CRM. More information: [Create a contact in your CRM from Sales Copilot](create-contact-crm-sales-copilot.md)|
|5|Pin or unpin the app pane.|
|6|Close the app pane.|
|7|Options menu|

### CRM tab

:::image type="content" source="media/anatomy-crm-tab.png" alt-text="Screenshot showing anatomy of the CRM tab.":::

|Annotation|Description|
|----------|-----------|
|1|Options menu to change the connected record.|
|2|Record to which email is connected. More information: [Save Outlook activities to your CRM](save-outlook-activities-crm.md)|
|3|Contacts associated with the email. Select a contact to open its details.|
|4|Account associated with the email. Select the record to open its details. You can also hover over the record and then select **More actions** (**...**) to copy link to the record or open it in your connected CRM. <br>**Note**: The option to edit a record is available only when it is enabled by your administrator.|
|5|Opportunities associated with the email. Select a record to open its details. You can also hover over a record and then select **More actions** (**...**) to copy link to the record or open it in your connected CRM.<br>**Note**: The option to edit a record is available only when it is enabled by your administrator.|

### Saved contact details

:::image type="content" source="media/anatomy-saved-contact.png" alt-text="Screenshot showing anatomy of saved contact details.":::

|Annotation|Description|
|----------|-----------|
|1|Contact name along with two key fields as configure by your administrator.|
|2|Indication that contact is saved to CRM. More information: [Create a contact in your CRM from Sales Copilot](create-contact-crm-sales-copilot.md)|
|3|Private notes card to enter personal notes for a contact. These notes are private to you and not saved to CRM system.|
|4|Options menu. Allows you to edit the contact, copy link to the contact, and open it in your connected CRM.<br>**Note**: The option to edit a record is available only when it is enabled by your administrator.|
|5|The customer’s contact information|
|6|Opportunities associated with the contact. Select a record to open its details. You can also hover over a record and then select **More actions** (**...**) to copy link to the record or open it in your connected CRM.<br>**Note**: The option to edit a record is available only when it is enabled by your administrator.|
|7|Account associated with the contact. Select the record to open its details. You can also hover over the record and then select **More actions** (**...**) to copy link to the record or open it in your connected CRM.<br>**Note**: The option to edit a record is available only when it is enabled by your administrator.|
|8|Recent emails and meetings (previous and upcoming) with the contact. More information: [View recent and upcoming activities](view-recent-upcoming-activities.md)|