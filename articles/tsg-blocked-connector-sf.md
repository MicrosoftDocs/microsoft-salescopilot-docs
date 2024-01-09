---
title: Unable to sign in to Salesforce due to blocked Salesforce connector
description: Troubleshoot and resolve error messages in Copilot for Sales when a user is unable to sign in to Salesforce due to blocked Salesforce connector.
ms.date: 01/09/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Unable to sign in to Salesforce due to blocked Salesforce connector

This article helps you troubleshoot and resolve error in Copilot for Sales when a user is unable to sign in to Salesforce due to blocked Salesforce connector.

## Who is affected?

| Requirement type |Description  |
|---------|---------|
|**Client app**     |  Copilot for Sales Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Salesforce        |
|**Users**     | All users  |

## Symptom

When a user tries to sign in to Salesforce from Copilot for Sales, the following error message is displayed: `Something went wrong` with the error code as `ConnectionApiPolicyViolation`.

:::image type="content" source="media/tsg-blocked-connector-sf.png" alt-text="Error about blocked Salesforce connector.":::

## Root cause and resolution

### Issue 1: The Salesforce connector is blocked

#### Root cause

Data Loss Prevention (DLP) is enabled on the default environment in the tenant thereby blocking the Salesforce connector.

#### Resolution

You must unblock the Salesforce connector in DLP policy to resolve this issue.

1. Sign in to the Power Platform admin center with admin credentials.
1. In the left navigation pane, select **Policies** > **Data policies**.
1. Select the data policy blocking the Salesforce connector, and then select **Edit Policy**.
1. On the **Prebuilt connectors** step, move the **Salesforce** connector to either **Business** or **Non-business**.
1. Go through rest of the steps, and then select **Update policy**.

## Is your issue still not resolved?

Visit the [Copilot for Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.