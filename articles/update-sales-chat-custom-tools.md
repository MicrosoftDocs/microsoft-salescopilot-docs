---
title: Update Sales agent custom tools and knowledge in the Microsoft 365 admin center
description: Learn how to update the custom tools and knowledge in Sales agent to the latest source-agent version while preserving the existing audience.
ms.date: 08/27/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# Update Sales agent custom tools and knowledge in the Microsoft 365 admin center

The custom tools and knowledge you add to Sales agent are a point-in-time copy of the selected source-agent version. Publishing a newer version of the source agent doesn't automatically update the extension in Sales agent.

When a newer version is available, use **Update from store** in the Microsoft 365 admin center to replace the copied tools and knowledge with the latest source-agent version. The update preserves the users and security groups assigned to the extension. You don't need to remove the extension, select the source agent again, or re-create its audience.

## When an update is available

The **Update from store** action appears in the source-agent row when Sales agent has an active custom-tools extension and a newer source-agent version is available.

The update message varies depending on whether the extension tracks the version from which it was originally copied:

- If no source version is recorded, the update message doesn't display the current version. Instead, it displays **Update from the agent version in store**. The update replaces the existing extension with the latest version available in the store.

    :::image type="content" source="media/update-agent-no-version.png" alt-text="Screenshot of update message when no source version is recorded":::

- If a source version is recorded, the update message displays both the current version and the version available in the store. For example, **Upgrade from V 10.3 to V 10.4.9**. This information helps administrators understand which version is installed and which version will be applied.

    :::image type="content" source="media/update-agent-version.png" alt-text="Screenshot of update message when a source version is recorded":::

## Update custom tools and knowledge

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/).
1. Go to **Agents** > **All agents**.
1. Select **Sales**, and then open the **Custom tools & knowledge** tab.
1. In the source-agent row, select **More actions** (**⋮**).

    :::image type="content" source="media/update-agent-button.png" alt-text="Screenshot of the More actions button.":::

1. Select **Update from store**. 

    Wait for the update to finish. The source-agent row shows the update progress.

    Confirm that the success message appears and that the source agent has the expected availability.

> [!NOTE]
> The update doesn't open the **Assign Users** pane. The update automatically preserves the users and security groups currently assigned to the extension.

## What changes during an update

After a successful update:

- The custom tools and knowledge are copied again from the latest source-agent version.
- The latest copy replaces the previous one without removing the extension from Sales agent.
- The assigned users and security groups remain unchanged.
- The built-in tools and knowledge in Sales agent remain unchanged.
- Sales agent continues to use the same source agent for its custom extension.

> [!NOTE]
> Users might not see the updated tools and knowledge immediately. The changes can take up to 24 hours to become available.

## If Update from store isn't available

The **Update from store** action doesn't appear in any of the following conditions:

- The copied version is the same as the latest source-agent version.
- The version in the store is older than the copied version.
- The latest source-agent version can't be determined.
- Sales agent doesn't have an active custom tools & knowledge extension.
- The extension or source-agent information is still loading.

The **Update from store** action is displayed for all older extensions that don't have a recorded source version.

## If the update fails

A failed update doesn't remove or change the existing extension. Sales agent continues to use the previously copied tools and knowledge, and the assigned users and security groups remain unchanged. Try the update again after resolving the issue that caused the failure.

## Update limitations

- Updates always use the latest source-agent version. You can't select an earlier version or downgrade the extension.
- Source-agent changes aren't applied automatically. An administrator must start each update.
- You can still copy tools and knowledge from only one source agent, and their combined size can't exceed 150 KB.
- The **Update from store** action preserves the current audience and doesn't provide an option to edit it.
- Updating the extension doesn't grant users access to external systems used by the copied tools or knowledge. Users must have the required permissions in those systems.

## Related information

- [Extend Sales agent with custom tools and knowledge in the Microsoft 365 admin center](extend-sales-chat-custom-tools.md)
- [Manage connected agents in the Microsoft 365 admin center](manage-connected-agents.md)