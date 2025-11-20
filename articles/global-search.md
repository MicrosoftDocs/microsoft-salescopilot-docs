---
title: Search for a CRM record using the Sales app
description: Explore the Sales app CRM integration, which offers AI-based recommendations and user-initiated searches to efficiently deliver relevant records.
ms.date: 11/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:05/15/2024
---

# Search for a CRM record using the Sales app

With the Sales app, you can use the global search functionality to search for a customer relationship management (CRM) record at any time, regardless of the context. You can quickly reference records even if they aren't related to the current context. The search functionality is also available in a range of other scenarios, such as when you save an email or email summary to your CRM.

> [!NOTE]
> Global search returns only records of the record types that your administrator configured.

## Search for a record using global search

1. In the **Sales** pane, select the search icon in the upper-right corner.
1. In the search box, enter the name of the record to search for.
1. In the search results, select the record to view the details.

    :::image type="content" source="media/global-search.png" alt-text="Screenshot of search results returned by global search.":::

You can filter the search results by record type. The record types that are available for filtering depend on the record types that your administrator configured. The record types are shown above the list of search results. Select a record type to filter the search to results by that record type.

## Search for a record using other surfaces

You can also search for records in the following scenarios:

- [Saving an email or meeting to your CRM](save-outlook-activities-crm.md)
- Creating or editing a relationship for an existing record (for example, searching for an account when [you create a new contact](create-contact-crm.md))
- [Saving a summary of an email or a meeting to your CRM](view-save-email-summary-crm.md)
- [Searching for a record that you want to share with a colleague](share-crm-record-teams-conversation.md)
- [Searching for an opportunity when you update your CRM with suggested updates](suggested-crm-updates.md#update-crm-with-suggested-updates)
- [Searching for a record when you create a CRM task from a meeting recap](view-meeting-summary-recap.md#create-a-crm-task-from-a-meeting-recap)

## Search features

When you open the search box in a context, the Sales app might use AI to proactively suggest records before you initiate a search. the Sales app takes advantage of contextual information, anticipates the records that you might be looking for, and presents them as options.

:::image type="content" source="media/ai-suggested-records.png" alt-text="Screenshot of AI-suggested records in global search.":::

When you search for a record in the Sales app, the search results are shown in a list that provides the following details:

- The name of the record.
- The type of record (for example, *Account*, *Contact*, or *Opportunity*). The search returns only records of the [record types that your administrator configured](customize-forms-and-fields.md).
- Up to two additional fields, based on the [key fields that your administrator configured](customize-forms-and-fields.md#select-key-fields-for-the-mini-view).

    > [!NOTE]
    > For Dynamics 365, the key fields must be configured as View Columns in the Quick Find View for the record type. Otherwise, the additional fields aren't shown in the search results.

### Filter search results 

To help you find the right record more easily, the Sales app provides filters that you can use to narrow down the search results. Filters are available for select record types and only when you save an email or a meeting to the CRM. The record types that are available for filtering depend on the record types that your administrator configured.

If the search results contain multiple records that have the same name, you can select each record to view more details. There is also a link that you can select to view the record in CRM. More details about a record are shown, based on the admin settings. These details are aligned with the [order of fields that are listed in the form configuration](customize-forms-and-fields.md#reorder-fields) for the record type.

When you expand the search results, you can view up to 10 fields. This number includes key fields. If fewer than 10 fields are configured, all fields are shown.

:::image type="content" source="media/global-search-features.png" alt-text="Screenshot of search results.":::

You can filter the search results by record details and record type.

**To filter the search results**:

1. [Save an email or a meeting to the CRM](save-outlook-activities-crm.md#save-from-the-highlight-card). 

2. Under **Connect to a record**, use the search box to find a record.

3. Select **Filter results** to filter the search results by record details and record type.

4. In the **Apply filters** box, select the filters that you want to apply. 

    - **Record details**: Filter the search results by **Active records** or **Owned by me**.
        > [!NOTE]
        > - For Dynamics 365 Sales, these filters apply to opportunities, accounts, and contacts. The **Active records** filter is based on the default **Status** field, and the **Owned by me** filter is based on the default **ownerId** field.
        > - For Salesforce, the **Active records** filter applies to opportunities and is based on the default **IsClosed** field. The **Owned by me** filter applies to opportunities, accounts, and contacts and is based on the default **ownerId** field.

    - **Record types**: Filter the search results by the record type.
        > [!NOTE]
        > The record types that are available for filtering depend on the record types that your administrator configured.

    :::image type="content" source="media/global-search-filter.png" alt-text="Screenshot of filter options.":::

5. Select **Apply**.

## How does search work in the Sales app?

The search functionality in the Sales app depends on the CRM system that you're using. You can enter search terms in any sequence, and they can encompass information from various fields.

### Dynamics 365

Dynamics 365 uses two search mechanisms: Dataverse search (also known as relevance search) and Quick Find search. Dataverse search is the recommended search mechanism and is used by default. However, Dynamics 365 administrators can disable it at both the organization level and the record type level. If Dataverse search is enabled, it forms the foundation for all Dynamics 365 search queries. If it's disabled for any record type that is included in the search, Quick Find search is used instead. More information: [Configure Dataverse search for your environment](/power-platform/admin/configure-relevance-search-organization)

To enable Dataverse search for a record type, admins must:

1. Enable Dataverse search in the Power Platform admin center.
1. Add the tables to the search index.
1. (Optional) Configure Quick Find Views for each table.

> [!NOTE]
> Changes made to the Dataverse search configuration or to the searchable data may take up to 15 minutes to appear in the search service. It may take up to an hour or more to complete a full sync for average size organizations, and a couple of days for very large size organizations.

It's crucial to understand that these search configurations affect all searches in Dynamics 365, not just searches in the Sales app. Other searches that use this configuration include lookups, Quick Find search, and Search this view on grid pages.

For both search mechanisms, only records that are visible in the Quick Find View are returned. Only columns that are configured as Find Columns are included in the search. Additionally, only columns that are configured as View Columns are returned in the search results. No other fields are shown in the Sales app.

### Salesforce

the Sales app uses Salesforce Object Search Language (SOSL) for search queries. Salesforce recommends this search mechanism because of its efficiency and comprehensive search capabilities. More information: [Introduction to SOQL and SOSL](https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql_sosl_intro.htm)

In Salesforce, all indexable fields of all eligible records are searched.
