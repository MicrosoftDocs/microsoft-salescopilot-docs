---
title: Privileges required to use Sales app
description: Learn what are the various privileges required to use Sales app
ms.date: 02/12/2025
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Privileges required to use Sales app

Sales applies your organization's existing CRM access controls and user permissions. Administrators must have correct permissions to customize their CRM systems, and users must have the correct permissions to view, update, and create records in their CRM systems from Sales app.

> [!NOTE]
> - If you've made changes in a user's permissions or security roles in your CRM, ask that user to sign out of Sales app in Outlook and then sign in again for these changes to be reflected appropriately. 
> - Changes in user permissions or security roles in CRM can take up to 15 minutes to reflect in Sales app for Teams.

## Permissions required for Salesforce administrators

Salesforce administrators who need to customize Sales app must have the following permissions.

|Requirement type  |You must have  |
|---------|---------|
| Permission | User profile needs to have **Modify All Data** or **Manage Data Integrations** permission.<br>**Note**: Permissions need to be on the user's profile and not in permission sets assigned to the user.|
| Privilege | **Read** and **Write** privileges on **Organization** table. |

## Privileges required for Dynamics 365 customers

### Dynamics 365 administrators

If you're using out-of-the-box **System Administrator** or **System Customizer** security roles, Sales app administration privileges are added automatically.

If you're using custom security roles, you must assign the **M365 Copilot Sales Administrator** security role and following privileges to Dynamics 365 administrators who need to customize Sales app.  

|Table| Logical name   | Privileges            | Access level       |
|-----|---------|-------------------------------|-------------|
| msdyn_vivausersetting | msdyn_vivausersetting       | Create, Read, Write, Delete, Append, Append to, Assign, Share | Organization |
| msdyn_vivaorgextensioncred | msdyn_vivaorgextensioncred  | Create, Read, Write, Delete, Append, Append to        | Organization |
| msdyn_vivaorgsetting  | msdyn_vivaorgsetting        | Create, Read, Write, Delete, Append, Append to        | Organization |
| msdyn_vivaentitysetting  | msdyn_vivaentitysetting     | Create, Read, Write, Delete, Append, Append to        | Organization |
|User | systemuser                  | Read                                                  | Organization |
| Recently Used | recentlyused                | Create, Read, Write, Delete                           | User        |
|Organization | organization                | Read, Write, Append to                                | Global      |

### Dynamics 365 sellers

If you're using the out-of-the-box **Salesperson** or **Sales Manager** security roles, Sales app privileges are added automatically and no further action is required.

If you're using custom security roles, you must assign the **M365 Copilot Sales User** security role and following privileges to Dynamics 365 sellers who need to use Sales app.

| Table       | Logical name       | Privileges        | Access level             |
|----------------|---------------------|---------------------|---------------------|
| Tagged Record       | msdyn_taggedrecord          | Create, Read, Write, Delete, Append, Append to        | User                           |
| External Record     | msdyn_externalrecord        | Create, Read, Write, Delete, Append, Append to        |  **Organization** access level for Read privilege.<br>**User** access level for Create, Write, Delete, Append, and Append to privileges. |
| External CRM        | msdyn_externalcrm           | Create, Read, Write, Delete, Append, Append to        | **Organization** access level for Read and Append to privileges.<br>**User** access level for Create, Write, Delete, and Append privileges. |
| CRM Connection      | msdyn_crmconnection         | Create, Read, Write, Delete, Append, Append to        | User                           |
| msdyn_vivausersetting| msdyn_vivausersetting       | Create, Read, Write, Delete, Append, Append to, Assign, Share | User                           |
| msdyn_vivaorgsetting| msdyn_vivaorgsetting        | Read                                                  | Organization                   |
| msdyn_vivaentitysetting| msdyn_vivaentitysetting   | Read                                                  | Organization                   |
| Note                | annotation                  | Create, Read, Write, Delete, Append, Append to, Assign, Share | User                           |
| User                | systemuser                  | Read                                                  | Organization                   |
| Recently Used       | recentlyused                | Create, Read, Write, Delete                           | User                           |


The **M365 Copilot Sales User** security role only compliments the custom security roles and does not replace them. If a custom security role assigned to sellers is missing any of the privileges included in Salesperson or Sales Manager security role, you might encounter errors specific to Dynamics 365 permission.

For information on how to assign security roles, see [Assign a security role to a user](/power-platform/admin/assign-security-roles).
  
To edit custom security roles to match with out-of-the-box Salesperson or Sales Manager role, see [Create or edit a security role to manage access](/power-platform/admin/create-edit-security-role). 

For information on security roles and privileges, see [Security roles and privileges](/power-platform/admin/security-roles-privileges).

## Deploy Sales app

Looking for step-by-step instructions on how to deploy Sales app? Here are the Sales app deployment guides:

- [Sales app deployment guide for Dynamics 365 customers](deploy-sales-app-d365.md)
- [Sales app deployment guide for Salesforce CRM customers](deploy-sales-app-sf.md)

### Related information

[Install Sales app](install-sales-app.md)