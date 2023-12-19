---
title: Turn on Copilot AI features
description: Learn how to turn on AI features in Microsoft Sales Copilot to help your sellers write better emails and stay on top of their deals.
ms.date: 12/19/2023
ms.topic: how-to
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.custom: bap-template
---

# Turn on Copilot AI features

Sales Copilot can use communication with sales contacts and information from your organization's customer relationship management (CRM) system to derive AI-powered insights that help your sellers write better emails, take better notes, and stay on top of their deals. As a tenant administrator or CRM administrator, you can set up Copilot AI features for your entire organization (tenant administrator) or specific environments (CRM administrator).

Copilot AI features might or might not be turned on by default, depending on where your tenant is located. For instance, if you're a new customer, your Dynamics 365 organization is located in North America or Europe, and your CRM resides in the same geography as Microsoft Entra ID, then Copilot AI features are turned on by default. Otherwise, you need to turn them on before your sellers can use them.

Copilot AI features in Sales Copilot are available only in some [supported languages](supported-languages.md).

## Turn on Copilot AI features for your organization

As a tenant administrator, you can control who can use AI capabilities in Sales Copilot for all environments in your organization. If you turn off Copilot AI features for your organization, CRM administrators can't turn them on in their environments.

1. [Open Sales Copilot administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).

1. Under **Tenant**, select **Copilot**.

1. Turn on **Copilot**.

1. Under **Apply to**, select one of the following options:

    - **The entire organization**: Turns on Copilot AI features for all sellers in all environments in your organization.
    - **Specific security groups**: Allows only selected security groups in your organization to use Copilot AI features. Search for and select the security groups you want to turn on Copilot AI features for.
    - **Exclude specific security groups**: Prevents selected security groups from using Copilot AI features. Search for and select the security groups you want to exclude.

    :::image type="content" source="media/viva-sales-tenant-admin.png" alt-text="Screenshot of Sales Copilot settings for a tenant.":::

1. Select **Save**.

## Turn on Copilot AI features in your environment

As a CRM administrator, you can control who can use AI capabilities in Sales Copilot in the environments you manage. If a tenant admin turned off Copilot AI features for your organization, you can't turn them on in your environments.

1. [Open Sales Copilot administrator settings](./administrator-settings-for-viva-sales.md#access-administrator-settings).

1. Under **Environment**, select **Copilot**.

1. Turn on **Copilot**.

1. To turn on preview features, select **Try our newest preview features before they're rolled out to everyone.**.

    Preview features allow sellers to benefit from new features before they're generally available. Preview features are turned off by default.

1. Select **Save**.

    :::image type="content" source="media/viva-sales-crm-admin.png" alt-text="Screenshot of Sales Copilot settings for an environment.":::

The following Copilot AI features are generally available:

- **Generate suggested email content**: Offers content that's generated using context from Outlook and your CRM, making it easy for sellers to compose or reply to emails quickly and confidently.

    *The AI-generated content is just a suggestion.* It's the seller's responsibility to review and edit the suggested content to make sure it's accurate and appropriate before sending the message.

    Make sure that the Sales Copilot for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the add-to-email functionality of the suggested content feature. [Learn how to update the Sales Copilot add-in](install-viva-sales-as-an-integrated-app.md#update-the-sales-copilot-add-in).

- **View and save email summary**: Allows sellers to view a summary of recent emails and save it to the CRM system.

- **View opportunity summary**: Allows sellers to view a summary of recent notes added to an opportunity.

- **Summarize sales meeting**: Offers an automated recap of a recently recorded Teams meeting with sales contacts that sellers can easily insert in an email.

## Data access and use

Sales Copilot uses the Azure OpenAI Service to generate AI-derived content. It doesn't process or store content for purposes of monitoring or preventing abusive or harmful uses of the service or for developing, testing, or improving capabilities that are designed to prevent abusive or harmful outputs. No Microsoft personnel have access to this content. Your users bear the sole risk and responsibility for any use of any Azure OpenAI-powered features. [Learn more about Azure OpenAI Service data, privacy, and security](/legal/cognitive-services/openai/data-privacy).

The Azure OpenAI Service is available in limited geographies. By using Copilot features powered by Azure OpenAI, you agree that data might be stored or processed outside of your geographic region, compliance boundary, or national cloud instance. Learn more about [data residency in Azure](https://azure.microsoft.com/explore/global-infrastructure/data-residency/#overview) and read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).

## FAQ

### Why do sellers see the Copy content button instead of the Add to email button in the suggested email content feature?

Their Sales Copilot for Outlook add-in is out of date. Make sure that the Sales Copilot for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the add-to-email functionality. [Learn how to update the Sales Copilot add-in](install-viva-sales-as-an-integrated-app.md#update-the-sales-copilot-add-in).

### See also

- [Use AI to kickstart email messages](use-copilot-kickstart-email-messages.md)
