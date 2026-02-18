---
title: Sales app data movement across geographies
description: Learn why you need to opt in to allow Copilot data to move outside of your default geography and how Azure OpenAI protects your data in transit.
ms.date: 02/18/2026
ms.topic: concept-article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Sales app data movement across geographies

Although the Sales app is available in most of the geographic regions, it requires the Microsoft Azure OpenAI Service, which is available only in specific regions. If your CRM environment is located in a region where Azure OpenAI Service is not available, your data, including personal data or data used in prompts or returned in completions, might be transmitted outside of the geographic locations that you've selected for your primary data residency.

You need to opt in to allow your data to move outside of your region to an Azure OpenAI endpoint in a different region. You can opt in by [providing consent in admin settings](suggested-replies.md). If you don't provide consent, Copilot AI features won't be available to your sellers and meeting insights won't be generated.

## How data movement across regions works

When you use copilots and generative AI features, your inputs (prompts) and outputs (results) might move outside of your region to the location where the Azure OpenAI Service endpoint that supports these features is hosted.

Effective February 21, 2024, for new customers who connect the Sales app to their Dynamics 365 environment, the following table explains when and how data for copilots and generative AI features can move across regions.

> [!IMPORTANT]
> If you've connected the Sales app to your Salesforce environment, consent for data movement across regions is required regardless of the region where your CRM environment is hosted.

| Region where your CRM environment is hosted | Consent required for data movement across regions? | How to allow data to move across regions|
|-------------------|-------------------|-------------------|
| Australia</br>United Kingdom</br>United States | No | No action required. Data doesn't move across regions in this scenario.|
| Europe | Yes\* | No action required. Data doesn't move outside the [EU Data Boundary](https://www.microsoft.com/en-us/trust-center/privacy/european-data-boundary-eudb) in this scenario.<br><br>**Note**: By default, the [**Allow moving data outside boundaries**](suggested-replies.md) checkbox is selected. If you don't want to provide the data movement consent, you can clear the **Allow moving data outside boundaries** checkbox. In this case, Copilot AI features won't be available to your sellers and meeting insights won't be generated.|
| Asia</br>Brazil</br>Canada</br>France</br>Germany</br>India</br>Japan</br>Norway</br>South Africa</br>South Korea</br>United Arab Emirates | Yes | [Provide consent in admin settings](suggested-replies.md). <br><br> **Note**: If you don't provide the data movement consent, Copilot AI features won't be available to your sellers and meeting insights won't be generated.|

\* If your CRM environment is hosted in the EU Data Boundary, we use an Azure OpenAI endpoint in the same boundary.
