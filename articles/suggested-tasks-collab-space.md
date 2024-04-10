---
title: Advanced collaboration with AI powered Planner tasks
description: Efficient task management for sales teams with AI powered Planner tasks in Copilot for Sales
ms.date: 04/15/2024
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:03/14/2024
---

# Advanced collaboration with AI powered Planner tasks

Sales teams work together closely and use apps like Microsoft Planner to manage their tasks efficiently. Numerous critical next steps and action items emerge in their daily conversations. However, many of these tasks are not captured and tracked, leading to missed opportunities and lost revenue.

The AI powered Planner tasks feature in Copilot for Sales helps sellers to stay on top of their action items by suggesting tasks that are related to their accounts and opportunities. This feature seamlessly integrates with the collaboration spaces in Teams and helps sellers to capture and track tasks that are discussed in their conversations. It automatically turns important discussions into Planner tasks, making it easy to track important activities. Sellers can also assign tasks to the right people and set deadlines.

`image`

Key benefits of the suggested tasks feature are:

- **Automated tasks suggestions**: As sales teams collaborate within collaboration spaces in Teams, the Copilot for Sales bot actively monitors the conversations in the channel for relevant discussions and action items. When it finds a potential task, it suggests the task to the channel members, who can then decide whether to add the task to their task list. Tasks are suggested once every 24 hours for new posts and replies in the channel.

    > [!NOTE]
    > - Automated task suggestions are available only in collaboration spaces that are created using the account team or deal room template in Microsoft Teams. They are not available in all Teams channels.
    > - Task suggestions are displayed only in the Standard channel and not in the private channel or shared channel.
    > - Task suggestions are shown only for the collaboration spaces that are created after March 2024 and not for the existing collaboration spaces.

- **Task creation and assignment**: Sales team members can select all or some of the suggested tasks and create them as Planner tasks. They can also assign the tasks to themselves or to other channel members. If required, they can update the task title, owner, and due date. Preview of the task is shown to the user creating the task.

- **Planner app integration**: Sales team members can add the Planner app as a tab in the channel to view and manage the tasks from it. They can also view and manage the tasks from the Planner app in Teams.

> [!NOTE]
> - Planner tasks created from collaboration spaces are not synced to the CRM system. They can only be accessed from the Planner app in Teams.
> - The AI-generated content is just a suggestion. It is your responsibility to review and edit the AI-generated content to make sure it's accurate and appropriate.

## License requirements

- Copilot for Sales
- Microsoft Planner

## Supported languages

This feature is currently supported only in English.

## Prerequisites

Collaboration space must be created for [account team](set-up-team-account-team-template.md) or [deal room](set-up-team-deal-room-template.md) in Microsoft Teams.

## Create Planner tasks from suggested tasks

1. Open an account team or deal room channel in Microsoft Teams. 

    If task suggestions are available, you'll see the **Suggested Planner tasks** card for a post in the channel.

2. In the **Suggested Planner tasks** card, review the suggested tasks. Task name, assignee, and due date are shown for each task.

3. If required, edit the task details inline. You can change the task name, assignee, and due date.

4. If you've multiple plans in your Planner app, select the plan where you want to create the task from the **Add to Plan** list.

4. Perform one of the following actions:
    - If there's only one task, select **Create task**. 
    - If there are multiple tasks, select the tasks you want to create, and then select **Create selected tasks**.

4. In the confirmation message, select **Go to Planner** to view the created tasks in the Planner app. Alternatively, you also add the Planner app as a tab in the channel. You must use the plan name from the confirmation message to add an existing plan. For information about adding an app in a tab, see [Use an app in a tab in a channel or chat in Microsoft Teams](https://support.microsoft.com/office/use-an-app-in-a-tab-in-a-channel-or-chat-in-microsoft-teams-83d0514f-2134-4db5-80f2-e9b43e111d57).

    Sales team members can make updates to the tasks directly from the Planner app added in a tab without switching to the Planner app. Tasks updates are automatically reflected in the Planner app as well.
     

`image`

### See also

[Set up account team template in Microsoft Teams](set-up-team-account-team-template.md) <br>
[Set up deal room template in Microsoft Teams](set-up-team-deal-room-template.md)
