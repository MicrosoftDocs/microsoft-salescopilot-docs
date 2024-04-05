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

Planner tasks that are created from the suggested tasks are accessible from the **Tasks** tab in the Teams channel. These tasks can also be accessed from the Microsoft Planner app.

`image`

Key benefits of the suggested tasks feature are:

- **Automated tasks suggestions**: As sales teams collaborate within collaboration spaces in Teams, the Copilot for Sales bot actively monitors the conversations in the channel for relevant discussions and action items. When it finds a potential task, it suggests the task to the channel members, who can then decide whether to add the task to their task list. Tasks are suggested once every 24 hours for new posts and replies in the channel.

    > [!NOTE]
    > - Automated task suggestions are available only in collaboration spaces that are created using the account team or deal room template in Microsoft Teams. They are not available in all Teams channels.
    > - Task suggestions are displayed only in the Standard channel and not in the private channel or shared channel.
    > - Task suggestions are shown only for the collaboration spaces that are created after March 2024 and not for the existing collaboration spaces.

- **Task creation and assignment**: Sales team members can select all or some of the suggested tasks and create them as Planner tasks. They can also assign the tasks to themselves or to other channel members. If required, they can update the task title, owner, and due date. Preview of the task is shown to the user creating the task.

- **Planner app integration**: The Planner app is pinned as **Tasks** tab in the channel. This helps the sales team not only to create tasks, but also to maintain a shared view of the tasks in the channel. Planner tasks are readily accessible from the dedicated account team or deal room channel through the **Tasks** tab in Teams. Planner tasks can also be viewed and managed from the Planner app in Teams.

> [!NOTE]
> Planner tasks created from collaboration spaces are not synced to the CRM system. They can only be accessed from the **Tasks** tab in the channel or from the Planner app in Teams.

## License requirements

- Copilot for Sales
- Microsoft Planner

## Supported languages

This feature is currently supported only in English.

## Prerequisites

Collaboration space must be created for [account team](set-up-team-account-team-template.md) or [deal room](set-up-team-deal-room-template.md) in Microsoft Teams.

## Create tasks from suggested tasks

1. Open an account team or deal room channel in Microsoft Teams. 

    If task suggestions are available, you'll see the **Suggested tasks** card for a post in the channel.

2. In the **Suggested tasks** card, review the suggested tasks. Task name, assignee, and due date are shown for each task.

3. If required, edit the task details inline. You can change the task name, assignee, and due date.

4. If you've more than one **Tasks** tab or multiple plans in your Planner app, select the plan where you want to create the task from the **Add to Plan** list.

4. Perform one of the following actions:
    - If there's only one task, select **Create task**. 
    - If there are multiple tasks, select the tasks you want to create, and then select **Create selected tasks**.

4. In the confirmation message, select **Go to tasks** to view the created tasks in the **Tasks** tab. Alternatively, you can view the tasks in the Planner app in Teams.

    If the channel doesn't have an existing **Tasks** tab, a new tab is pinned to the channel. Sales team members can make updates to the tasks directly from the **Tasks** tab without switching to the Planner app. Tasks updates are automatically reflected in the Planner app as well.
     

`image`

### See also

[Set up account team template in Microsoft Teams](set-up-team-account-team-template.md) <br>
[Set up deal room template in Microsoft Teams](set-up-team-deal-room-template.md)
