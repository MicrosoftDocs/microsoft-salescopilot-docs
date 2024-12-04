---
title: Install Copilot for Sales (admin-deployed)
description: Learn what are the various ways to install Copilot for Sales
ms.date: 11/29/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Install Copilot for Sales (admin-deployed)

You can install Copilot for Sales as an integrated app on multiple platforms or as an individual app on a single platform. Whichever method you choose, you can start from either the Microsoft 365 admin center or Microsoft AppSource to install it in Outlook and assign users. If you start from AppSource, you'll finish installation in the Microsoft 365 admin center. Either way, we recommend an administrator installs it for best performance and usability.  

You need to go to the Microsoft Teams admin center and create setup policies to install the app and assign users. If you install the Copilot for Sales app for Teams from AppSource, you'll install it to your personal scope only, not for your users.

You need to be a Microsoft 365 administrator to deploy and install the Copilot for Sales add-in for Outlook and Microsoft 365 apps. You need to be a Teams administrator to deploy and install Copilot for Sales for Teams.

> [!NOTE]
> If your users are using Salesforce, ensure that Microsoft Power Platform is not blocked. You can check its status on the **Connected Apps OAuth Usage** page in Salesforce. If it's blocked, you need to unblock it to use Copilot for Sales and might take up to 24 hours for the add-in to show up for your users.

Watch this video to learn how to install Copilot for Sales in Outlook and Teams:

> [!VIDEO da2701bb-06f0-49e0-b757-80c584af69f7]

## Privileges required to use Copilot for Sales

Copilot for Sales applies your organization's existing CRM access controls and user permissions. Administrators must have correct permissions to customize their CRM systems, and users must have the correct permissions to view, update, and create records in their CRM systems from Copilot for Sales.

> [!NOTE]
> - If you've made changes in a user's permissions or security roles in your CRM, ask that user to sign out of Copilot for Sales in Outlook and then sign in again for these changes to be reflected appropriately. 
> - Changes in user permissions or security roles in CRM can take up to 15 minutes to reflect in Copilot for Sales app for Teams.

### Permissions required for Salesforce administrators

Salesforce administrators who need to customize Copilot for Sales must have the following permissions.

|Requirement type  |You must have  |
|---------|---------|
| Permission | User profile needs to have **Modify All Data** or **Manage Data Integrations** permission.<br>**Note**: Permissions need to be on the user's profile and not in permission sets assigned to the user.|

### Privileges required for Dynamics 365 customers

#### Dynamics 365 administrators

If you're using out-of-the-box **System Administrator** or **System Customizer** security roles, Copilot for Sales administration privileges are added automatically.  
If you're using custom security roles, you must assign the following security role and privilege to Dynamics 365 administrators who need to customize Copilot for Sales.  

|Requirement type  |You must have  |
|------------------|---------------|
| Security role | Copilot for Sales Administrator |
| Privilege | **Read** privilege on **User** table |

#### Dynamics 365 sellers

If you're using the out-of-the-box Salesperson or Sales Manager security roles, Copilot for Sales privileges are added automatically and no further action is required.  
If you're using custom security roles, you must assign the following security role and privilege to Dynamics 365 sellers who need to use Copilot for Sales.

|Requirement type  |You must have  |
|---------|---------|
|Security role | Copilot for Sales User |
|Privilege | **Read** privilege on **User** table |

The **Copilot for Sales User** security role only compliments the custom security roles and does not replace them. If a custom security role assigned to sellers is missing any of the privileges included in Salesperson or Sales Manager security role, you might encounter errors specific to Dynamics 365 permission.  
For information on how to assign security roles, see [Assign a security role to a user](/power-platform/admin/assign-security-roles).  
To edit custom security roles to match with out-of-the-box Salesperson or Sales Manager role, see [Create or edit a security role to manage access](/power-platform/admin/create-edit-security-role).  
For information on security roles and privileges, see [Security roles and privileges](/power-platform/admin/security-roles-privileges).

## Deploy Copilot for Sales

Looking for step-by-step instructions on how to deploy Copilot for Sales? Here are the Copilot for Sales deployment guides:

- [Copilot for Sales deployment guide for Dynamics 365 customers](deploy-viva-sales-d365.md)
- [Copilot for Sales deployment guide for Salesforce CRM customers](deploy-viva-sales-sf.md)

## How to use Copilot for Sales?

After you install Copilot for Sales for your users, they can start using it in Outlook and Teams. For information on how to use Copilot for Sales, see [Access the Copilot for Sales app](open-app.md).

### Related information

[Install Copilot for Sales in Outlook](install-viva-sales-as-an-integrated-app.md)  
[Install and pin Copilot for Sales in Teams](install-pin-viva-sales-teams.md)  
