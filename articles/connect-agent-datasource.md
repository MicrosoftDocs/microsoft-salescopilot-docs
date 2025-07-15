---
title: Connect your agents to a data source
description: Learn how to connect agents to a data source for seamless data retrieval using server-to-server connections.
ms.date: 07/15/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ai-usage: ai-assisted
---

# Connect your agents to a data source

Agents such as Sales Agent need to connect to a data source in order to collect data. This is done by setting up a server-to-server connection to the data source. This connection allows the agent to run in the background and access and retrieve data from the data source without requiring user interaction.

If you're using Dynamics 365 Sales as your CRM, the agent connects directly to it, as it is deployed in the same environment. No extra setup steps are needed.

If you're using other CRM systems, such as Salesforce, the agent needs to connect to it in order to collect data. This is done by setting up a server-to-server connection.

## Set up server-to-server connection to Salesforce

When you set up a server-to-server connection to Salesforce, a connected app and an integration user are created in Salesforce. The connected app is used to authenticate the agent with Salesforce, while the integration user is used to access data in Salesforce. The integration user is created with a specific set of permissions that allow it to access the data needed by the agent.

### Enable server-to-server connection to Salesforce

1. In the Copilot for Sales admin settings, select **Connectors**.
1. Under **Agent connections**, select **Salesforce**.
1. Turn on the **Turn on access** toggle.
1. Select **Save**.

The connection might take a few minutes to get established. Once the connection is established, connected app and integration user details are displayed under **Connection details**.

If in the future you want to disable the server-to-server connection to Salesforce, you can do so by turning off the **Turn on access** toggle. This deletes the connected app and integration user from Salesforce. The agent will no longer be able to access data in Salesforce, and you need to set up the connection again if you want to use the agent with Salesforce.

> [!NOTE]
> You can connect a Salesforce environment to only one Microsoft tenant using the server-to-server connection. Connecting the same Salesforce environment to multiple Microsoft tenants is not supported and may lead to unexpected errors.

### How is the connection established?

When a connection is established, following components are created in Salesforce using the Salesforce APIs. The components can be viewed in Salesforce CRM on the **Setup** page.

- **Connected app**: Used to authenticate the agent with Salesforce. The name of the connected app is `Copilot for Sales connected app`. 
- **Integration user**: Used to access data in Salesforce. The name of the integration user is `Copilot for Sales integration user`.
- **Permission set**: Used to grant the integration user access to the data needed by the agent. The name of the permission set is `Copilot for Sales permission set`.

The minimum privilege principle is followed to ensure that the integration user has only the permissions needed to access the data required by the agent. If the agent is reconfigured to access more custom fields in the CRM, the connection must be recreated to access them correctly. An error message is shown in that case, and an option to recreate the connection is made available.

If an error occurs that prevents the connection from working properly, an error message is shown. Select **Reconnect** to recreate the connection. This action deletes the existing connection and creates a new one. 