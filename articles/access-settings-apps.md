---
title: Manage access to Sales agent and Dynamics 365 Sales plugins across Microsoft apps
description: Control access to Sales agent and Dynamics 365 Sales plugins across Microsoft 365 Copilot, Outlook, Teams, and Dynamics 365 using tenant-level access settings.
author: sbmjais
ms.author: shjais
ms.service: microsoft-365-copilot-sales
ms.date: 11/02/2026
ms.topic: how-to
ai-usage: ai-assisted
---

# Manage access to Sales agent and Dynamics 365 Sales plugins across Microsoft apps

As an administrator, you can use tenant-level access settings to control access to Sales agent and Dynamics 365 Sales plugins:

- **Sales agent**: Manage access separately in Microsoft 365 Copilot, the Sales pane in Outlook, Teams, and Dynamics 365.
- **Dynamics 365 Sales plugins**: Manage access to sales skills in Copilot Cowork, Copilot Code, and Microsoft Scout.

For each, you can turn access on or off and use Microsoft Entra security groups to control who has access. For Sales agent, you can also restrict users who received it through automatic installation.

These settings control access only. They don't install apps, assign licenses, connect to a CRM environment, or grant access to CRM data.

## Prerequisites

- Sales agent is installed or enabled in each application where your organization plans to use it.
- You must have one of the following Microsoft Entra roles:
  - Global Administrator
  - Exchange Administrator
  - Power Platform Administrator

## Configure Sales agent access in Microsoft 365 apps and Dynamics 365

1. Open Sales agent administrator settings.
2. Under **Tenant**, select **Access settings**.
3. Select **Allow access to Sales agent**.

    :::image type="content" source="media/access-settings-apps-entry.png" alt-text="Screenshot of the Sales agent access settings entry page":::

1. In the **Sales agent** pane, locate the application you want to configure:
   - **Microsoft 365 Copilot**: Allows access to the Sales agent in Microsoft 365 Copilot.
   - **Outlook sidecar**: Allows access to the Sales agent in the Sales pane in Outlook.
   - **Teams**: Allows access to the Sales agent in Microsoft Teams.
   - **Dynamics 365**: Allows access to the Sales agent in Microsoft 365 Copilot in Dynamics 365.
1. Use the toggle next to the application to turn Sales agent access on or off:
   - **On**: Allows users to access Sales agent in the selected application. You can configure access restrictions for each application individually.
   - **Off**: Prevents users from using Sales agent in the selected application.

6. If you turn on access, expand the application and, under **Who can use this feature?**, select one of the following options:
    - **No restrictions**: Everyone who meets the applicable licensing and configuration requirements can use Sales agent.
    - **Set access restrictions**: Use Microsoft Entra security groups to control access.

7. If you select **Set access restrictions**, configure one or both of the following lists:
    - **Allow access**: Search for and add security groups whose members can use Sales agent. If you leave this list empty, everyone can use the feature except members of groups under **Restrict access**.
    - **Restrict access**: Search for and add security groups whose members can't use Sales agent.

8. To prevent users who received Sales agent through automatic installation from accessing the feature, select **Restrict auto-installed users**.
9. Optional: Select **Download restricted auto-installed users (CSV)** to download the list of affected users.
10. Select **Save**.

    :::image type="content" source="media/access-settings-apps.png" alt-text="Screenshot of the Sales agent access settings page with application toggles":::

## Allow access to Dynamics 365 Sales plugins

Dynamics 365 Sales plugins give eligible users access to sales skills in Copilot Cowork, Copilot Code, and Microsoft Scout. These skills use Dynamics 365 Sales data together with Microsoft 365 context to help users analyze deals, assess competitive positioning, and prepare business cases and proposals. Use the following settings to control who can access the plugins. By default, all eligible users have access unless you configure access restrictions.

To learn more about the available skills and how users work with them, see [Use sales skills in Copilot Cowork](/dynamics365/sales/use-copilot-cowork-sales-skills).

1. Open Sales agent administrator settings.
1. Under **Tenant**, select **Access settings**.
1. Select **Allow access to Dynamics 365 Sales plugins**.
1. In the **Dynamics 365 Sales plugins** pane, use the toggle to turn access on or off.
1. Under **Who can use this feature?**, select one of the following options:
   - **No restrictions**: Everyone who meets the applicable licensing and configuration requirements can use Dynamics 365 Sales plugins.
   - **Set access restrictions**: Use Microsoft Entra security groups to control access.
1. If you select **Set access restrictions**, configure one or both of the following lists:
    - **Allow access**: Search for and add security groups whose members can use Dynamics 365 Sales plugins. If you leave this list empty, everyone can use the feature except members of groups under **Restrict access**.
    - **Restrict access**: Search for and add security groups whose members can't use Dynamics 365 Sales plugins.
1. Select **Save**.

    :::image type="content" source="media/access-settings-sales-plugins.png" alt-text="Screenshot of the Dynamics 365 Sales plugins access settings page with application toggles":::

## How access rules are evaluated

Sales agent evaluates each user's access in the following order and stops at the first matching rule:

1. If the application is turned off, access is blocked.
2. If **No restrictions** is selected, access is allowed.
3. If the user received Sales agent through automatic installation and **Restrict auto-installed users** is selected, access is blocked.
4. If the user belongs to a group under **Restrict access**, access is blocked.
5. If one or more groups are configured under **Allow access**, only members of those groups are allowed access.
6. Otherwise, access is allowed.

> [!NOTE]
> - **Restrict auto-installed users** blocks auto-installed users even if they belong to a group under **Allow access**.
> - **No restrictions** overrides **Restrict auto-installed users**. When you select **No restrictions**, auto-installed users aren't blocked by the checkbox.
> - Tenant access settings don't grant access to CRM data and don't override licensing, environment, or security requirements.

> [!TIP]
> When you pilot Sales agent with an allow list, clear **Restrict auto-installed users**, and then use groups under **Allow access** to limit the pilot to selected users.

## Default access after automatic installation

Automatic installation makes the Sales app available to users. By default, Sales agent is turned on for all apps, but the following access settings apply:

| App | Default access |
|------|----------------|
| Microsoft 365 Copilot | Auto-installed users are blocked. Other eligible users have access. |
| Sales pane in Outlook | Auto-installed users are blocked. Other eligible users have access. |
| Teams | Auto-installed users are blocked. Other eligible users have access. |
| Dynamics 365 | All eligible users have access. Microsoft 365 Copilot in Dynamics 365 must also be turned on. |
| Dynamics 365 Sales plugins | All eligible users have access. |

You can modify these defaults by:

- Turning an application off
- Changing security group restrictions
- Clearing **Restrict auto-installed users**

> [!IMPORTANT]
> Access to either Dynamics 365 Sales Enterprise or Dynamics 365 Sales Premium can make a user eligible for Sales agent and automatic distribution. Additional Microsoft 365 licenses or entitlements might be required to access Microsoft 365-grounded features and data.

## What users experience when access is disabled

Disabling access doesn't remove or uninstall Sales agent. The experience depends on the application.

| App | User experience |
|------|------|
| Microsoft 365 Copilot | Sales agent remains visible but displays an administrator-disabled message. |
| Sales pane in Outlook | The add-in remains visible but displays an administrator-disabled message. |
| Teams | Sales agent remains visible but displays an administrator-disabled message. |
| Dynamics 365 | Sales agent remains available in Microsoft Copilot in Dynamics 365, if enabled, but displays an administrator-disabled message. |

> [!NOTE]
> Visibility of Sales agent depends on whether the application is installed. Access settings affect behavior only and don't remove installed experiences.

## How tenant access settings work with other controls

Tenant access settings don't override other Sales agent requirements.

| Requirement | Description |
|-------------|-------------|
| Environment-level Sales chat access | Sales chat must be enabled and configured for the CRM environment. |
| App installation and enablement | Sales agent must be installed and enabled in the appropriate application. |
| Licensing | Users must have the required licenses and entitlements. |
| CRM connection and privileges | Users can access only the CRM environments, records, tables, and fields permitted by their assigned security roles and privileges. |

Turning on tenant access doesn't move or expose data automatically. Data is accessed only when an eligible user invokes an enabled capability and has the required Microsoft 365 and CRM permissions.

## Troubleshoot access issues

If a user can't access Sales agent:

1. Verify that the Sales app is installed in the affected application.
2. Verify that agents and Sales are allowed in the Microsoft 365 admin center.
3. Verify that the application is enabled under **Tenant** > **Access settings**.
4. Check whether the user:
   - Belongs to a restricted security group.
   - Is excluded from configured allowed groups.
   - Is identified as an auto-installed user while **Restrict auto-installed users** is selected.

5. Verify that Sales Chat is enabled and configured for the user's CRM environment.
6. Verify the user's:
   - Product licenses.
   - CRM connection.
   - Environment access.
   - CRM security privileges.

> [!NOTE]
> Access setting changes can take up to 15 minutes to take effect. Microsoft Entra security group membership changes can take up to one hour to appear in access evaluations.

### Check whether a user is auto-installed

Blocked users see the same disabled message regardless of which access rule blocks them. To determine whether **Restrict auto-installed users** blocks a specific user:

1. In Sales agent administrator settings, go to **Tenant** > **Access settings**, and then select **Allow access to Sales agent**.
2. In the **Sales agent** pane, locate the application you want to check, and expand its settings.
3. Select **Download restricted auto-installed users (CSV)**.
4. Stay on the page while the file is prepared. A CSV file downloads to your device and contains one column of Microsoft Entra object IDs for all auto-installed users.
5. Find the user's object ID in the Microsoft Entra admin center, and compare it with the IDs in the CSV file. If the ID appears in the file, the user is considered auto-installed.

To remove the auto-installation block for a user in an application, expand the application settings and clear **Restrict auto-installed users**. This checkbox applies per app, and clearing it removes the block for all auto-installed users of that app, not only the selected user. Other access rules still apply. To limit access, select **Set access restrictions**, and then configure security groups under **Allow access** and **Restrict access**.

### Administrator permissions error

If you see the message **"You need admin permissions to manage these settings"**, verify that you have one of the following roles:

- Global Administrator
- Exchange Administrator
- Power Platform Administrator

If necessary, contact an administrator with one of these roles.

## Related information

- [Install Sales agent in Outlook and Microsoft 365 Copilot](install-sales-as-an-integrated-app.md)
- [Install and pin Sales agent in Teams](install-pin-sales-teams.md)
- [Set up Sales agent in Microsoft 365 Copilot](set-up-sales-chat.md)
- [Use Sales agent in Microsoft 365 Copilot](use-sales-chat.md)
- [Privileges required to use Sales agent](privileges.md)