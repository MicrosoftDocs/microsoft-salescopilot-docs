---
title: Advanced collaboration with AI-powered Planner tasks
description: Efficient task management for sales teams with AI-powered Planner tasks in Copilot for Sales
ms.date: 05/01/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:03/14/2024
---

# Advanced collaboration with AI-powered Planner tasks (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note.md)]

Sales teams work together closely and use apps like Microsoft Planner to manage their tasks efficiently. Numerous critical next steps and action items emerge in their daily conversations. However, many of these tasks aren't captured and tracked, leading to missed opportunities and lost revenue.

The AI powered Planner tasks feature in Copilot for Sales helps sellers to stay on top of their action items by suggesting tasks that are related to their accounts and opportunities. This feature seamlessly integrates with the collaboration spaces in Teams and helps sellers to capture and track tasks that are discussed in their conversations. It automatically turns important discussions into Planner tasks, making it easy to track important activities. Sellers can also assign tasks to the right people and set deadlines.

Planner tasks that are created from the suggested tasks can be accessed from the Microsoft Planner app. Sales team members can also add the Planner app as a tab in the channel to view and manage the tasks from it.

Key benefits of the suggested tasks feature are:

- **Automated tasks suggestions**: As sales teams collaborate within collaboration spaces in Teams, the Copilot for Sales bot actively monitors the conversations in the channel for relevant discussions and action items. When it finds a potential task, it suggests the task to the channel members, who can then decide whether to add the task to their task list. Tasks are suggested once every 24 hours for each post and its replies in the channel.

    > [!NOTE]
    > - The channel must have at least 10 messages in the last 24 hours in at least one of the posts in the channel for the task suggestions to be generated. If there's no task suggestion, a message is displayed informing the user about the same.
    > - Automated task suggestions are available only in collaboration spaces that are created using the account team or deal room template in Microsoft Teams. They are not available in all Teams channels.
    > - Task suggestions are displayed only in the Standard channel and not in the private channel or shared channel.
    > - Task suggestions are shown only for the collaboration spaces that are created after May 01, 2024 and not for the existing collaboration spaces.

- **Task creation and assignment**: Sales team members can select all or some of the suggested tasks and create them as Planner tasks. They can also assign the tasks to themselves or to other channel members. If necessary, they can update the task title, owner, and due date. Preview of the task is shown to the user creating the task.

- **Planner app integration**: Sales team members can add the Planner app as a tab in the channel to view and manage the tasks from it. They can also view and manage the tasks from the Planner app.

> [!NOTE]
> - Planner tasks created from collaboration spaces are not synced to the CRM system. They can only be accessed from the Planner app in Teams.
> - The AI-generated content is just a suggestion. It is your responsibility to review and edit the AI-generated content to make sure it's accurate and appropriate.
> - Suggested tasks are shown only to the active participants who either replied or reacted to the messages in the channel.

## License requirements

- Copilot for Sales (standard or premium)
- Microsoft Teams

## Supported languages

This feature is currently supported only in English.

## Prerequisites

Collaboration space must be created for [account team](set-up-team-account-team-template.md) or [deal room](set-up-team-deal-room-template.md) in Microsoft Teams.

### See also

[Create Planner tasks from suggested tasks](create-planner-tasks.md)<br>
[Set up account team template in Microsoft Teams](set-up-team-account-team-template.md) <br>
[Set up deal room template in Microsoft Teams](set-up-team-deal-room-template.md)
