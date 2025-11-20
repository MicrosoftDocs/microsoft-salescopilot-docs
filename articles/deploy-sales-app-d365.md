---
title: Sales app deployment guide for Dynamics 365 customers
description: Learn how to deploy Sales app for Dynamics 365 customers.
ms.date: 11/20/2025
ms.topic: install-set-up-deploy
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Sales app deployment guide for Dynamics 365 customers

Follow the instructions in this guide to deploy Sales app for your Dynamics 365 Sales customers.

## Prerequisites

- You must be a tenant administrator to install the integrated app from the [Microsoft 365 admin center](https://admin.microsoft.com/). [How do I find my tenant admin?](sales-m365-copilot-faq.md#how-do-i-find-my-tenant-admin)
- You must be a Teams administrator to create a setup policy in the [Teams admin center](https://admin.teams.microsoft.com/dashboard).
- You must assign the Microsoft 365 Copilot license to each user that will be using the product. [Learn more about assigning licenses from the Microsoft 365 admin center](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide&preserve-view=true)

## Step 1: Install Sales app in Outlook

[Install Sales app in Outlook](install-sales-as-an-integrated-app.md)

![Screenshot showing Sales app installed as an add-in for Outlook.](media/integrated-app-admin-center.png "Screenshot showing Sales app installed as an integrated app.")

## Step 2: Create a policy to automatically install and pin the Sales app in Teams

[Install and pin Sales app in your sellers' personal Teams environment and meetings they create](install-pin-sales-teams.md)

![Screenshot showing Teams policy.](media/teams-policy-viva-sales.png "Screenshot showing Teams policy.")

## Step 3: Enable Teams meeting transcripts

Enable transcripts for Teams calls so that when Sales app is added to a recorded Teams meeting, it can generate a meeting summary.

1.  Sign in to the [Teams admin center](https://admin.teams.microsoft.com).

2.  In the left pane, select **Meetings** &gt; **Meeting policies**.

3.  On the **Manage policies** tab, select **Global (Org-wide default)**.

5.  On the **Global (Org-wide default)** page, scroll down to the **Recording & transcription** section, and turn on the **Transcription** toggle.

6.  Select **Save**.

    ![Screenshot showing how to enable transcription in Teams admin center ](media/enable-transcription-teams.png "Screenshot showing how to enable transcription in Teams admin center.")

## Step 4: Set up server-side synchronization of emails and appointments

Sales app allows sellers to save Outlook emails and appointments to Dynamics 365. Saving Outlook activities to Dynamics 365 requires [server-side synchronization for emails and appointments](/power-platform/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks) to be enabled. While sellers can enable server-side synchronization for their own mailboxes when they save Outlook activities to Dynamics 365 using Sales app for the first time, you can simplify their experience by setting up server-side synchronization of emails and appointments for all Sales app users. 

For information about enabling server-side synchronization, see [Connect to Exchange Online](/power-platform/admin/connect-exchange-online). 

## Step 5: Confirm users have the right security roles

If you're using the following out-of-the-box Dynamics 365 Sales security roles, you don't need to do anything. Sales app privileges are added automatically for:

-   Primary sales roles: Salesperson or Sales Manager

-   Administration roles: System Administrator or System Customizer

If you're using custom security roles, [assign users the right roles and privileges required for Dynamics 365 customers](privileges.md#privileges-required-for-dynamics-365-customers).

## Step 6 (optional): Customize Sales app

[Administrator settings](administrator-settings-sales-app.md) control the seller's Sales app experience in Outlook and Teams. You can customize Sales app to meet your organization's needs.

### Set up Copilot AI features

You can [set up AI features in Sales app](suggested-replies.md) to use AI features that are in preview or generally available.

### Customize forms and fields

Sales app comes configured to allow users to be productive out-of-the-box. You can [customize forms and fields](customize-forms-and-fields.md) as needed.


## Step 7: Welcome sellers to Sales app

Now that you've installed and configured Sales app in Outlook and Teams, get your sellers to use it. Here's an example email message you can share.


| |
|---------|
|**Subject**: Welcome to Sales app!</br><br>Dear Sellers,</br><br>Welcome to Sales app, a new app that brings CRM data and AI-powered intelligence into your flow of work in Outlook and Teams.</br><br>See what Sales app can do for you by taking the [Sales app training](/training/modules/boost-sales-performance/). </br><br>**Step 1: Logging into Sales app for the first time**</br><br>[Sign in to your CRM system](sign-in-crm-outlook.md) and [pin the app](open-app.md#pin-the-sales-app-in-outlook).</br><br>**Additional resources**</br><br>The following articles guide you through using various Sales app features:</br><ul></br><li>[Connect a contact to your CRM](connect-contact.md)</li></br><li>[Change the connected CRM contact](change-connected-crm-contact.md)</li></br><li>[Create a contact in your CRM from Sales app](create-contact-crm.md)</li></br><li>[Save Outlook activities to your CRM](save-outlook-activities-crm.md)</li></br><li>[View recent and upcoming activities](view-recent-upcoming-activities.md)</li></br><li>[View record details](view-record-details.md)</li></br><li>[Add private notes](add-personal-notes.md)</li></br><li>[Share a link to a CRM record](share-link-crm-record.md)</li></br><li>[Edit a CRM record](edit-crm-record.md)</li></br><li>[Draft email messages](use-copilot-kickstart-email-messages.md)</li></br><li>[Generate a meeting summary](create-teams-meeting.md#generate-a-meeting-summary)</li></br><li>[View sales insights in Microsoft Teams meeting recap](view-meeting-summary-recap.md)</li></br><li>[Share a link to a CRM record](share-link-crm-record.md)</li></br><li>[View and update CRM record details](view-update-crm-record-details.md)</li></br></ul>**Troubleshooting**</br><br>See the [Sales app troubleshooting guide](troubleshoot.yml) article for common problems and solutions.</br><br>For additional community help, visit the [Sales app - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) page.</br><br>For ideas and suggestions, visit the [Sales app Community](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) page.     |

> [!IMPORTANT]
> - It can take up to 48 hours for the app to appear in Outlook and other Microsoft 365 apps. If users can't see the app after 48 hours, it might be due to the public attachment handling policy. More information: [Why can't users see the Sales app in Outlook after it's deployed?](sales-m365-copilot-faq.md#why-cant-users-see-the-sales-app-in-outlook-after-its-deployed)
> - Sales app doesn't support multiple tenants. It uses Microsoft Entra ID credentials to authenticate end users, so access is restricted to environments in the same tenant.
> - Users added as guests to a tenant can't access Sales app.

## Community

We encourage all Sales app users to visit and register on the [Sales app community](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales). The community has:

-   Forums to connect with peers and discuss shared experiences.

-   Forums to contribute and receive support on common issues, which are routinely reviewed by our team of experts.

-   Spaces to [share ideas](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) and engage with the product development team.


