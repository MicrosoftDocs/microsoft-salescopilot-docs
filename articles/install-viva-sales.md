---
title: Install Sales Copilot (admin-deployed)
description: Learn what are the various ways to install Sales Copilot
ms.date: 04/11/2023
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Install Sales Copilot (admin-deployed)

You need to be a Microsoft 365 administrator to deploy and install the Sales Copilot add-in for Outlook. You need to be a Teams administrator to deploy and install Sales Copilot for Teams.

You can install Sales Copilot as an integrated app on multiple platforms or as an individual add-in on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft AppSource to install it in Outlook and assign users. If you start from AppSource, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator installs it for best performance and usability. 

The add-in is enabled in Teams but not installed. You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Sales Copilot app for Teams from AppSource, you'll install it to your personal scope only, not for your users.


> [!NOTE]
> - If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce.
> - It can take up to 24 hours for the add-in to show up for your users.

<br>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW10Mca]

## Privileges required to use Sales Copilot

Sales Copilot applies your organization's existing CRM access controls and user permissions. Administrators must have correct permissions to customize their CRM systems, and users must have the correct permissions to view, update, and create records in their CRM systems from Sales Copilot.

> [!NOTE]
> - If you've made changes in a user's permissions or security roles in your CRM, ask that user to sign out of Sales Copilot in Outlook and then sign in again for these changes to be reflected appropriately. 
> - Changes in user permissions or security roles in CRM can take up to 15 minutes to reflect in Sales Copilot app for Teams.

### Permissions required for Salesforce administrators

Salesforce administrators who need to customize Sales Copilot must have the following permissions.

|Requirement type  |You must have  |
|---------|---------|
|Permission    |  User profile needs to have **Modify All Data** or **Manage Data Integrations** permission <br><br> **Note**: Permissions need to be on the user's profile and not in permission sets assigned to the user.|

### Additional privileges required for Dynamics 365 customers

#### Dynamics 365 administrators

If you're using out-of-the-box System Administrator or System Customizer security roles, Sales Copilot administration privileges are added automatically.

If you're using custom security roles, you must assign the following security role and privilege to Dynamics 365 administrators who need to customize Sales Copilot. 

|Requirement type  |You must have  |
|---------|---------|
|Security role     | Sales Copilot Administrator |
|Privilege     | **Read** privilege on **User** table     |

#### Dynamics 365 sellers

If you're using the out-of-the-box Salesperson or Sales Manager security roles, Sales Copilot privileges are added automatically and no further action is required.

If you're using custom security roles, you must assign the following security role and privilege to Dynamics 365 sellers who need to use Sales Copilot.

|Requirement type  |You must have  |
|---------|---------|
|Security role     | Sales Copilot User |
|Privilege     | **Read** privilege on **User** table     |


The **Sales Copilot User** security role only compliments the custom security roles and does not replace them. If a custom security role assigned to sellers is missing any of the privileges included in Salesperson or Sales Manager security role, you might encounter errors specific to Dynamics 365 permission.

For information on how to assign security roles, see [Assign a security role to a user](/power-platform/admin/assign-security-roles).

To edit custom security roles to match with out-of-the-box Salesperson or Sales Manager role, see [Create or edit a security role to manage access](/power-platform/admin/create-edit-security-role).

For information on security roles and privileges, see [Security roles and privileges](/power-platform/admin/security-roles-privileges).

## Deploy Sales Copilot

Looking for step-by-step instructions on how to deploy Sales Copilot? Here are the Sales Copilot deployment guides:

- [Sales Copilot deployment guide for Dynamics 365 customers](deploy-viva-sales-d365.md)
- [Sales Copilot deployment guide for Salesforce CRM customers](deploy-viva-sales-sf.md)

## How to use Sales Copilot?

After you install Sales Copilot for your users, they can start using it in Outlook and Teams. For information on how to use Sales Copilot, see:

- [Use Sales Copilot in Outlook](use-sales-copilot-outlook.md)
- [Use Sales Copilot in Teams](use-sales-copilot-teams.md)

### See also

[Install Sales Copilot add-in for Outlook](install-viva-sales-as-an-integrated-app.md)<br>
[Install and pin Sales Copilot in Teams](install-pin-viva-sales-teams.md)
