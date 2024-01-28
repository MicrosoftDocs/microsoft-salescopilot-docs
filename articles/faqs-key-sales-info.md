---
title: FAQ for key sales info feature in Outlook
description: This FAQ provides information about the AI technology used in the key sales info feature in Microsoft Copilot for Sales, along with key considerations and details about how AI is used, how it was tested and evaluated, and any specific limitations.
ms.date: 02/01/2024
ms.custom: 
  - responsible-ai-faqs
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.reviewer: shjais
---

# FAQ for key sales info feature in Outlook

These frequently asked questions (FAQ) describe the AI impact of Microsoft Copilot for Sales's key sales info feature in Outlook.

## What is the key sales info feature?

The key sales info feature shows shows relevant CRM data based on the context of an email in the **Key sales info** card in the Copilot for Sales app in Microsoft Outlook. Users must have the Copilot for Sales premium license to see this card. The data is retrieved from the connected CRM and emails. User must open the Copilot for Sales side pane in Outlook to see the **Key sales info** card. Based on the email that the user has selected, the app finds relevant CRM key information related to email like contact, account, and opportunity.


## What the feature can do?

Create CRM highlights based on the email and the CRM relevant data such as contact, account, and opportunity.

## What is the feature's intended use?

The intended use of this feature is to show sales relevant information from the CRM such as contact, account and opportunity highlights to the user. 

## How was the key sales info feature evaluated? What metrics are used to measure performance? 

In the context of our Copilot for Sales product, the evaluation process involves a comprehensive approach to red teaming, performance metrics, and targeted mitigations. Red teaming is employed to rigorously assess the system's resilience and identify potential vulnerabilities in the handling of key sales information. Robust performance metrics are implemented to quantitatively measure the effectiveness and efficiency of the Copilot for Sales, ensuring it meets and exceeds the desired benchmarks. Mitigations are specifically tailored to address identified weaknesses, providing a proactive and strategic approach to enhance the overall security and functionality of the product in handling critical sales data. This meticulous evaluation framework aligns with our commitment to delivering a secure and high-performance solution for our clients.

## What are the limitations of this feature? How can users minimize the impact of system’s limitations when using the system? 

System may not find relevant CRM information to show, in that case, it will not show any data in the **Key sales info** card.

## What operational factors and settings allow for effective and responsible use of the system?

- **Data privacy and security**: Implement robust data privacy measures to protect customer information and ensure compliance with relevant regulations. Use secure communication channels and encryption methods to safeguard sensitive data.

- **User training and guidelines**: Provide comprehensive training to users on the system's features, capabilities, and limitations. Establish clear guidelines and best practices for responsible and ethical use, emphasizing the importance of accurate representation, respectful communication, and adherence to legal and ethical standards.

- **User permissions and access control**: Implement role-based access control to limit system functionalities and data access based on user roles and responsibilities. Ensure that users have appropriate permissions aligned with their job responsibilities and authorized access to customer data.

- **Monitoring and auditing**: Regularly monitor system usage, interactions, and outcomes to identify any potential issues or concerns. Conduct periodic audits to assess adherence to guidelines, data protection measures, and ethical practices.

- **Feedback and continuous improvement**: Encourage users to provide feedback on system performance, accuracy, and user experience. Actively seek user input to understand their needs and identify areas for improvement. Regularly update the system based on feedback and advancements in technology.

- **Transparency and explainability**: Foster transparency by clearly communicating to users how the system works, the underlying technologies used, and any limitations or potential biases. Ensure that users have a basic understanding of the system's capabilities and are informed about its AI-powered nature.

- **Accountability and error correction**: Establish mechanisms for addressing errors or inaccuracies that may occur in system-generated content. Encourage users to review and correct any inaccuracies, taking responsibility for the final output, and ensuring it aligns with their knowledge and expertise.

- **Set up the system**: Copilot AI features must be enabled by an administrator and fields for the opportunity record must be selected. Copilot for Sales must be connected to a CRM. 

## See also

- [Summarize an email thread using sales information with Copilot in Outlook](email-summary-premium.md)