---
title: Copilot for Sales deployment guide for Salesforce CRM customers
description: Learn how to deploy Copilot for Sales for Salesforce CRM customers.
ms.date: 06/20/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Copilot for Sales deployment guide for Salesforce CRM customers

Follow the instructions in this guide to deploy Copilot for Sales for your Salesforce CRM customers. Here's a quick video overview of the steps involved:

<br>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1kFRW]

## Prerequisites

- You must be a tenant administrator to install the integrated app from the [Microsoft 365 admin center](https://admin.microsoft.com/). [How do I find my tenant admin?](sales-copilot-faq.md#how-do-i-find-my-tenant-admin)
- You must be a Teams administrator to create a setup policy in the [Teams admin center](https://admin.teams.microsoft.com/dashboard).
- You must assign the Copilot for Sales license to each user that will be using the product. [Learn more about assigning licenses from the Microsoft 365 admin center](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide&preserve-view=true)

## Step 1: Install Copilot for Sales in Outlook

[Install Copilot for Sales in Outlook](install-viva-sales-as-an-integrated-app.md)

![Screenshot showing Copilot for Sales installed as an add-in for Outlook.](media/integrated-app-admin-center.png "Screenshot showing Copilot for Sales installed as an integrated app.")

> [!NOTE]
> It can take up to 24 hours for the add-in to show up for your users.

## Step 2: Create a setup policy to auto install and pin the Copilot for Sales app in Teams

[Install and pin Copilot for Sales in your sellers' personal Teams environment and meetings they create](install-pin-viva-sales-teams.md)

![Screenshot showing Teams policy.](media/teams-policy-viva-sales.png "Screenshot showing Teams policy.")

## Step 3: Enable Teams meeting transcripts

Enable transcripts for Teams calls so that when Copilot for Sales is added to a recorded Teams meeting, it can generate a meeting summary.

1.  Sign in to the [Teams admin center](https://admin.teams.microsoft.com).

2.  In the left pane, select **Meetings** &gt; **Meeting policies**.

3.  On the **Manage policies** tab, select **Global (Org-wide default)**.

5.  On the **Global (Org-wide default)** page, scroll down to the **Recording & transcription** section, and turn on the **Transcription** toggle.

6.  Select **Save**.

    ![Screenshot showing how to enable transcription in Teams admin center ](media/enable-transcription-teams.png "Screenshot showing how to enable transcription in Teams admin center.")

## Step 4: Confirm users have the right security roles

Copilot for Sales applies your organization's existing CRM access controls and user permissions. Administrators must have correct permissions to customize their CRM systems, and users must have the correct permissions to view, update, and create records in their CRM systems from Copilot for Sales.

Salesforce administrators who need to customize Copilot for Sales [must have appropriate permissions](install-viva-sales.md#permissions-required-for-salesforce-administrators).

Users of Copilot for Sales need to be API enabled in Salesforce so that they can access Salesforce using APIs. [Learn how to grant API Enabled permission](tsg-api-perm.md).

## Step 5: Ensure Salesforce connector isn't blocked in Power Platform

If there are Data Loss Prevention (DLP) policies defined in Power Platform for the msdyn_viva environment, ensure that the Salesforce connector is on the allow list. [Learn more about allowing Salesforce connector in the DLP policy](tsg-blocked-connector-sf.md)

## Step 6: Ensure Microsoft Power Platform connected app isn't blocked in Salesforce

Copilot for Sales uses the Power Platform connector to connect to Salesforce CRM. Ensure that the connector is enabled for the Copilot for Sales users.

1. Sign in to Salesforce CRM as an administrator.

2. Go to **Setup** > **Platform Tools** > **Apps** > **Connected Apps** > **Managed Connected Apps**.

3. Ensure that **Microsoft Power Platform** is listed under **Connected Apps**.

    > [!NOTE]
    > If **Microsoft Power Platform** is not listed under **Connected Apps**, go to the **Connected Apps OAuth Usage** page, and then select **Install** for Microsoft Power Platform.

4. Select **Microsoft Power Platform** to view details about the connected app. 

5. Under **OAuth Policies**, ensure that you've set the following values:

    1. Value for **Permitted Users** is set to **Admin approved users are pre-authorized** or **All users may self-authorize**.

        > [!NOTE]
        > If **Admin approved users are pre-authorized** is selected, you must explicitly grant permissions to individual users through policies and permissions sets.

    2. Value for **IP Relaxation** is set to **Relax IP restrictions**.
    3. Value for **Refresh Token Policy** is set to **Refresh token is valid until revoked**.

6. Under **Session Policies**, ensure that the value for **Timeout Value** is set to **None**.

7. Under **Profiles** or **Permission Sets**, check whether there are any existing profiles or permission sets or if they're empty. Check and add the appropriate target for your users.

## Step 7: First user sign in

When the first user in the tenant connects to Salesforce CRM, Copilot for Sales provisions a Dataverse environment to store the data generated  while using Copilot for Sales. Refer to [Copilot for Sales architecture](architecture.md) for more details on how the environment is used and what data is stored.

Copilot for Sales automatically assigns all the Power Platform administrators and Microsoft 365 global administrators as the System Administrator role in the **Trial** environment. We recommend you review the administrators in the environment after it is created to ensure that the right users are set as administrators.

> [!NOTE]
> The first user connecting to Salesforce CRM from Copilot for Sales will see an error if they are not an admin user and trial environment creation by non-admin users is disabled for the tenant in the Power platform admin center.
To avoid this error, it's recommended that the tenant administrator signs in to Salesforce CRM from Copilot for Sales first. This creates a trial environment in Dataverse. Once the trial environment is created, other users can sign in to Copilot for Sales. For information on how to sign in to Copilot for Sales, see [Sign in to CRM](use-sales-copilot-outlook.md#sign-in-to-crm).


## Step 8 (optional): Customize Copilot for Sales

[Administrator settings](administrator-settings-for-viva-sales.md) control the seller's Copilot for Sales experience in Outlook and Teams. You can customize Copilot for Sales to meet your organization's needs.

### Set up Copilot AI features

You can [set up AI features in Copilot for Sales](suggested-replies.md) to use AI features that are in preview or generally available.

### Customize forms and fields

Copilot for Sales comes configured to allow users to be productive out-of-the-box. You can [customize forms and fields](customize-forms-and-fields.md) as needed.

### Integrate with other applications

You can [integrate Copilot for Sales with other applications](use-extensions.md) to extend the capabilities of Copilot for Sales.

## Step 9: Welcome sellers to Copilot for Sales

Now that you've installed and configured Copilot for Sales in Outlook and Teams, get your sellers to use it. Here's an example email message you can share.


| |
|---------|
|**Subject**: Welcome to Copilot for Sales!</br><br>Dear Sellers,</br><br>Welcome to Copilot for Sales, a new app that brings CRM data and AI-powered intelligence into your flow of work in Outlook and Teams.</br><br>See what Copilot for Sales can do for you by [watching this short video](https://www.microsoft.com/en-us/videoplayer/embed/RW181Q6) and taking the [Microsoft Copilot for Sales training](/training/modules/boost-sales-performance/). </br><br>**Step 1: Logging into Copilot for Sales for the first time**</br><br>[Access Copilot for Sales in Outlook](open-app.md#access-copilot-for-sales-in-outlook), [sign in to your CRM system](sign-in-crm-outlook.md), and [pin the app](open-app.md#pin-the-copilot-for-sales-app-in-outlook).</br><br>**Additional resources**</br><br>The following articles guide you through using various Copilot for Sales features:</br><ul></br><li>[Connect a contact to your CRM](connect-contact.md)</li></br><li>[Change the connected CRM contact](change-connected-crm-contact.md)</li></br><li>[Create a contact in your CRM from Copilot for Sales](create-contact-crm-sales-copilot.md)</li></br><li>[Save Outlook activities to your CRM](save-outlook-activities-crm.md)</li></br><li>[View recent and upcoming activities](view-recent-upcoming-activities.md)</li></br><li>[View record details](view-record-details.md)</li></br><li>[Add private notes](add-personal-notes.md)</li></br><li>[Share a link to a CRM record](share-link-crm-record.md)</li></br><li>[Edit a CRM record](edit-crm-record.md)</li></br><li>[Draft email messages](use-copilot-kickstart-email-messages.md)</li></br><li>[Generate a meeting summary](generate-meeting-summary.md)</li></br><li>[View and understand the meeting summary](view-understand-meeting-summary.md)</li></br><li>[Share a link to a CRM record](share-link-crm-record.md)</li></br><li>[View and update CRM record details](view-update-crm-record-details.md)</li></br></ul>**Troubleshooting**</br><br>See the [Copilot for Sales troubleshooting guide](troubleshoot.yml) article for common problems and solutions.</br><br>For additional community help, visit the [Copilot for Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) page.</br><br>For ideas and suggestions, visit the [Microsoft Copilot for Sales · Community](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) page.     |

> [!IMPORTANT]
> It can take up to 48 hours for the app to appear in Outlook and other Microsoft 365 apps. If users can't see the app after 48 hours, it might be due to the public attachment handling policy. More information: [Why can't users see the Copilot for Sales app in Outlook after it's deployed?](sales-copilot-faq.md#why-cant-users-see-the-copilot-for-sales-app-in-outlook-after-its-deployed)

## Community

We encourage all Copilot for Sales users to visit and register on the [Copilot for Sales community](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales). The community has:

-   Forums to connect with peers and discuss shared experiences.

-   Forums to contribute and receive support on common issues, which are routinely reviewed by our team of experts.

-   Spaces to [share ideas](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) and engage with the product development team.

