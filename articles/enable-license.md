---
title: Enable Copilot for Sales licenses
description: Learn how to enable Copilot for Sales licenses and deploy the app to users for enhanced integration with Microsoft 365 applications.
ms.date: 11/29/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:03/20/2024
---

# Enable Copilot for Sales licenses

The new Copilot for Sales license brings together the power of Microsoft 365 Copilot and sales-specific insights. The result is a "better together" experience across Microsoft 365 applications, such as Outlook, Word, and Teams.  
To enable Copilot for Sales licenses, you must complete these steps:

1. Assign a Copilot for Sales license to each user.
1. Deploy the Copilot for Sales app to users.
1. Validate that licenses are assigned to users, and that the correct app is installed in Outlook.

## Assign Copilot for Sales licenses to users

A Copilot for Sales license must be assigned to each user from the Microsoft 365 admin center. To assign licenses to users, you must be assigned an appropriate [Microsoft 365 admin role](/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide&preserve-view=true#commonly-used-microsoft-365-admin-center-roles) such as license admin or user admin.  
For detailed instructions, see [Assign licenses to users](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide&preserve-view=true).

## Deploy the Copilot for Sales app

For Outlook and Microsoft 365 integration capabilities, the new Copilot for Sales [enhanced Teams app](whats-new-copilot-sales.md#enhanced-teams-app-support) must be deployed to users through the Microsoft 365 admin center. For Teams integration capabilities, the app must be deployed through the Teams admin center. The enhanced Teams app includes the necessary integration for Microsoft 365 Copilot integration.

- For instructions for Dynamics 365, go to [Copilot for Sales deployment guide for Dynamics 365 customers](deploy-viva-sales-d365.md).

- For instructions for Salesforce, go to [Copilot for Sales deployment guide for Salesforce CRM customers](deploy-viva-sales-sf.md).

> [!NOTE]
>
> - If Copilot for Sales was deployed before February 2024, you must [deploy the enhanced Teams app](whats-new-copilot-sales.md#update-existing-sales-copilot-deployments) to enable the full capabilities of the product.
> - Ensure that an admin deploys the Copilot for Sales app by using the instructions in the preceding links. If system users install the app directly in Outlook, it won't have the required permissions for all supported scenarios.

## Validate the app installation

After the app is deployed, validate that the correct license is assigned to each user, and that the correct app is installed in Outlook.

### License validation

1. In Outlook, [open the Copilot for Sales pane](open-app.md#access-copilot-for-sales-in-outlook).
1. Select **Options** (**&hellip;**) in the upper-right corner, and then select **Diagnostics**.
1. Under **Client version**, ensure that "(Premium)" is appended to the value. This text indicates that the user has the correct license, and the app is installed correctly.

    :::image type="content" source="media/license-validate.svg" alt-text="Screenshot showing the Client version value for a Copilot for Sales premium license.":::

### App validation

To ensure that you deployed the enhanced Teams app, check for the new integration that it provides in Outlook. One of the new features is the Teams personal app. For this app, **Home** and **Settings** tabs are available in Outlook and other Microsoft 365 apps.

In Outlook, select **More Apps** on the left navigation bar, and then search for and select **Copilot for Sales**.  

:::image type="content" source="media/outlook-app-validate.svg" alt-text="Screenshot showing the Copilot for Sales app in Outlook.":::

When the personal app is opened, it should have **Home** and **Settings** tabs. If it does, the enhanced Teams app is correctly deployed and installed.

:::image type="content" source="media/outlook-personal-app.svg" alt-text="Screenshot showing a personal app that has Home and Settings tabs in Outlook.":::

## Integrated experiences with Microsoft 365 Copilot

This section describes the integrated experiences that Copilot for Sales provides across Microsoft 365 applications.

### Email summarization in Outlook

In Outlook, view email summaries that are enriched with sales information from CRM. For more information, go to [Summarize an email thread using sales information with Copilot in Outlook](email-summary-premium.md).

**Prerequisites**: To use the integrated experience, you must use Outlook on the web or the new Outlook for Windows. For a complete list of prerequisites, go to [Prerequisites](email-summary-premium.md#prerequisites).

:::image type="content" source="media/outlook-email-summary.svg" alt-text="Screenshot showing an email summary with sales insights in Outlook.":::

### Generative email replies in Outlook

In Outlook, generate email replies that use sales-specific insights. For more information, go to [Draft an email message using sales information with Copilot in Outlook](email-reply-premium.md).

**Prerequisites**: To use the integrated experience, you must use Outlook on the web or the new Outlook for Windows. For a complete list of prerequisites, go to [Prerequisites](email-reply-premium.md#prerequisites).

:::image type="content" source="media/outlook-email-reply.svg" alt-text="Screenshot showing the email reply option in Outlook.":::

### Teams meeting recap

View sales-related insights in Teams meeting recap. For more information, go to [View sales related insights in Microsoft Teams meeting recap](view-meeting-summary-recap.md).

**Prerequisites**: For a complete list of prerequisites, go to [Prerequisites](view-meeting-summary-recap.md#prerequisites).

:::image type="content" source="media/sales-insights-recap.png" alt-text="Screenshot showing sales insights in Teams meeting recap.":::

### Premeeting reports in Word

In Word, generate premeeting reports that use sales insights. For more information, go to [Generate premeeting report with Copilot in Microsoft Word (preview)](meeting-report-word.md).

**Prerequisites**: For a complete list of prerequisites, go to [Prerequisites](meeting-report-word.md#prerequisites).

:::image type="content" source="media/word-sales-meetings.png" alt-text="Screenshot showing Sales meetings select on the menu in Word.":::
