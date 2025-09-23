---
title: Sales Chat overview (preview)
description: 
ms.date: 09/09/2025
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ai-usage: ai-assisted
---

# Sales Chat overview (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Sales Chat is a conversational agent available within Microsoft 365 Copilot Chat. It enables sellers to efficiently search, synthesize, and take action on sales data from various applications they use.

Traditional sales CRM systems are primarily designed to capture information and prevent knowledge loss, but they often make it difficult to quickly retrieve and analyze data. For instance, creating a status report on an account typically requires sellers to navigate through multiple CRM pages and other applications to gather details about past purchases, marketing interactions, and more.

As a seller, you can use natural language with Sales Chat to request the information you need. The system handles the complex task of identifying and compiling relevant data, making it easier and faster for sellers to access insights and take action.

## What can Sales Chat help you with?

You can use natural language with Sales Chat to query and get insights from data in your connected CRM and past customer conversations. All CRM queries adhere to your security access level—if you do not have permission to view certain data in the CRM, that information is not available in Sales Chat.

Below are some example scenarios where you can use Sales Chat, along with sample prompts for each.

### Scenario 1: Become an expert on your accounts

This scenario is ideal for users who:

- Recently took over an account that was previously managed by other teams.
- Work on an account with multiple touchpoints across the business.
- Want to quickly get up to speed on an account they plan to engage with.

#### Information prompts

- Get me all accounts in the `<vertical name>` industry as a table and order it by estimated revenue from open opportunities.
- Get me the account summary for `<account name>`. Organize the opportunities in a table sorted by close date
- What is the number of employees at `<account name>`?
- What is the opportunity pipeline for `<account name>`?
- Briefly summarize the discussion on `<topic>` with `<account name>`.
- Has `<account name>` mentioned any competitors in past meetings?

#### Relationship prompts

- Who is the primary customer contact for `<account name>`?
- Who at my company has the best relationship with `<account name>` based on recent meetings? List the key topics of interest for the customer.
- Who are the internal champions at `<account name>` based on recent meetings that I should reach out to?

#### Action prompts

- Who is the primary contact at `<account name>`? Draft an email to them asking for time to meet.
- Who is the account owner of `<account name>`? Draft an email to them asking for time to meet about the open opportunities at `<account name>`. Include details and links to the open opportunities at `<account name>` in the email for context.

### Scenario 2: Be prepared and confident in customer meetings

This scenario is ideal for users who:

- Manage accounts with multiple meetings involving various stakeholders and team members within the company.
- Need to catch up on meetings they have not attended.
- Want reminders of previous interactions and engagements to stay up to date with the latest insights.

#### Know what is top of mind for customers

- What was discussed in the previous meeting with `<account name>`?
- What's `<account name>`'s sentiment based on recent meetings? Summarize the top 3 positive and negative feedback from contacts.
- Summarize the discussions with `<account name>` in the last month. List the top 5 topics of interest to them.

#### Be prepared to address open items

- What are the follow-ups tasks from recent meetings with `<account name>`? Categorize by Owner. Sort the tasks by due date.
- Are there any open incidents for `<account name>`? Show the cases a table with one row for each case. For each case, show details about the case title, owner, status, creation date and number of days since case was created as columns.

### Scenario 3: Pipeline review and deal coaching

This scenario is ideal for users who:

- Want to review their opportunity pipeline and identify areas for improvement.
- Need coaching on specific deals to increase their chances of closing.
- Want to ensure they are following best practices in their sales process.

#### Analyze your pipeline health

- Get the estimated revenue across opportunities by forecast category
- Get the list of opportunities owned by `<seller name>` in the "Pipeline" forecasting category. Show the results in a table with one row for each opportunity. Each row should have four columns, one each for opportunity title, account name, estimated value and close date.
- What are the top 5 opportunities by estimated revenue that have a target close date this quarter?
- What are the largest opportunities by revenue owned by `<seller name>`?
- Get me the accounts owned by `<seller name>`. What is the estimated revenue from open opportunities in each account? Show as a table and sort by estimated revenue

#### Get coaching to close on deals faster

- When did `<seller name>` last meet with `<account name>`?
- Does `<contact name>` at `<account name>` have a good sentiment on `<topic>`? What should `<seller name>` do to impress her?
- What are the top three concerns of `<account name>` that `<seller name>` must address to close the deal with them?

> [!NOTE]
> - The effectiveness of prompts depends on the quality and structure of your CRM data. Sales Chat generates responses based on your data, so maintaining a strong data foundation is essential.
> - For prompts related to previous meetings, ensure that customer meetings are scheduled in Teams by Copilot for Sales users and that, at a minimum, a transcription is generated.
> - You are encouraged to try prompts beyond the provided samples to discover additional capabilities.

## Getting started

Sales Chat is configured by your administrator to help you converse with your sales data. Learn more about how to [set up Sales Chat](set-up-sales-chat.md).

Once configured, you can start using Sales Chat to ask questions about your sales data and get insights to help you close deals faster. Learn more about how to [use Sales Chat](use-sales-chat.md).

## Related information

- [Set up Sales Chat](set-up-sales-chat.md)
- [Use Sales Chat](use-sales-chat.md)
