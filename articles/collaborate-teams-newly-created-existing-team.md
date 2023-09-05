---
title: Collaborate in Teams using the newly created or existing team
description: Learn how to collaborate in Teams using the newly created or existing team.
ms.date: 09/05/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais 
---

# Collaborate in Teams using the newly created or existing team

After you've created a collaboration space to work on account or opportunity activities, you can access it by using any of the following options:

- In the Sales Copilot pane in Outlook, go to the **Collaborate in Teams** card in the **Highlights** tab, and then select the team.

- Open Microsoft Teams and then select the newly created team or the existing team.

- In the Sales app, open an account or opportunity, and then select **Collaborate** on the command bar at the top. Select the team linked to the account or opportunity. More information: [Access linked teams and channels](access-linked-teams-channels.md)

The team consists of two channels to:

- **Collaborate with colleagues**: This is the standard channel used to collaborate with people within your organization.

    If you've set up a new team using account team template, the General channel is linked to the CRM account.

    If you've set up a new team using deal room template, a new channel is created and linked to the CRM opportunity.

    If you've set up a collaboration space using an existing team, a new channel is created. By default, the name of the new channel is the account's or opportunity's name. The CRM account or CRM opportunity is linked to the newly created channel.

    This channel has the following pre-pinned apps:

    - **Files**: Three starter folders for document organization and one CRM folder (CRM related files) with the link to the CRM storage location associated with your account or opportunity if it has been configured by your administrator.

    - **CRM**: It displays the linked CRM account or opportunity. You can view and update CRM information from this tab.

        > [!NOTE]
        > If you are using Salesforce CRM, you must use Teams desktop app to see the CRM entity details. CRM tab does not load in Teams web client.

    - **CRM OneNote**: OneNote app can be used for sharing notes among all the team members in this channel. Customers who are in shared channel can't access this OneNote.

- **Collaborate with customers**: This is the shared channel used to collaborate with people outside your organization. The name of the shared channel is the account name prefixed with "Customer".

    To add customers to shared channels using their federated identity, ensure that your tenant administrator has enabled shared channels in Teams. More information: [Collaborate with external participants in a shared channel](/microsoft-365/solutions/collaborate-teams-direct-connect?view=o365-worldwide&preserve-view=true)

    Shared channel has the following pre-pinned apps:

    - **Files**: Three starter folders for document organization.

    - **OneNote**: This OneNote is different from the one created in the internal collaboration channel.   Sellers can use it for sharing notes with their customers. Team members who aren't part of the shared channel can't access this OneNote.

        > [!NOTE]
        >
        > - The CRM related files folder will not be created in the Files tab of the Shared channel to protect sensitive data.
        >
        > - CRM account will not be pinned in the Shared channel to protect sensitive organization data from being shared with customers.

:::image type="content" source="media/anatomy-account-team.png" alt-text="Screenshot showing anatomy of account team.":::

:::image type="content" source="media/anatomy-deal-room-team.png" alt-text="Screenshot showing anatomy of deal room team.":::

| Annotation | Description |
|------------|-------------|
| 1          | New account team created with two default channels.    |
| 2          | General channel to collaborate on account related activities with people within your organization. It's linked to the CRM account. |
| 3          | Shared account team channel to collaborate with people outside your organization.  |
| 4          | Pre-pinned apps  |
| 5          | New deal room channel created in the existing account team. It's linked to the CRM opportunity and is used to collaborate with people within your organization. |
| 6          | Shared deal room channel to collaborate with people outside your organization. |

## View AI-generated opportunity summary in deal room

When you open the team created using the deal room template in Teams for the first time, you will see the AI-generated [opportunity summary](view-opportunity-summary.md) in the standard channel as part of the welcome post. 

:::image type="content" source="media/oppty-summary-deal-room.png" alt-text="Screenshot showing AI-generated opportunity summary in deal room.":::

If you want to view the opportunity summary again at a later point in time, you can generate it using either of the following methods:
- Enter `@Sales Copilot show summary` in the message box and press **Enter**.
- Enter `@Sales Copilot help` in the message box, press **Enter**, and then select **Generate Opportunity Summary** from the list of options.

> [!NOTE]
> - The AI-generated opportunity summary is displayed only when your administrator has enabled copilot AI features. If your administrator has disabled copilot AI features, the opportunity summary is displayed in the form of field-value pairs. The fields in the summary are displayed as configured by your administrator.
> :::image type="content" source="media/oppty-summary-deal-room-non-ai.png" alt-text="Screenshot showing opportunity summary in deal room when copilot AI features are disabled.":::
> - If your administrator has blocked the Sales Copilot app in Teams, the opportunity summary is not generated.

### Data used to generate the opportunity summary  

A brief summary of the opportunity is generated using the following CRM fields from the opportunity record:
- Opportunity name
- Opportunity ID
- Created On
- Estimated close date
- Sales stage
- Budget amount
- Description
- Parent Account name
- Primary contact name

Content under the **Latest activity** section is generated from the summary of the last three notes added to the opportunity record.
