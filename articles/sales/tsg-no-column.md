---
title: Salesforce CRM users unable to see data in Sales Copilot
description: Troubleshoot and resolve error messages in Sales Copilot related to field level security in Salesforce.
ms.date: 05/15/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Salesforce CRM users unable to see data in Sales Copilot

[!INCLUDE[vs-rebrand-note](../includes/vs-rebrand-note.md)]

This article helps you troubleshoot and resolve error messages in Sales Copilot related to field level security in Salesforce.

## Who is affected?

|  |  |
|---------|---------|
|**Client app**     |  Sales Copilot Outlook add-in        |
|**Platform**     | Web and desktop clients         |
|**OS**     | Windows and Mac         |
|**Deployment**     | User managed and admin managed       |
|**CRM**     | Salesforce        |
|**Users**     | Users who do not have permissions to view fields added in Sales Copilot forms   |


## Symptom

When using Sales Copilot in Outlook, users see error such as `To see this data in Sales Copilot, ask your Salesforce admin to delete the fields listed in the error details from Sales Copilot.`. This could happen when an administrator sets up a field to be displayed or editable in Sales Copilot, while the same field is not allowed to be edited or viewed as per the settings in Salesforce CRM.

:::image type="content" source="media/tsg-field-error.png" alt-text="Error to delete fields.":::

## Root cause and resolution

### Issue 1: Sales Copilot displays error to delete the fields after signing to Salesforce CRM

#### Root cause

Users don't have access to view all fields added in Sales Copilot forms.

#### Resolution

Change the admin settings from the Sales Copilot admin settings in Microsoft Teams to hide the fields or remove edit capabilities.

1. Sign in to Microsoft Teams with your administrator credentials.

2. In the navigation bar on the left, select **Sales Copilot**.

3. On the **Settings** tab, select Forms.

4. Select the entity for which you are seeing the error.

5. Under **Manage fields**, perform one of the following actions:

    - If the issue is related to editing of a field, turn off **Allow editing** for the corresponding field.

        :::image type="content" source="media/tsg-allow-edit.png" alt-text="Turn off editing for a few fields":::

    - If the issue is related to viewing the field, hover over the field, and select **Remove field** (![Delete icon.](media/delete-icon.png "Delete icon")).

6. Select **Publish** to save your changes.

## Is your issue still not resolved?

Visit the [Sales Copilot - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/viva-sales/bd-p/VivaSales) to engage with our experts.
