---
title: Set up Copilot AI features
description: Help sellers write better emails and stay on top of their deals with AI-driven insights.
ms.date: 10/30/2023
ms.topic: article
ms.service: microsoft-sales-copilot
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
---

# Set up Copilot AI features

Sales Copilot can help sellers write better emails, take better notes, and stay on top of their deals with AI-driven insights that are based on their communication with sales contacts and information from their CRM system. 

As a tenant administrator or CRM administrator, you can set up Copilot AI features for your organization and environment, respectively.

## Tenant administrator settings

As a tenant administrator, you can control who can use AI capabilities in Sales Copilot for all environments in your organization.

### Setup Copilot AI features

Enable Copilot AI features for all environments in your organization so your sellers can benefit from the available AI capabilities in Sales Copilot.

1.  In Sales Copilot admin settings, select **Copilot** under **Tenant**.
2.  Turn on **Copilot**.
3. Under **Apply to**, select one of the following options:
    - **The entire organization**: Enables Copilot AI features for all environments in your organization. All sellers in your organization can use Copilot AI features, unless turned off by a CRM administrator.
    - **Specific security groups**: Allows only selected security groups in your organization to use Copilot AI features. To select groups, select this option, and then search and select the groups you want to enable Copilot AI features for.
4. To exclude specific groups from using Copilot AI features, select **Exclude specific security groups**, and then search and select the groups you want to exclude.
    
    :::image type="content" source="media/viva-sales-tenant-admin.png" alt-text="Setting to turn on Copilot preview features.":::

5. Select **Save**.

> [!NOTE]
> If you've disabled Copilot AI features for your organization, CRM administrators can't enable Copilot AI features for their environments.

## CRM administrator settings

As a CRM administrator, you can configure environment-specific settings for Sales Copilot from a central location and control Sales Copilot experience across Outlook and Teams. You can configure:

- **Copilot AI features**: Enable Copilot AI features so your sellers can benefit from the available AI capabilities in Sales Copilot.

    Following are the generally available Copilot AI features:
    
    - **Generate suggested email content**: Allows sellers to generate suggested email content using context from Outlook, your CRM, and AI. This makes it easy for your sellers to compose or reply to emails quickly and confidently.
    - **View and save email summary**: Allows sellers to view a summary of the recent emails and save it to the CRM system.
    - **View opportunity summary**: Allows sellers to view a summary of the recent notes added to an opportunity.

- **Copilot preview features**: Allow sellers to benefit from the preview features before they are generally available. By default, preview features are turned off.

    Following are the preview features:
    
    - **Summarize sales meeting**: Allows sellers to generate suggested email content that contains an automated recap of a recently recorded Teams meeting with sales contacts.

> [!NOTE]
> - Copilot features are enabled by default for new customers with Dynamics 365 organizations in North America and Europe, only if the CRM resides in the same geography as Microsoft Entra ID.
> - The AI-generated content is just a suggestion. It is your responsibility to review and edit the suggested content to make sure it’s accurate and appropriate before sending your email.
> - Generally available Copilot features in Sales Copilot are available in [supported languages](supported-languages.md).
> -  Ensure that the Sales Copilot for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the add-to-email functionality of the suggested content feature. For information on how to update the add-in, go to [Update the Sales Copilot add-in](install-viva-sales-as-an-integrated-app.md#update-the-sales-copilot-add-in).

### Set up Copilot AI features

1.  In Sales Copilot admin settings, select **Copilot**.

2.  Turn on **Copilot**.

    > [!NOTE]
    > If copilot capabilities are turned off for your organization by a tenant administrator, you can't turn on copilot capabilities for your environment.

3. To turn on preview features, select **Try our newest preview features before they're rolled out to everyone.**.

    :::image type="content" source="media/viva-sales-crm-admin.png" alt-text="Setting to turn on Copilot preview features.":::

## Data access and use

As part of providing AI suggestions (via Azure OpenAI), Sales Copilot does not process and store content submitted to the Azure OpenAI Service for monitoring or preventing abusive or harmful uses of the service, nor developing, testing, or improving capabilities designed to prevent abuse use and/or harmful outputs. No Microsoft personnel have access to this content. Customer bears the sole risk and responsibility for any use of any AOAI-powered features, including use by Customer’s end users. For more information, see the [Azure OpenAI product documentation](/legal/cognitive-services/openai/data-privacy).

The Azure OpenAI Service is currently available in limited geographies. By using Copilot features powered by Azure OpenAI, you agree that data may be stored and/or processed outside of your geographic region, compliance boundary, or national cloud instance. Learn more about [Data Residency in Azure](https://azure.microsoft.com/explore/global-infrastructure/data-residency/#overview) and read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).

## FAQ

### Why do sellers see the Copy text button instead of the Copy to email button in the suggested email content feature?

Ensure that the Sales Copilot for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the copy to email functionality. For information on how to update the add-in, go to [Update the Sales Copilot add-in](install-viva-sales-as-an-integrated-app.md#update-the-sales-copilot-add-in).

### See also

[Use AI to kickstart email message](use-copilot-kickstart-email-messages.md)
