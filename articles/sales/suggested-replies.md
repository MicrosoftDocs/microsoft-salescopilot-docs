---
title: Set up Copilot in Viva Sales
description: Help sellers write better emails and stay on top of their deals with AI-driven insights.
ms.date: 06/19/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Set up Copilot in Viva Sales

Viva Sales can help sellers write better emails, take better notes, and stay on top of their deals with AI-driven insights that are based on their communication with sales contacts and information from their CRM system.

As an administrator, you can configure:

- **Copilot in Viva Sales**: Allows sellers to use Copilot features that are generally available.

- **Copilot preview features**: Allows sellers to try out new features that are in preview. 


## Copilot in Viva Sales

Enable Copilot features so your sellers can benefit from the available Copilot capabilities in Viva Sales.

Following are the generally available Copilot features:

- **Generate suggested email content**: Allows sellers to generate suggested email content using context from Outlook, your CRM, and AI. This makes it easy for your sellers to compose or reply to emails quickly and confidently.
- **View and save email summary**: Allows sellers to view a summary of the recent emails and save it to the CRM system.

> [!NOTE]
> - Copilot features are enabled by default for new customers with Dynamics 365 Sales in North America (NAM).
> - The AI-generated content is just a suggestion. It is your responsibility to review and edit the suggested content to make sure it’s accurate and appropriate before sending your email.
> - Generally available Copilot features in Viva Sales are available in [supported languages](supported-languages.md).
> -  Ensure that the Viva Sales for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the copy-to-email functionality of the suggested content feature. For information on how to update the add-in, go to [Update the Viva Sales add-in](install-viva-sales-as-an-integrated-app.md#update-the-viva-sales-add-in).

### Turn on Copilot features in Viva Sales

1.  In Viva Sales admin settings, select **Copilot**.

2.  Turn on **Copilot in Viva Sales**.

    :::image type="content" source="media/viva-sales-replies-admin.png" alt-text="Setting to turon on Copilot features.":::


## Copilot preview features

Allow sellers to benefit from the latest new features before they are generally available. By default, preview features are turned off. You can turn them on in Viva Sales admin settings.

Following are the preview features:
    
- **Summarize sales meeting**: Allows sellers to generate suggested email content that contains an automated recap of a recently recorded Teams meeting with sales contacts.

- **View opportunity summary**: Allows sellers to view a summary of the recent notes added to an opportunity.


### Turn on Copilot preview features in Viva Sales

1. In Viva Sales admin settings, select **Copilot**.

2. Under **Copilot in Viva Sales**, select **Try our newest preview features before they’re rolled out to everyone.**.

    :::image type="content" source="media/viva-sales-summary-admin.png" alt-text="Setting to turn on Copilot preview features.":::

## Data access and use

As part of providing AI suggestions (via Azure OpenAI), Viva Sales does not process and store content submitted to the Azure OpenAI Service for monitoring or preventing abusive or harmful uses of the service, nor developing, testing, or improving capabilities designed to prevent abuse use and/or harmful outputs. No Microsoft personnel have access to this content. Customer bears the sole risk and responsibility for any use of any AOAI-powered features, including use by Customer’s end users. For more information, see the [Azure OpenAI product documentation](/legal/cognitive-services/openai/data-privacy).

The Azure OpenAI Service is currently available in limited geographies. By using Copilot features powered by Azure OpenAI, you agree that data may be stored and/or processed outside of your geographic region, compliance boundary, or national cloud instance. Learn more about [Data Residency in Azure](https://azure.microsoft.com/explore/global-infrastructure/data-residency/#overview) and read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).

## FAQ

### Why do sellers see the Copy text button instead of the Copy to email button in the suggested email content feature?

Ensure that the Viva Sales for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the copy to email functionality. For information on how to update the add-in, go to [Update the Viva Sales add-in](install-viva-sales-as-an-integrated-app.md#update-the-viva-sales-add-in).

### See also

[Use AI to kickstart email message](https://support.microsoft.com/topic/use-ai-to-kickstart-email-replies-148708be-e1f9-477c-baba-0b4dd4b7abef)
