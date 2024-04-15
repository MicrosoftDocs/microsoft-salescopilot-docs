---
title: Copilot data movement across geographies
description: Learn why you need to opt in to allow Copilot data to move outside of your default geography and how Azure OpenAI protects your data in transit.
ms.date: 03/18/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Copilot data movement across geographies

Although Copilot is available in all geographic regions, it requires the Microsoft Azure OpenAI Service, which is available only in specific regions. If your CRM environment is located in a region where Azure OpenAI Service is not available, your data, including personal data or data used in prompts or returned in completions, might be transmitted outside of the geographic locations that you've selected for your primary data residency.

You need to opt in to allow your data to move outside of your region to an Azure OpenAI endpoint in a different region. You can opt in by [providing consent in admin settings](suggested-replies.md). If you don't provide consent, Copilot AI features won't be available to your sellers and meeting insights won't be generated.

## How data movement across regions works

When you use copilots and generative AI features, your inputs (prompts) and outputs (results) might move outside of your region to the location where the Azure OpenAI Service endpoint that supports these features is hosted. We might store prompt and output data for up to 30 days to [monitor for abuse](/azure/ai-services/openai/concepts/abuse-monitoring), but we don't look at it unless our automated systems flag it for review.

Effective February 21, 2024, for new customers, the following table describes when and how data can move across regions for copilots and generative AI features.

| Region where your CRM environment is hosted | Consent required for data movement across regions? | How to allow data to move across regions|
|-------------------|-------------------|-------------------|
| Australia</br>United Kingdom</br>United States | No | No action required. Data doesn't move across regions in this scenario.|
| Europe | Yes\* | No action required. Data doesn't move outside the [EU Data Boundary](https://www.microsoft.com/en-us/trust-center/privacy/european-data-boundary-eudb) in this scenario.<br><br>You can clear the [**Allow moving data outside boundaries**](suggested-replies.md) checkbox, if you want to. |
| Asia</br>Brazil</br>Canada</br>France</br>Germany</br>India</br>Japan</br>Norway</br>South Africa</br>South Korea</br>United Arab Emirates | Yes | [Provide consent in admin settings](suggested-replies.md). |

\* If your CRM environment is hosted in the EU Data Boundary, we use an Azure OpenAI endpoint in the same boundary.