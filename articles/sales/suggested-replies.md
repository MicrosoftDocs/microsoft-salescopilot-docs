---
title: Set up email insights
description: Help sellers write better emails and stay on top of their deals with AI-driven insights.
ms.date: 05/18/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Set up email insights

Viva Sales can help sellers write better emails and stay on top of their deals with AI-driven insights that are based on their communication with sales contacts and information from their CRM system.

As an administrator, you can configure:

- **Suggested email content**: Makes it easy for sellers to compose and reply to emails quickly and confidently with the suggested content.

- **Summarizing sales meeting**: Allows sellers to generate suggested email content that contains an automated recap of a recently recorded Teams meeting with sales contacts.


## Configure suggested email content in Outlook

As an administrator, you can allow Viva Sales to generate suggested email content using context from Outlook, your CRM, and GPT technology. This makes it easy for your sellers to compose or reply to emails quickly and confidently. By default, the capability to generate suggested content is turned on.

> [!NOTE]
> - The AI-generated content is just a suggestion. It is your responsibility to review and edit the suggested content to make sure it’s accurate and appropriate before sending your email.
> - Suggested email content is available in [supported languages](supported-languages.md).
> -  Ensure that the Viva Sales for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the copy to email functionality of the suggested reply feature. For information on how to update the add-in, go to [Update the Viva Sales add-in](install-viva-sales-as-an-integrated-app.md#update-the-viva-sales-add-in).

**To enable suggested email content in Outlook**

1.  In Viva Sales admin settings, select **Email**.

2.  Turn on **Suggested email content**.

    :::image type="content" source="media/viva-sales-replies-admin.png" alt-text="Setting to generate suggested email content.":::

## Preview: Configure sales meeting summarization

> [!IMPORTANT]
> This feature is currently available only for public preview customers and is subject to change.

You can control whether sellers can generate suggested email content that contains an automated recap of a recent recorded Teams meeting with sales contacts.

1. In Viva Sales admin settings, select **Email**.

2. Under **Suggested email content**, select **Include the option to summarize sales meetings (preview)**.

    > [!NOTE]
    > The option to summarize sales meeting is available only when **Suggested email content** is turned on.

    :::image type="content" source="media/viva-sales-summary-admin.png" alt-text="Setting to allow sellers to summarize sales meetings.":::

## Data access and use

As part of providing AI suggestions (via Azure OpenAI), Viva Sales does not process and store content submitted to the Azure OpenAI Service for monitoring or preventing abusive or harmful uses of the service, nor developing, testing, or improving capabilities designed to prevent abuse use and/or harmful outputs. No Microsoft personnel have access to this content. Customer bears the sole risk and responsibility for any use of any AOAI-powered features, including use by Customer’s end users. For more information, see the [Azure OpenAI product documentation](/legal/cognitive-services/openai/data-privacy).

The Azure OpenAI Service is currently available in limited geographies. By using Copilot features powered by Azure OpenAI, you agree that data may be stored and/or processed outside of your geographic region, compliance boundary, or national cloud instance. Learn more about [Data Residency in Azure](https://azure.microsoft.com/explore/global-infrastructure/data-residency/#overview) and read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).

## FAQ

### Users don't see the **Copy to email** button and instead only the **Copy text** button in the suggested e-mail feature.

Ensure that the Viva Sales for Outlook add-in is updated to the latest version (10.0.0.11 or newer) to use the copy to email functionality. For information on how to update the add-in, go to [Update the Viva Sales add-in](install-viva-sales-as-an-integrated-app.md#update-the-viva-sales-add-in).

### See also

[Use AI to kickstart email replies](https://support.microsoft.com/topic/use-ai-to-kickstart-email-replies-148708be-e1f9-477c-baba-0b4dd4b7abef)
