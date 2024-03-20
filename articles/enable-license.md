---
title: Enable Copilot for Sales licenses
description: 
ms.date: 03/22/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Enable Copilot for Sales licenses

The new Copilot for Sales license brings together the power of Copilot for Microsoft 365 and the sales specific insights in a 'better together' experience across Microsoft 365 applications such as Outlook, Word, and Teams. 

To enable Copilot for Sales licenses, you must:

1. Assign a Copilot for Sales license to each user 
2. Deploy the Copilot for Sales app to users
3. Validate that end users have licenses assigned and the correct app is installed in Outlook

## Assign Copilot for Sales licenses to users

Each user must have a Copilot for Sales license assigned to them from within the Microsoft 365 admin center. You must be a global admin, license admin, or user admin to assign licenses to users.

For detailed instructions, see [Assign licenses to users](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide).

## Deploy the Copilot for Sales app

The Copilot for Sales [enhanced Teams app](whats-new-copilot-sales.md#enhanced-teams-app-support) must be deployed to users through the Microsoft 365 admin center for Outlook and Microsoft 365 integration capabilities, and through the Teams admin center for Teams integration capabilities. The new enhanced Teams app includes the needed integration for Microsoft 365 Copilot integration. 

For Dynamics 365, see [Copilot for Sales deployment guide for Dynamics 365 customers](deploy-viva-sales-d365.md).

For Salesforce, see [Copilot for Sales deployment guide for Salesforce CRM customers](deploy-viva-sales-sf.md).

> [!NOTE]
> - If Copilot for Sales was deployed before February 2024, you must [deploy the enhanced Teams app](whats-new-copilot-sales.md#update-existing-sales-copilot-deployments) to enable the full capabilities of the product.
> - Ensure that the Copilot for Sales app is admin-deployed with the instructions provided in the above links. If end users install the app directly in Outlook, the app will not have the required permissions for all supported scenarios.

## Validate the app installation

After the app is deployed, validate that a user has the correct license assigned to them.

### License validation

1. In Outlook, [open the Copilot for Sales pane](open-app.md#access-copilot-for-sales-in-outlook).
2. Select **Options** (**...**) in the upper-right corner, and then select **Diagnostics**.
3. Ensure that **Client version** has `(Premium)` appended to it. This indicates that the user has the correct license and the app is installed correctly.

    :::image type="content" source="media/license-validate.svg" alt-text="Screenshot showing Copilot for Sales premium license.":::

### App validation

To ensure that you have deployed the enhanced Teams app, check for the new integration it provides within Outlook. One of the new features is the Teams personal app that has **Home** and **Settings** tabs available in Outlook and other Microsoft 365 apps.

In Outlook, select **More Apps** on the left navigation pane, and then search and select **Copilot for Sales**. 

:::image type="content" source="media/outlook-app-validate.svg" alt-text="Screenshot showing Copilot for Sales app in Outlook.":::

The personal app should open with the **Home** and **Settings** tabs. This confirms that the enhanced Teams app is deployed and installed correctly.

:::image type="content" source="media/outlook-personal-app.svg" alt-text="Screenshot showing personal app in Outlook.":::

## Integrated experiences with Copilot for Microsoft 365

Following are the integrated experiences that Copilot for Sales provides across Microsoft 365 applications:

## Email summarization in Outlook

View email summary enriched with sales information from CRM in Outlook. For more information, see [Summarize an email thread using sales information in Outlook](email-summary-premium.md).

:::image type="content" source="media/outlook-email-summary.svg" alt-text="Screenshot showing email summary with sales insights in Outlook.":::

## Generative email replies in Outlook

Generate email replies with sales specific insights in Outlook. For more information, see [Generate email replies with sales information in Outlook](email-replies-premium.md).

:::image type="content" source="media/outlook-email-reply.svg" alt-text="Screenshot showing email reply option in Outlook.":::

## Teams meeting recap

View sales related insights in Microsoft Teams meeting recap. For more information, see [View sales related insights in Microsoft Teams meeting recap](view-meeting-summary-recap.md).

:::image type="content" source="media/sales-insights-recap.png" alt-text="Screenshot showing sales insights in Teams meeting recap.":::

## Premeeting report in Microsoft Word

Generate premeeting reports with sales insights in Microsoft Word. For more information, see [Generate premeeting reports with sales insights in Microsoft Word](meeting-report-word.md).

:::image type="content" source="media/word-sales-meetings.png" alt-text="Screenshot of a selected Sales meeting from the menu.":::