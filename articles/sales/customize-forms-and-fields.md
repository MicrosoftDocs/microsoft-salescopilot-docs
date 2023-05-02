---
title: Customize forms and fields
description: Learn how to customize the CRM information your sellers see in Viva Sales.
ms.date: 05/17/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Customize forms and fields

As an administrator, you can customize the CRM information that's displayed in Viva Sales to give your sellers a more relevant view. To know more about privileges required to access administrator settings, see [Who can access administrator settings?](administrator-settings-for-viva-sales.md#who-can-access-administrator-settings).

CRM forms and fields customization is environment-specific—each environment has its own set of configurations. Contact, account, and opportunity record types are available by default. You can add other out-of-the-box and custom record types. You can perform following actions:

- **Add a new record type**: Add a new record type to Viva Sales. For example, you can add a custom record type called "Project" to track projects.
- **Change the view of a record type**: Select view to define how a list of records for a specific record type is displayed. For example, you can select a view to show only active accounts.
- **Control editing of records**: Control which records can be edited in Viva Sales.
- **Control new contact creation**: Control whether sellers can create new contacts and edit existing contacts inline in Viva Sales.
- **Manage fields**: Select the fields that will be shown in Viva Sales, and decide if sellers should be able to edit them.
- **Select key fields**: Choose which fields to show under record names when they're collapsed or in a list.

Record names, field names, and mandatory fields are displayed as they're defined in the CRM.

> [!NOTE]
> If you change the name of a record type in CRM, they are not updated in Adaptive Card or messaging extensions in Teams. For example, if you rename Account to Customer, the name in Adaptive Card and messaging extensions will show as Account.

## Prerequisites

CRM administrators must access administrator settings from the Viva Sales app in Teams. More information: [Administrator settings for Viva Sales](administrator-settings-for-viva-sales.md)

## Add a new record type

You can add new custom or out-of-the-box record types to Viva Sales. For example, you can add a custom record type called "Project" to track projects.

1. In Viva Sales admin settings, select **Forms**.

2. Select **Add a record type**.

3. In the **Add a record type** window, select a record type to add, and then select **Next**.

    > [!NOTE]
    > - Only record types that are related to a currently available record type are displayed. For example, contact, account, and opportunity record types are available by default, so you can add other out-of-the-box and custom record types that are related to these record types.
    > - You can add only one record type at a time.
    > - Logical names of record types and fields are displayed to optimize performance. 

4. In the **Select the relationship for (record type)** window, select the relationship to existing record types or fields in Viva Sales, and then select **Next**.

    > [!NOTE]
    > - Only 1:N and N:1 relationships are supported.
    > - Logical names of record types and fields are displayed to optimize performance.
    > - This step is displayed only if the record type you selected in the previous step relates to more than one record type or field. Otherwise, the relationship is automatically set.

5. In the **Select the view for (record type)** window, select the view to define how a list of records for a specific entity is displayed, and then select **Add**.

    > [!NOTE]
    > All public and personal views are displayed in the list. You can select only one view at a time.

6. On the record type settings page, select **Publish** to save your changes.


## Change view of a record type

You can change the view of a record type to define how a list of records for a specific record is displayed. For example, you can select a view to show only active accounts.

## View filter used in a view



## Remove a record type

You can remove a record type from Viva Sales. When you remove a record type that has related record types in Viva Sales, all related record types are also removed. The changes are automatically published. You can't remove the contact record type.

In Viva Sales admin settings, select **Forms**.
Hover over the record type you want to remove, and then select **Remove (record type) (:::image type="icon" source="media/delete-icon.png" border="false":::)**.

## Refresh data from CRM

You can refresh data to get recent changes from CRM into Viva Sales. For example, if you add a new field to a record type in CRM, you can refresh data to reflect the new field in Viva Sales. You can refresh data either for all record types or for a specific record type.

### Refresh data for all record types

1. In Viva Sales admin settings, select **Forms**.

2. Select **Refresh data**.

### Refresh data for a specific record type

1. In Viva Sales admin settings, select **Forms**.

2. Hover over the record type for which you want to refresh data, and then select **More options** (**...**).

3. Select **Refresh** from the context menu.

Alternatively, you can select the record type, and then select **Refresh data** under **Manage fields**.

## Control order of record types in side pane

You can control the order in which record types are displayed in the **Viva Sales** side pane in Outlook. The order is based on the order in which record types are added to Viva Sales. You can change the order by removing and adding record types in the desired order. Default order for new environments is contact, opportunity, and account. Newly added record types are added at the end of the list.

## Configure editing of records and fields

You can control which records and fields sellers can edit directly in Viva Sales. If a record isn't allowed to be edited in Viva Sales, sellers must update the record in the CRM.

By default, contacts are editable. For other records, you must turn on the option to allow editing.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE5fHzM]

**To allow editing of records**

1.  In Viva Sales admin settings, select **Forms**.

2.  Select a record type for which you need to allow editing.

    ![Screenshot showing Viva Sales Settings tab.](media/viva-sales-admin.png "Screenshot showing Viva Sales Settings tab.")

3.  Turn on **Allow editing** to allow sellers to edit all relevant fields in that record type.

4.  To restrict editing for specific fields, in the **Manage fields** section, and turn off **Allow editing** for corresponding fields.

    ![Screenshot showing how to enable editing of records and fields in Viva Sales.](media/viva-sales-allow-edit.png "Screenshot showing how to enable editing of records and fields in Viva Sales.")

5.  Select **Publish** to save your changes.

## Configure new contact creation

You can control whether sellers can create contacts inline, directly in Viva Sales, or must do so in the CRM. By default, new contacts are created inline in Viva Sales.

**To configure new contact creation**:

1.  In Viva Sales admin settings, select **Forms**.

2.  Select the **Contact** record type.

3.  Under **Allow editing**, select **Allow new contacts to be created directly from Viva Sales**.

    ![Screenshot showing how to configure contact creation in Viva Sales.](media/viva-sales-inline-contact-create.png "Screenshot showing how to configure contact creation in Viva Sales.")

4.  Select **Publish** to save your changes.

## Customize the detailed view

To customize the detailed view of CRM records in Viva Sales, select fields to include in the view and the order in which they should appear. Changes to the detailed view are reflected in the Viva Sales pane in Outlook and Adaptive Cards shared in Teams chat.

You can add up to 40 out-of-the-box and custom fields to a record form.

![Screenshot showing detailed view of CRM records in Viva Sales.](media/viva-sales-detailed-view.png "Screenshot showing detailed view of CRM records in Viva Sales.")

![Screenshot showing Adaptive card in Teams.](media/viva-sales-contact-card.png "Screenshot showing Adaptive card in Teams.")

### Add fields

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE5fC5a]

**To add fields**

1.  In Viva Sales admin settings, select **Forms**.

2.  Select a record type to which you need to add fields.

3.  In the **Manage fields** section, select **Add fields**.

    ![Screenshot showing how to add fields to a CRM record in Viva Sales.](media/viva-sales-add-fields.png "Screenshot showing how to add fields to a CRM record in Viva Sales.")

4.  In the **Add fields** window, select fields to display in the form, and then select **Add**.

    The new fields are added after existing fields, but you can [reorder them](#reorder-fields).

    > [!NOTE]
    > If you've connected Viva Sales to Salesforce, add only the fields that all users of Viva Sales have access to. If a user doesn't have access to some of the added fields, they'll not be able to view the CRM record.

5.  Select **Publish** to save your changes.

### Remove fields

1.  In Viva Sales admin settings, select **Forms**.

2.  Select the record type from which you need to remove fields.

3.  In the **Manage fields** section, hover over the field you want to remove from the form, and then select **Remove field** (![Delete icon.](media/delete-icon.png "Delete icon")).

4.  Select **Publish** to save your changes.

### Reorder fields

1.  In Viva Sales admin settings, select **Forms**.

2.  Select the record type in which you need to reorder fields.

3.  In the **Manage fields** section, hover over the field you want to reorder, and then select the **Move up** or **Move down** arrows (![Up arrow icon.](media/up-arrow-icon.png "Up arrow icon") ![Down arrow icon.](media/down-arrow-icon.png "Down arrow icon")).

    You can also drag the field to change its order.

4.  Select **Publish** to save your changes.

## Customize the mini view

Each record type has a mini view that displays limited information when they're collapsed or shown in a list. The mini view is available at various places in the Viva Sales pane, such as in the quick view on the CRM tab.

The mini view includes a fixed title and two configurable subtitle fields. The fields available in the mini view are the ones that are available in the detailed view.

![Screenshot showing mini view of CRM records in Viva Sales.](media/viva-sales-mini-view.png "Screenshot showing mini view of CRM records in Viva Sales.")

> [!NOTE]
> - Mini view settings affect the results when sellers search for connected records in Dynamics 365. In Dynamics 365, the search behavior for connected records depends on the quick find view. Make sure that the fields you select for the mini view exist in the quick find view, otherwise, the search list won’t show them. In Salesforce, the search is performed on the name and the additional fields selected for the mini view.
> - Key fields selected for accounts, contacts, and opportunities affect the search results displayed for these entities. Key fields are displayed, if they are not empty, along with the name of the record in the search results.

### Select fields for the mini view

1.  In Viva Sales admin settings, select **Forms**.

2.  Select the record type in which you need to select fields for mini view.

3.  In the **Key fields** section, select fields from the list.

    ![Screenshot showing how to select key fields for mini view in Viva Sales.](media/viva-sales-key-fields.png "Screenshot showing how to select key fields for mini view in Viva Sales.")

4.  Select **Publish** to save your changes.


## FAQ

### Are changes in the CRM reflected automatically in Viva Sales?

Changes made in the CRM aren't reflected automatically in Viva Sales. You must select **Refresh** on the **Customize forms and fields** page to get the latest updates from the CRM.

![Screenshot showing how to get latest changes from CRM.](media/viva-sales-crm-refresh.png "Screenshot showing how to get latest changes from CRM.")

### Why is the delete option disabled for some fields in the contact record?

If you enable new contact creation from within Viva Sales, you can't remove a field from the contact form if it's marked as required in CRM.

### Which fields can't be customized?

The following fields can't be added from the Viva Sales **Admin settings** page:

**Dynamics 365**

-   Fields of type File, Image, Rich text, or MultiSelect Option Set.

-   Entity Id

-   All fields where [**IsValidODataAttribute**](/dotnet/api/microsoft.xrm.sdk.metadata.attributemetadata.isvalidodataattribute?view=dataverse-sdk-latest&preserve-view=true) is set to false. 

**Salesforce**

-   Fields of type Geolocation, Text area (rich), Text area (encrypted), External Lookup Relationship, or Picklist (Multi-Select).

-   Entity Id

### How many fields can I add to a record?

You can add a maximum of 40 fields to a record.

### Why are some fields noneditable, although the record is set as editable?

A field can be noneditable in the following cases:
- The field is calculated
- The field is required in the CRM

### Why are users getting an error with error code 4100 when viewing a CRM record?

If you've connected Viva Sales to Salesforce, and your users see a 4100 error when viewing a CRM record, they don't have access to some of the fields added to be displayed. Ensure that all users of the app have access to the fields added to a CRM record.

