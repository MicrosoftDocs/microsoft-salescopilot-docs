---
title: Search for a CRM record using Copilot for Sales
description: Explore Copilot for Sales' CRM integration, offering AI-based recommendations and user-initiated searches to deliver relevant records efficiently.
ms.date: 05/30/2024
ms.topic: overview
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/15/2024
---

# Search for a CRM record using Copilot for Sales

You can search for a CRM record using Copilot for Sales at any time, regardless of the context, using the global search functionality. This feature allows you to quickly reference records, whether they are related to the current context or not. The search functionality is also available in various other surfaces such as saving an email or email summary to your CRM.

> [!NOTE]
> Global search returns only records that belong to the record types configured by your administrator. 


## Search for a record using global search

1. In **Copilot for Sales** pane, select the search icon in the upper-right corner.
1. In the search box, enter the name of the record you want to search for.
1. Select the record from the search results to view the details.

    :::image type="content" source="media/global-search.png" alt-text="Screenshot of the search results returned by global search.":::

## Search for a record using other surfaces

You can also search for records in the following scenarios:

- [Saving an email or meeting to your CRM](save-outlook-activities-crm.md)
- Creating or editing a relationship for an existing record. For example, searching for an account when [creating a new contact](create-contact-crm-sales-copilot.md).
- [Saving a summary of an email or a meeting to your CRM](view-save-email-summary-crm.md)
- [Searching for any record you wish to share with a colleague](share-crm-record-teams-conversation.md)
- [Changing the opportunity in key sales information](key-sales-info.md#change-the-opportunity)
- [Searching for an opportunity when updating CRM with suggested updates](suggested-crm-updates.md#update-crm-with-suggested-updates)
- [Searching for a record when creating a CRM task from meeting recap](view-meeting-summary-recap.md#create-a-crm-task-from-meeting-recap)


## Search features

When you open the search box in a context, Copilot for Sales might proactively suggest records using AI before you initiate a search. By leveraging contextual information, it anticipates the records you might be looking for and presents them as options.

:::image type="content" source="media/ai-suggested-records.png" alt-text="Screenshot of the AI-suggested records in global search.":::

When you search for a record in Copilot for Sales, the search results are displayed in a list with the following details:

- Name of the record. 
- Type of record (for example, account, contact, or opportunity). The search returns only those records that belong to the [record types configured by your administrator](customize-forms-and-fields.md). 
- Up to two additional fields based on the [key fields configured by the administrator](customize-forms-and-fields.md#select-key-fields-for-the-mini-view)

> [!NOTE]
> For Dynamics 365, if the key fields are not configured as **View Columns** in the **Quick Find View** for that record type, the additional fields are not displayed in the search results.

You can also filter the search results by record types. The record types available for filtering are based on the record types configured by the administrator. The record types are displayed above the search results list. You can select a record type to filter the search to results for that record type.

:::image type="content" source="media/global-search-filter.png" alt-text="Screenshot of the filter options in global search.":::

If the search results contain multiple records with the same name, you can select each record to view more details. It also includes a link to view the record in the CRM. More details about a record are displayed based on the admin settings. These details align with the [order of fields listed in the form configuration](customize-forms-and-fields.md#reorder-fields) for the respective record type.

When you expand the search results, you can view up to 10 fields. If less than 10 fields are configured, all fields are displayed. Key fields are included in the count of the 10 total fields displayed.

:::image type="content" source="media/global-search-features.png" alt-text="Screenshot of the search results.":::

## How does search work in Copilot for Sales?

The search functionality in Copilot for Sales depends on the CRM system you are using. You can enter search terms in any sequence and they can encompass information from various fields.

### Dynamics 365

Dynamics 365 uses two types of search mechanisms: Dataverse search (also known as relevance search) and Quick Find search. Dataverse search is the recommended search mechanism and is used by default. However, Dynamics 365 administrators have the ability to disable this at both the organization and record type levels. If relevance search is enabled, it forms the foundation for all Dynamics 365 search queries. If it's disabled for any record type included in the search, the Quick Find search is used. More information: [Configure Dataverse search for your environment](/power-platform/admin/configure-relevance-search-organization)

To enable Dataverse search for a record type, admins must:
1. Enable Dataverse search in the Power Platform admin center.
2. Add the tables to the search index.
3. (Optional) Configure Quick Find Views for each table.

It's crucial to understand that these search configurations impact all searches in Dynamics 365, not just those in Copilot for Sales. Other searches utilizing this configuration include lookups, quick find search, and search this view on grid pages.

In both types of searches, only records that are visible in the **Quick Find View** are returned. Only those columns configured as **Find Columns** are included in the search. Furthermore, only columns set as **View Columns** are returned in the search results. No other fields are displayed in Copilot for Sales.

### Salesforce

Copilot for Sales uses Salesforce Object Search Language (SOSL) for search queries. This search mechanism is recommended by Salesforce for its efficiency and comprehensive search capabilities. More information: [Introduction to SOQL and SOSL](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_sosl_intro.htm) 

In Salesforce, all indexable fields of all eligible records are searched.




