---
title: FAQ for Sales Agent
description: This FAQ provides information about the AI technology used in the Sales Agent feature in Sales app, along with key considerations and details about how AI is used, how it was tested and evaluated, and any specific limitations.
ms.date: 11/20/2025
ms.custom: 
  - responsible-ai-faqs
ms.topic: faq
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.reviewer: shjais
---

# FAQ for Sales Agent

These frequently asked questions (FAQs) describe the AI impact of Sales Agent.

## What is Sales Agent?

Sales Agent uses a combination of internal and external data sources to research leads. It connects to your CRM (Microsoft Dynamics 365 Sales or Salesforce Sales Cloud) to find leads, and then uses the web and third-party data services to gather additional information about the lead's company, recent news, and other relevant insights.
Sales Agent also generates personalized outreach emails based on the insights gathered during the research process. These emails are tailored to the lead's interests and needs, increasing the chances of a positive response.

## What are the feature's capabilities?

Sales Agent utilizes large language models (LLM), natural language processing (NLP), and machine learning algorithms to analyze salesperson input, customer data, and historical email interactions. It leverages this information to generate tailored email drafts by suggesting content, subject lines, and personalized messaging, enhancing the salesperson's ability to engage with customers effectively.

## What is the feature's intended use? 

The intended use of this feature is to assist salespeople in qualifying leads and creating effective and personalized email drafts to communicate with customers. It aims to save time, improve writing skills, and enhance customer engagement by providing content suggestions and guidance based on historical data and customer insights.

## How was the Sales Agent feature evaluated? What metrics are used to measure performance?

The feature is evaluated through a combination of comparative analysis, human review, and customer engagement metrics. Performance is measured based on criteria such as accuracy, relevance, engagement, and customer satisfaction. Human reviewers assess the quality of system-generated content, ensuring it aligns with human-written drafts.
End-users provide ongoing feedback on each Copilot feature, along with iterative improvements contribute to optimizing the system's performance across all features.

## What are the limitations of this feature? How can users minimize the impact of the limitations when using the system?

The research may not always be completely accurate or up-to-date. The research may also be for the wrong company in the event there is ambiguity in the company name. To minimize the impact, users should review the research and check the citations to ensure the accuracy of the research.
The generated email drafts may not always capture the nuance or tone of the salesperson's individual style, potentially affecting personalization. To minimize the impact, users should review and customize the generated drafts to align with their preferred style, ensuring personalized communication.

## What operational factors and settings allow for effective and responsible use of the system?

- **Data privacy and security**: Implement robust data privacy measures to protect customer information and ensure compliance with relevant regulations. Use secure communication channels and encryption methods to safeguard sensitive data.  
- **User training and guidelines**: Provide comprehensive training to users on the system's features, capabilities, and limitations. Establish clear guidelines and best practices for responsible and ethical use, emphasizing the importance of accurate representation, respectful communication, and adherence to legal and ethical standards.  
- **User permissions and access control**: Implement role-based access control to limit system functionalities and data access based on user roles and responsibilities. Ensure that users have appropriate permissions aligned with their job responsibilities and authorized access to customer data.  
- **Monitoring and auditing**: Regularly monitor system usage, interactions, and outcomes to identify any potential issues or concerns. Conduct periodic audits to assess adherence to guidelines, data protection measures, and ethical practices.  
- **Feedback and continuous improvement**: Encourage users to provide feedback on system performance, accuracy, and user experience. Actively seek user input to understand their needs and identify areas for improvement. Regularly update the system based on feedback and advancements in technology.  
- **Transparency and explainability**: Foster transparency by clearly communicating to users how the system works, the underlying technologies used, and any limitations or potential biases. Ensure that users have a basic understanding of the system's capabilities and are informed about its AI-powered nature.  
- **Accountability and error correction**: Establish mechanisms for addressing errors or inaccuracies that may occur in system-generated content. Encourage users to review and correct any inaccuracies, taking responsibility for the final output, and ensuring it aligns with their knowledge and expertise.

## Which languages does Sales Agent support?

Sales Agent currently supports only English. 

## What data sources does Sales Agent use?

Sales Agent currently makes use of data from the following data sources:
- Dynamics 365 Sales or Salesforce CRM: Data from lead, account, contact, opportunity records and their related activity records are used when performing lead research.
- Publicly available web pages available internet.

## Related Information

- [Set up Sales Agent](set-up-sales-agent.md)
- [Use Sales Agent](use-sales-agent.md)
- [Send outreach email to leads](send-outreach-emails.md)
