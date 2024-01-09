---
title: Connection lost due to an expired or invalid session or a bad OAuth token
description: Troubleshoot and resolve error messages in Copilot for Sales when a user is logged out due to an expired or invalid session or a bad OAuth token.
ms.date: 01/09/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
---

# Connection lost due to an expired or invalid session or a bad OAuth token

This article helps you troubleshoot and resolve error when a user is logged out of Copilot for Sales due to an expired or invalid session or a bad OAuth token.

## Who is affected?

| Requirement type |Description  |
|---------|---------|
|**Client app**     |  Copilot for Sales Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Salesforce        |
|**Users**     | Users performing any action that requires a connection to Salesforce.|

## Symptom

When a user tries to perform any action in Copilot for Sales, which requires a connection to Salesforce, the user is logged out of Copilot for Sales and the following error message is displayed: `Connection lost`.

:::image type="content" source="media/tsg-conn-lost.png" alt-text="Screenshot showing connection lost error.":::

## Root cause and resolution

### Issue 1: Bad OAuth token

#### Root cause

The Salesforce connection, created using the Salesforce connector, maintains the authentication tokens for the connected user. The same authentication tokens are used to communicate with Salesforce. The bad OAuth token error occurs when the Salesforce connection is unable to renew the authentication tokens. 

### Issue 2: Expired or invalid session

#### Root cause

The Salesforce session has reached its expiration time or the session has become invalid. This is based on the session configuration in Salesforce.

### Resolution

You must perform any one of the following steps to resolve the issue:

- Select **Sign in again** in the error message, and then sign in to Salesforce again.
- [Sign out from Copilot for Sales](sign-out-sales-copilot.md) and then sign in to Salesforce again.

## Is your issue still not resolved?

Visit the [Copilot for Sales - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.