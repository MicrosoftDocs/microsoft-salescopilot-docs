---
title: Configure email insights settings in Copilot for Sales
description: Learn how to configure email insights settings in Copilot for Sales, including sharing settings and sensitivity labels.
ms.date: 08/07/2025
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

As an admin, you can configure settings for email insights in Copilot for Sales. Email insights are generated from sales emails sent and received with at least one CRM contact. These settings allow you to control whether email insights are shared with other sellers and which emails are included based on sensitivity labels.

## Configure email insights sharing settings

With this setting, you can control whether stored email insights contribute to the AI knowledge base and other sellers can see them. By default, this setting is turned off, meaning that email insights are not shared. If you turn on this setting, only team members with access to the associated CRM record to an email can see email insights for that email. You can also choose whether to share email insights of all users or only of specific security groups.

### Prerequisites

- [Email insights storage must be turned on](access-settings.md#configure-email-insights-storage-settings-preview)

### Turn on or off email insights sharing

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).
1. Under **Environment**, select **Email insights (preview)**.
1. Select **Share email insights**.
1. Turn on or off the **Turn on access** toggle.
1. If the toggle is turned on, you can choose to share email insights of all users or only of specific security groups. To do this, select one of the following options:
    - **No restrictions**: All users' email insights are shared.
    - **Set access restrictions**: Email insights are shared only of users in the selected security groups. You can add security groups in **Allow access** and **Restrict access** sections. Leaving the **Allow access** section empty will allow all users to access the feature, except those in the **Restrict access** section.
1. Select **Save** to apply the changes.

## Include email based on sensitivity labels

With this setting, you can control whether emails with specific sensitivity labels are included in email insights. Emails without a sensitivity label are always included in email insights.

To include emails based on sensitivity labels:

1. [Open Copilot for Sales administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).
1. Under **Environment**, select **Email insights (preview)**.
1. Select **Include emails based on sensitivity labels**.
1. Select **Edit** next to **Choose Sensitivity labels**.
1. Select the sensitivity labels you want to include in email insights.
1. Select **Save** to apply the changes.

## Related information

- [Configure email insights storage settings (preview)](access-settings.md#configure-email-insights-storage-settings-preview)