---
title: Configure the conversation intelligence dashboard (preview)
description: Learn how to connect the conversation intelligence dashboard to your organization's data in Dataverse.
ms.date: 02/01/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:01/29/2024
---

# Configure the conversation intelligence dashboard (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

The Copilot for Sales conversation intelligence dashboard is a Power BI template app that provides insights into your sales conversations. The dashboard includes a prebuilt report and pages that help you understand the quality of your sales conversations, and how to improve them.

In this article, you learn how to configure the Copilot for Sales conversation intelligence dashboard using the [Power BI template app](/power-bi/connect-data/service-template-apps-overview).

## Download the Copilot for Sales dashboard app

You can download the Copilot for Sales - Conversation intelligence dashboard from [Microsoft AppSource](https://go.microsoft.com/fwlink/p/?linkid=2259835).

## Connect the dashboard to your organization's data

When you download Copilot for Sales - Conversation intelligence dashboard from Microsoft AppSource, it includes sample data. To connect the dashboard to your own data in Dataverse, follow these steps:

1. Open the downloaded Copilot for Sales dashboard in Power BI desktop.

1. Select **Connect your data**.  

    :::image type="content" source="media/connect-data.png" alt-text="Screenshot showing Connect your data link.":::

1. Enter the following information:
    1. **EnvironmentPath**: URL to your Dataverse environment. You must remove the `https://` prefix from the environment path URL you enter.
    1. **CRM type**: Type of CRM you're using.  

    :::image type="content" source="media/env-path-crm-type.png" alt-text="Screenshot of the fields to enter your Dataverse environment path (URL) and select the type of CRM you're using.":::

1. Select **Next**.

1. Select an authentication method and privacy level settings for your data source.

    :::image type="content" source="media/auth-privacy.png" alt-text="Screenshot of the fields to select authentication method and privacy level settings.":::

1. Select **Sign in and connect**.

1. After the dashboard is connected successfully to the organization's data, you can edit the report and publish it.  

> [!NOTE]
>
> Any edits you make to the dashboard are overridden if you install a newer version of the dashboard. Consider using the downloaded version as-is to avoid the need to manually edit the dashboard every time you install a new version. For more information, see, [How to edit and publish Power BI reports to a workspace](/power-bi/connect-data/service-template-apps-install-distribute).

## Update the dashboard to a newer version

To learn how to update to a newer version of the dashboard, see [Power BI template apps](/power-bi/connect-data/service-template-apps-overview).

## Configure access permissions in the dashboard

The Copilot for Sales dashboard uses Row-Level Security (RLS) to grant users with access, according to your organization hierarchy, which is imported from the system users table in Dataverse. Admins of Salesforce organizations can sync their organizations hierarchy from either Salesforce or Microsoft Entra ID.

For information about syncing your organization hierarchy see, [How to import hierarchy for Salesforce orgs](hierarchy-settings-sf.md).

The dashboard uses the organization hierarchy to determine who is each user's manager, and allows access to data based on the defined role of each user.

For information about RLS see, [Row-level security (RLS) with Power BI](/power-bi/enterprise/service-admin-rls).

The Copilot for Sales dashboard includes four predefined roles:

- **Seller (Agent)**: Can view data only of conversations to which they have access (can access the conversation summary page).

- **Sales Manager (Manager)**: Can view data of conversations to which they or their team have summary page access.

- **Business Unit Admin (BuAdmin)**: Can view data of conversations owned by anyone.

- **OrgAdmin**: Can view data of all conversations.

For information about configuring RLS in your managers' dashboard, see [Manage security on your model](/power-bi/enterprise/service-admin-rls#manage-security-on-your-model).
