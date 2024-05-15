---
title: Search experiences in Copilot for Sales
description: Explore Copilot for Sales' CRM integration, offering AI-based recommendations and user-initiated searches to deliver relevant records efficiently.
ms.date: 05/17/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/15/2024
---

# Search experiences in Copilot for Sales

Copilot for Sales integrates CRM directly into the seller's workflow. A crucial aspect of this is presenting the appropriate records at the right moment. This can be achieved through:

- AI-based recommendations
- User-initiated searches

This dual approach effortlessly delivers relevant records to users through AI, while also offering search support for instances where the user is seeking something specific.

This article primarily discusses the implementation of user-initiated searches and the surfaces where they are provided, but it also mentions available AI capabilities.

## Search surfaces and scenarios

The search functionality in Copilot for Sales spans across various surfaces and scenarios. The following is a detailed overview of these surfaces, their implementations, and their respective functionalities.

- **Save to CRM**: [Save an email or meeting to your CRM](save-outlook-activities-crm.md). It helps in finding the record in CRM that the email or meeting should be associated with.
- **Record lookup**: Create or edit a relationship for an existing record. For example, search for an account when [creating a new contact](create-contact-crm-sales-copilot.md).
- **Save summary**: [Save a summary of an email or a meeting to your CRM](view-save-email-summary-crm.md). It helps in finding the record to which the summary should be added.
- **Global search**: Search for any record at any time. It's useful for quickly referencing records, regardless of whether they are related to the current context or not.
- **Message extension search**: [Search for any record you wish to share with a colleague](share-crm-record-teams-conversation.md), for example, in Teams. The chosen records are then shared as adaptive cards.

## Search details

When you search for a record in Copilot for Sales, the search results are displayed in a list with the following details:
- Name of the record
- Type of the record (for example, account, contact, or opportunity)
- Up to two additional fields based on the [key fields configured by the administrator](customize-forms-and-fields.md#select-key-fields-for-the-mini-view)

> [!NOTE]
> For Dynamics 365, if the key fields are not configured as **View Columns** in the **Quick Find View** for that record type, the additional fields are not displayed in the search results.

### Record type filering

Some of the searches in Copilot for Sales offer the ability to fitler resuls by record types. The record types available for filtering are based on the record types configured by the administrator. The record types are displayed as tabs above the search results list. You can select a tab to view the search results for that record type.

### AI ranker for opportunities

The AI ranker in Copilot for Sales proactively suggests opportunities before you initiate a search. By leveraging contextual information, it anticipates the records you might be looking for and presents them as options. This eliminates the need for explicit user input.

### Record disambiguation

Record disambiguation in Copilot for Sales allows you to expand the search results to view extra details about each record and includes a link to view the record in the CRM. This is helpful when naming conventions result in multiple records with similar titles. The extra details displayed are dependent on the admin settings. For Salesforce, these details align with the [order of fields listed in the form configuration](customize-forms-and-fields.md#reorder-fields) for the respective record type. For Dynamics 365, they correspond to the [order of the **View Columns** defined in the **Quick Find View**](/power-platform/admin/configure-relevance-search-organization#select-searchable-fields-and-filters-for-each-table) for that record type in Dataverse. 

When you expand the search results, you can view up to 10 fields. If less than 10 fields are configured, all fields are displayed. Key fields are included in the count of the 10 total fields displayed.

## How does search work in Copilot for Sales?

The search functionality in Copilot for Sales depends on the CRM system you are using. You can enter search terms in any sequence and they can encompass information from various fields. However, the behavior of the search functionality varies significantly between Dynamics 365 and Salesforce.

In Dynamics 365, the search functionality is based on the **Quick Find View** for each record type. Only the fields that are configured in the **Find Columns** of each record type's **Quick Find View** are included in the search. The search results display the fields that are configured as **View Columns** in the **Quick Find View** for that record type.

In Salesforce, all fields of all eligible records are searched. The search results display all fields that are configured in the admin settings. 

## What's used for search in Copilot for Sales?

### Dynamics 365

Dataverse search (also known as relevance search) is the recommended search mechanism and is used by default in our APIs. However, Dynamics 365 administrators have the ability to disable this at both the organization and record type levels. If relevance search is enabled, it forms the foundation for all our Dynamics 365 search queries. If it's disabled for any record type included in the search, we fallback to the Quick Find search. More information: [Configure Dataverse search for your environment](/power-platform/admin/configure-relevance-search-organization)

To enable Dataverse search for a record type, admins must:
1. Enable Dataverse search in the Power Platform admin center.
2. Add the tables to the search index.
3. (Optional) Configure Quick Find Views for each table.

It's crucial to understand that these search configurations impact all searches in Dynamics 365, not just those in Copilot for Sales. Other searches utilizing this configuration include lookups, quick find search, and search this view on grid pages.

In both types of searches, only records that are visible in the **Quick Find View** are returned. Only those columns configured as **Find Columns** are included in the search. Furthermore, only columns set as **View Columns** are returned in the search results. No other fields are displayed in Copilot for Sales.
 
### Salesforce

Salesforce Object Search Language (SOSL) is a highly efficient and comprehensive search option provided by Salesforce. It is recommended by Salesforce itself, takes relevancy into account, and is utilized by Salesforce's Einstein search. On the other hand,  Salesforce Object Query Language (SOQL) offers a more focused search, designed in the style of a database query. More information: [Introduction to SOQL and SOSL](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_sosl_intro.htm) 






