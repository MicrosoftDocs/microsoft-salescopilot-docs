---
title: Sales Copilot deployment guide for Salesforce CRM customers
description: Learn how to deploy Sales Copilot for Salesforce CRM customers.
ms.date: 10/09/2023
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Sales Copilot deployment guide for Salesforce CRM customers



Follow the instructions in this guide to deploy Sales Copilot for your Salesforce CRM customers. Here's a quick video overview of the steps involved:

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW10Mca]

## Prerequisites

- You must be a tenant administrator to install the integrated app from the [Microsoft 365 admin center](https://admin.microsoft.com/). [How do I find my tenant admin?](#how-do-i-find-my-tenant-admin)
- You must be a Teams administrator to create a setup policy in the [Teams admin center](https://admin.teams.microsoft.com/dashboard).

## Step 1: Install and deploy the Sales Copilot Outlook Add-in

[Install Sales Copilot Add-in for Outlook](install-viva-sales-as-an-integrated-app.md)

![Screenshot showing Sales Copilot installed as an add-in for Outlook.](media/install-viva-sales.png "Screenshot showing Sales Copilot installed as an integrated app.")

> [!NOTE]
> It can take up to 24 hours for the add-in to show up for your users.

## Step 2: Create a setup policy to auto install and pin the Sales Copilot app in Teams

[Install and pin Sales Copilot in your sellers' personal Teams environment and meetings they create](install-pin-viva-sales-teams.md)

![Screenshot showing Teams policy.](media/teams-policy-viva-sales.png "Screenshot showing Teams policy.")

## Step 3: Enable Teams meeting transcripts

Enable transcripts for Teams calls so that when Sales Copilot is added to a recorded Teams meeting, it can generate a meeting summary.

1.  Sign in to the [Teams admin center](https://admin.teams.microsoft.com).

2.  In the left pane, select **Meetings** &gt; **Meeting policies**.

3.  On the **Manage policies** tab, select **Global (Org-wide default)**.

5.  On the **Global (Org-wide default)** page, scroll down to the **Recording & transcription** section, and turn on the **Transcription** toggle.

6.  Select **Save**.

    ![Screenshot showing how to enable transcription in Teams admin center ](media/enable-transcription-teams.png "Screenshot showing how to enable transcription in Teams admin center.")

## Step 4: Confirm users have the right security roles

Sales Copilot applies your organization's existing CRM access controls and user permissions. Administrators must have correct permissions to customize their CRM systems, and users must have the correct permissions to view, update, and create records in their CRM systems from Sales Copilot.

Salesforce administrators who need to customize Sales Copilot must have the following permissions. More information: [Privileges required to use Sales Copilot](install-viva-sales.md#privileges-required-to-use-sales-copilot)

|Requirement type|You must have|
|---------------|-------------|
|Permission|User profile needs to have Modify All Data or Manage Data Integrations permission|

## Step 5: Ensure Microsoft Power Platform isn't blocked

Sales Copilot uses the Power Platform connector to connect to Salesforce CRM. Ensure that the connector is enabled for the Sales Copilot users.

1. Sign in to Salesforce CRM as an administrator.

2. Go to **Setup** > **Platform Tools** > **Apps** > **Connected Apps** > **Managed Connected Apps**.

3. Ensure that **Microsoft Power Platform** is listed under **Connected Apps**.

    > [!NOTE]
    > If **Microsoft Power Platform** is not listed under **Connected Apps**, go to the **Connected Apps OAuth Usage** page, and then select **Install** for Microsoft Power Platform.

4. Select **Microsoft Power Platform** to view details about the connected app. 

5. Under **OAuth Policies**, ensure that the value for Permitted Users is set to **Admin approved users are pre-authorized** or **All users may self-authorize**.

    > [!NOTE]
    > If **Admin approved users are pre-authorized** is selected, you must explicitly grant permissions to individual users through policies and permissions sets.

6. Under **Profiles** or **Permission Sets**, check whether there are any existing profiles or permission sets or if they're empty. Check and add the appropriate target for your users.

## Step 6: First user sign in

When the first user in the tenant connects to Salesforce CRM, Sales Copilot provisions a Dataverse environment to store the data generated  while using Sales Copilot. Refer to [Sales Copilot architecture](architecture.md) for more details on how the environment is used and what data is stored.

Sales Copilot automatically sets one of the Power Platform administrators or Microsoft 365 global administrators as the environment administrator. We recommend you review the administrators in the environment after it is created to ensure that the right users are set as administrators.

> [!NOTE]
> The first user connecting to Salesforce CRM from Sales Copilot will see an error if they are not an admin user and trial environment creation by non-admin users is disabled for the tenant in the Power platform admin center.
To avoid this error, it's recommended that the tenant administrator signs in to Salesforce CRM from Sales Copilot first. This creates a trial environment in Dataverse. Once the trial environment is created, other users can sign in to Sales Copilot. For information on how to sign in to Sales Copilot, see [Sign in to CRM](use-sales-copilot-outlook.md#sign-in-to-crm).


## Step 7 (optional): Customize Sales Copilot

[Administrator settings](administrator-settings-for-viva-sales.md) control the seller's Sales Copilot experience in Outlook and Teams. You can customize the CRM fields that are shown on forms and whether Sales Copilot generates suggested email content.

![Screenshot showing Sales Copilot admin center ](media/viva-sales-admin-sf.png "Screenshot showing Sales Copilot admin center.")

### Customize forms and fields

Sales Copilot comes configured to allow users to be productive out-of-the-box. You can [customize forms and fields](customize-forms-and-fields.md) as needed.

![Screenshot showing form settings in Sales Copilot admin center ](media/viva-sales-forms-admin-sf.png "Screenshot showing form settings in Sales Copilot admin center.")

### Set up Copilot AI features

You can [set up AI features in Sales Copilot](suggested-replies.md) to use AI features that are in preview or generally available.

![Screenshot showing Copilot settings in Sales Copilot admin center ](media/viva-sales-replies-admin-sf.png "Screenshot showing Copilot settings in Sales Copilot admin center.")

## Step 8: Welcome sellers to Sales Copilot

Now that you've installed and configured Sales Copilot in Outlook and Teams, get your sellers to use it. Here's an example email message you can share.


| |
|---------|
|**Subject**: Welcome to Sales Copilot!</br><br>Dear Sellers,</br><br>Welcome to Sales Copilot, a new app that brings CRM data and AI-powered intelligence into your flow of work in Outlook and Teams.</br><br>See what Sales Copilot can do for you by [watching this short video](https://www.microsoft.com/en-us/videoplayer/embed/RW181Q6) and taking the [Microsoft Sales Copilot training](/training/modules/boost-sales-performance/). </br><br>**Step 1: Logging into Sales Copilot for the first time**</br><br>The [Use Sales Copilot in Outlook](use-sales-copilot-outlook.md) article shows you how to find Sales Copilot within Outlook, sign into your CRM system and pin the app pane.</br><br>**Additional resources**</br><br>The following articles guide you through using various Sales Copilot features:</br><ul></br><li>[Connect a contact to your CRM](connect-contact.md)</li></br><li>[Change the connected CRM contact](change-connected-crm-contact.md)</li></br><li>[Create a contact in your CRM from Sales Copilot](create-contact-crm-sales-copilot.md)</li></br><li>[Save Outlook activities to your CRM](save-outlook-activities-crm.md)</li></br><li>[View recent and upcoming activities](view-recent-upcoming-activities.md)</li></br><li>[View record details](view-record-details.md)</li></br><li>[Add private notes](add-personal-notes.md)</li></br><li>[Share a link to a CRM record](share-link-crm-record.md)</li></br><li>[Edit a CRM record](edit-crm-record.md)</li></br><li>[Use Copilot to kickstart email messages](use-copilot-kickstart-email-messages.md)</li></br><li>[Use Sales Copilot in Teams](use-sales-copilot-teams.md)</li></br><li>[Create a Teams meeting](create-teams-meeting.md)</li></br><li>[Generate a meeting summary](generate-meeting-summary.md)</li></br><li>[View and understand the meeting summary](view-understand-meeting-summary.md)</li></br><li>[Share a link to a CRM record](share-link-crm-record.md)</li></br><li>[View and update CRM record details](view-update-crm-record-details.md)</li></br></ul>**Troubleshooting**</br><br>See the [Sales Copilot troubleshooting guide](tsg-no-column.md) article for common problems and solutions.</br><br>For additional community help, visit the [Sales Copilot - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) page.</br><br>For ideas and suggestions, visit the [Microsoft Sales Copilot · Community](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) page.     |


## Community

We encourage all Sales Copilot users to visit and register on the [Sales Copilot community](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales). The community has:

-   Forums to connect with peers and discuss shared experiences.

-   Forums to contribute and receive support on common issues, which are routinely reviewed by our team of experts.

-   Spaces to [share ideas](https://feedbackportal.microsoft.com/feedback/forum/7fcacc26-460c-ed11-b83d-000d3a4d91d1) and engage with the product development team.

## FAQ

### Is Sales Copilot available for Salesforce CRM customers?

Sales Copilot is a generally available app for Salesforce CRM customers, [watch this short video to learn more](https://www.youtube.com/watch?v=hfDPogeGTHk).

A Microsoft 365 for Enterprise or Office 365 for Enterprise product license is required to use the Sales Copilot app in Outlook and Microsoft Teams.

### How does Sales Copilot work?

Sales Copilot uses an Outlook add-in and a Teams app to bring the context of your CRM into your sellers' workflows. [Learn more about Microsoft Sales Copilot](https://www.microsoft.com/microsoft-viva/sales).

### Is Sales Copilot safe and secure?

Sales Copilot is a certified Microsoft app. That means it meets our rigorous security and compliance standards.

Get information about license requirements, role requirements, and region availability in [Introduction to Microsoft Sales Copilot](introduction.md) and [Sales Copilot FAQ](tsg-no-column.md).


### How do I find my tenant admin?

[How to find your Microsoft 365 admin](https://support.microsoft.com/en-us/office/how-do-i-find-my-microsoft-365-admin-59b8e361-dbb6-407f-8ac3-a30889e7b99b).

You may also find your tenant admin's email address on the [Azure Active Directory admin center tenant properties page](https://aad.portal.azure.com/#view/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/~/Properties), if an administrator hasn't locked it down.

![Screenshot showing how to find tenant admin.](media/get-tenant-admin.png "Screenshot showing how to find tenant admin.")

### Are there any special browser settings needed to use Sales Copilot in the web versions of Outlook and Teams?

Users may need to change a few settings to get the best experience of Sales Copilot in Outlook and Teams on the web.

- **Edge**:
  - Turn on "Enable sites to save and read cookie data (recommended)."
  - Turn off "Block third-party cookies."

- **Safari**: Turn off "Prevent Cross-site tracking."

- **Chrome**: Turn off "Block third-party cookies."

The [Sales Copilot troubleshooting guide](tsg-no-column.md) can help with solutions for common issues.

