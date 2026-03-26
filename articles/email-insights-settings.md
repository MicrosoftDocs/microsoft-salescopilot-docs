---
title: Configure email insights settings in the Sales agent
description: Learn how to configure email insights settings in the Sales agent.
ms.date: 03/26/2026
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ai-usage: ai-assisted
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-title
  - ai-seo-date:08/07/2025
---

# Configure email insights settings (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Email insights is an AI-powered feature that analyzes sales emails involving CRM contacts and surfaces key details such as summaries, sentiment, objections, and next steps.

As an administrator, you can configure how email insights are stored and shared, and control which emails are included based on sensitivity labels. These settings help ensure that only authorized users or groups can access insights, while supporting your organization’s privacy and compliance requirements. 

## Configure email insights sharing settings

You can control whether stored email insights contribute to the AI knowledge base and other sellers can see them. By default, this setting is turned off, meaning that email insights are not shared. If you turn on this setting, only team members with access to the associated CRM record to an email can see email insights for that email. You can also choose whether to share email insights of all users or only of specific security groups.

### Prerequisites

- [Email insights storage must be turned on](access-settings.md#email-insights-preview)

### Turn on email insights sharing

1. [Open the Sales agent administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Environment**, select **Email insights (preview)**.
1. Select **Share email insights**.
1. In the **Share email insights** pane, turn on the toggle.
1. Under **Who can access this feature?**, choose to share email insights of all users or only of specific security groups. To do this, select one of the following options:

    - **No restrictions**: All users' email insights are shared.
    - **Set access restrictions**: Use security groups to decide which users' email insights are shared. You must add security groups in either of the sections to save the changes.
        - **Allow access**: Search and add security groups that can access the feature.
        - **Restrict access**: Search and add security groups that cannot access the feature.

1. Select **Save**.

    :::image type="content" source="media/email-insights-share.png" alt-text="Screenshot showing email insights sharing settings.":::

## Include email based on sensitivity labels

You can control whether emails with specific sensitivity labels are included in email insights. Emails without a sensitivity label are always included in email insights.

To include emails based on sensitivity labels:

1. [Open the Sales agent administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Environment**, select **Email insights (preview)**.
1. Select **Include emails based on sensitivity labels**.
1. Select **Edit** next to **Choose Sensitivity labels**.
1. Select the sensitivity labels you want to include in email insights.
1. Select **Save**.

    :::image type="content" source="media/email-insights-labels.png" alt-text="Screenshot showing email insights sensitivity label settings.":::

## Automatically summarize email in the Key email info card

You can control whether emails are automatically summarized in the [**Key email info**](view-save-email-summary-crm.md) card. By default, this setting is turned on. If you turn it off, sellers must manually summarize emails in the **Key email info** card by selecting **Summarize email**.

To configure this setting:

1. [Open the Sales agent administrator settings](./administrator-settings-sales-app.md#access-administrator-settings).
1. Under **Features**, select **Email insights (preview)**.
1. Turn on or off the **Auto-summarize emails** toggle to enable or disable automatic email summarization.

    :::image type="content" source="media/email-insights-auto-summary.png" alt-text="Screenshot showing email insights auto-summary settings.":::

## Related information

- [View and save email summaries to your CRM](view-save-email-summary-crm.md)
- [Configure email insights storage settings (preview)](access-settings.md#email-insights-preview)