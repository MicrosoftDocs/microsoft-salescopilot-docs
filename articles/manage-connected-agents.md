---
title: Manage connected agentss in the Microsoft 365 admin center  
description: Learn how to manage connected agents for Sales in the Microsoft 365 admin center. Enhance responses by linking agents and leveraging shared insights.
ms.date: 12/08/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Manage connected agents in the Microsoft 365 admin center

The **Connected agents** tab enables you to link additional agents to Sales, extending its capabilities by leveraging information from other agents in your organization. When users interact with Sales, connected agents provide supplementary data and insights to enhance responses.

## What are connected agents?

Connected agents are other Copilot-enabled agents in your organization that can share data and insights with Sales. Once connected, Sales can query these agents and incorporate their responses to provide users with more comprehensive information.

### Key details

**Connection limit**
- You can connect up to 10 agents to Sales.

**Maker-added agents**
- Agents added by the maker cannot be removed by administrators.

**Access requirements**
- Ensure all connected agents are accessible to users who need them.
> [!NOTE]
> Only [declarative agents](/microsoft-365-copilot/extensibility/overview-declarative-agent) can be connected to Sales.

## Connect agents to Sales

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Agents** > **All agents**.
1. Select **Sales** and then go to the **Connected agents** tab.
1. Select **Connect agents**.
1. In the **Select agent to connect** pane:
    1. Find the agents using the search box.
    1. Select the agents you want to connect to Sales.
1. Select **Save**.

## Manage connected agents

1. In the [Microsoft 365 admin center](https://admin.microsoft.com/), go to **Agents** > **All agents**.
1. Select **Sales** and then go to the **Connected agents** tab.
1. To remove a connected agent, select the agent you want to remove and then select **Remove**.
1. To clear all custom connections and revert to the default state, select **Reset to default**.