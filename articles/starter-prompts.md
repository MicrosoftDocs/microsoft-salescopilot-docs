---
title: Configure starter prompts for Sales agent chat
description: Learn how to configure starter prompts for Sales agent chat to enhance your seller's interactions with sales data and CRM records. This article covers creating, managing, and optimizing prompts to drive better sales outcomes.
ms.date: 07/28/2026
ms.topic: how-to
ms.service: microsoft-365-copilot-sales
author: sbmjais
ms.author: shjais
---

# Configure starter prompts for Sales agent chat

As an administrator, you can configure starter prompts for Sales agent chat to help sellers quickly initiate common, high-value scenarios. Starter prompts appear in the Sales agent chat interface and give sellers a starting point for interacting with their sales data. By tailoring prompts to your organization's terminology, sales workflows, and priorities, you reduce friction and encourage consistent use of Sales agent.

You can configure separate sets of starter prompts for each context where sellers use Sales agent:

- **Dynamics 365**: Prompts shown in the Sales agent chat within Dynamics 365.
- **Microsoft 365 Copilot**: Prompts shown in Sales agent when sellers use Microsoft 365 Copilot.

In addition to any prompts you create, Microsoft provides a set of out-of-the-box starter prompts for each context. These Microsoft-provided prompts are read-only and can't be edited or deleted, but you can disable them if they're not relevant for your organization. The out-of-the-box prompts are marked with the **Default** tag.

## Prerequisites

- The Sales agent is installed in either [Outlook](install-sales-as-an-integrated-app.md) or [Teams](install-pin-sales-teams.md).
- You have access to environment-level settings in the [administrator settings for Sales agent](administrator-settings-sales-app.md).

## Access starter prompts settings

1. [Open the Sales agent administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Features**, select **Starter Prompts**.

The **Starter Prompts** page displays the out-of-the-box prompts and any custom prompts you create. You can also filter prompts by apps, type, or status to find specific prompts or view subsets of prompts.

:::image type="content" source="media/starter-prompts.png" alt-text="Screenshot of the Starter Prompts page":::

## Create a prompt

Create custom starter prompts that reflect your organization's workflows and guide sellers toward priority use cases. 

1. [Access the starter prompts settings](#access-starter-prompts-settings).
1. Select **Add prompt**.
1. In the **Add new prompt** pane, enter the following details:
    - **Title**: A short, descriptive label for the prompt that sellers see in the chat interface.
    - **Prompt text**: The full text of the prompt that is sent to Sales agent when the seller selects it.
1. Under the **Apps** section, select the contexts where you want the prompt to be available (for example, Dynamics 365 or Microsoft 365 Copilot).
1. Select **Add and translate prompt**.

    :::image type="content" source="media/starter-prompts-new.png" alt-text="Screenshot of the Add New Prompt pane":::

The new prompt appears in the list and is enabled by default. You can edit, disable, or delete the prompt at any time.

English is the default language for prompts. The system automatically translates prompts into other languages. You can review and edit translations for custom prompts, if needed, in the **Translations** tab. 

## Edit a prompt

You can edit custom prompts at any time. You can't edit out-of-the-box prompts.

1. [Access the starter prompts settings](#access-starter-prompts-settings).
1. Go to the prompt you want to edit and select the **Edit** icon.
1. Update the **Title**, **Prompt text**, or **Apps** as needed.
1. Select **Save changes**.
1. In the confirmation dialog, select **Continue to save** to confirm.

## Enable or disable a prompt

You can enable or disable both custom prompts and out-of-the-box prompts. Sellers don't see disabled prompts in the chat interface.

1. [Access the starter prompts settings](#access-starter-prompts-settings).
1. Turn on or off the toggle next to a prompt you want to enable or disable.

## Delete a prompt

You can delete custom prompts that you no longer need. You can't delete built-in prompts.

1. [Access the starter prompts settings](#access-starter-prompts-settings).
1. Go to the prompt you want to delete and select the **Delete** icon.
1. In the confirmation dialog, select **Delete** to confirm.

> [!CAUTION]
> Deleting a prompt is permanent. If you want to temporarily hide a prompt from sellers without losing it, consider [disabling it](#enable-or-disable-a-prompt) instead.

## Reorder prompts

You can reorder prompts to prioritize the most important or frequently used prompts for your sellers. Sellers see prompts in the chat interface in the order they appear in the list.

1. [Access the starter prompts settings](#access-starter-prompts-settings).
1. Go to the prompt you want to move and select the **Reorder** icon.
1. Drag the prompt to its new position in the list, and then release to drop it in place.

## Filter prompts

You can filter prompts to find specific prompts or view subsets of prompts based on criteria such as the context (Dynamics 365 or Microsoft 365 Copilot apps), type (custom or default), or status (enabled or disabled).

1. [Access the starter prompts settings](#access-starter-prompts-settings).
1. Select the criteria you want to filter by: 
    - **Apps**: Filter prompts based on the context where they're available (Calendar, Dynamics 365, Email, or Microsoft 365 Copilot).
    - **Type**: Filter prompts based on whether they're custom prompts you created or default out-of-the-box prompts provided by Microsoft.
    - **Status**: Filter prompts based on whether they're currently enabled or disabled.


## Related information

- [Set up Sales agent in Microsoft 365 Copilot](set-up-sales-chat.md)
- [Administrator settings for Sales agent](administrator-settings-sales-app.md)
- [Use Sales agent in Microsoft 365 Copilot](use-sales-chat.md)
