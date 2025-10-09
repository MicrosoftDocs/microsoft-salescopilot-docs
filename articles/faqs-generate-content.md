---
title: FAQ for generate content feature in Outlook
description: This FAQ provides information about the AI technology used in the generate content feature in Sales app, along with key considerations and details about how AI is used, how it was tested and evaluated, and any specific limitations.
ms.date: 06/26/2025
ms.custom: 
  - responsible-ai-faqs
ms.topic: faq
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.reviewer: shjais
---

# FAQ for generate content feature in Outlook

These frequently asked questions (FAQ) describe the AI impact of Sales app's generate content feature in Outlook.

## What is generate content feature in Outlook?

Sales app empowers salespeople to be more productive with their time by generating email drafts for them to send to their customers. By leveraging generative AI, it provides valuable assistance in crafting effective and personalized communication, saving time and enhancing the seller's writing skills.

## What are the feature's capabilities?

Sales app utilizes large language models (LLM), natural language processing (NLP), and machine learning algorithms to analyze salesperson input, customer data, and historical email interactions. It leverages this information to generate tailored email drafts by suggesting content, subject lines, and personalized messaging, enhancing the salesperson's ability to engage with customers effectively.

Sales app supports the following capabilities:

- **CRM-aware email generation**: When the seller's prompt or the email body indicates intent to reference CRM data, the generated draft includes relevant CRM record information—limited to accounts and opportunities—if that record is saved to the email. Only one CRM record is referenced per draft, based on what is associated with the email.
- **Meeting intent detection and time suggestions**: The system identifies if a meeting is being proposed and suggests appropriate times based on the seller's availability and working hours as per their calendar.
- **Tone and language refinement**: The system detects tone and language preferences from the prompt and adjusts the draft accordingly. 
- **Multilingual generation**: When a specific language is indicated in the seller's custom prompt, the email is generated in that language. If no language is specified, the system infers the language from the prompt. For out-of-the-box (OOB) prompts, the email is generated in the client's UI language set in Outlook.
- **Sales meeting summary email generation**: When a seller selects a specific sales meeting to summarize under **More options** in the **Draft an email** section while drafting an email in the Outlook side pane, the system generates a summary of the interaction and relevant action items or next steps. 

## What is the feature's intended use?

The intended use of this feature is to assist salespeople in creating effective and personalized email drafts to communicate with customers. It aims to save time, improve writing skills, and enhance customer engagement by providing content suggestions and guidance based on historical data and customer insights.

## How was the generate content feature evaluated? What metrics are used to measure performance?

The feature is evaluated through a combination of comparative analysis, human review, and customer engagement metrics. Performance is measured based on criteria such as accuracy, relevance, engagement, and customer satisfaction. Human reviewers assess the quality of system-generated content, ensuring it aligns with human-written drafts.

End-users provide ongoing feedback on each Copilot feature, along with iterative improvements contribute to optimizing the system's performance across all features.

## What are the limitations of this feature? How can users minimize the impact of the limitations when using the system?

The generated email drafts may not always fully capture the nuance, tone, or stylistic preferences of an individual salesperson. This might affect the degree of personalization and alignment with the seller's communication style.

Additionally, while the system can detect and incorporate CRM data when prompted, it only includes information from a single CRM record—specifically, the one saved to the email. If no CRM record is associated with the email, no CRM data will be referenced in the generated draft. 

To minimize the impact of these limitations:

- **Use clear prompts**: Provide specific instructions in the custom prompt—such as tone, language, meeting details, or CRM references—to help the system generate more accurate and relevant content.
- **Verify CRM associations**: Ensure that the appropriate CRM record (account or opportunity) is saved to the email if CRM data is expected to be included in the draft.
- **Adjust meeting suggestions**: Review suggested meeting times and adjust them as needed to better match your availability and the customer's preferences.
- **Meeting follow up**: Up to five recently transcribed Teams meetings with your sales contacts are available for summarization when you draft email in the Outlook side pane.

## What operational factors and settings allow for effective and responsible use of the system?

- **Data privacy and security**: Implement robust data privacy measures to protect customer information and ensure compliance with relevant regulations. Use secure communication channels and encryption methods to safeguard sensitive data.

- **User training and guidelines**: Provide comprehensive training to users on the system's features, capabilities, and limitations. Establish clear guidelines and best practices for responsible and ethical use, emphasizing the importance of accurate representation, respectful communication, and adherence to legal and ethical standards.

- **User permissions and access control**: Implement role-based access control to limit system functionalities and data access based on user roles and responsibilities. Ensure that users have appropriate permissions aligned with their job responsibilities and authorized access to customer data.

- **Monitoring and auditing**: Regularly monitor system usage, interactions, and outcomes to identify any potential issues or concerns. Conduct periodic audits to assess adherence to guidelines, data protection measures, and ethical practices.

- **Feedback and continuous improvement**: Encourage users to provide feedback on system performance, accuracy, and user experience. Actively seek user input to understand their needs and identify areas for improvement. Regularly update the system based on feedback and advancements in technology.

- **Transparency and explainability**: Foster transparency by clearly communicating to users how the system works, the underlying technologies used, and any limitations or potential biases. Ensure that users have a basic understanding of the system's capabilities and are informed about its AI-powered nature.

- **Accountability and error correction**: Establish mechanisms for addressing errors or inaccuracies that may occur in system-generated content. Encourage users to review and correct any inaccuracies, taking responsibility for the final output, and ensuring it aligns with their knowledge and expertise.


### Related information

- [Draft an email message in Sales app](use-copilot-kickstart-email-messages.md)
- [Draft an email message using sales information with Copilot in Outlook](email-reply-premium.md)
