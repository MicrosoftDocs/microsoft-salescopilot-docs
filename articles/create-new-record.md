---
title: Create a new record in your CRM from Copilot for Sales
description: Learn how to create a new record in your CRM from Copilot for Sales.
ms.date: 07/05/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Create a new record in your CRM from Copilot for Sales

You can create a new record in your CRM from the Copilot for Sales side pane. This capability is useful when you want to create a new record in your CRM without having to go to the CRM system. New record creation is supported for all record types that your administrator adds to Copilot for Sales.

> [!NOTE]
> - The option to create a new record is available only if your [administrator enables it](customize-forms-and-fields.md#configure-new-record-creation).
> - For each record type, your CRM administrator can enable inline creation, creation in CRM, or both.

## Create a new record by using the global option

1. In the **Copilot for Sales** pane, select the plus sign (**+**) in the upper-right corner.

    :::image type="content" source="media/global-create.png" alt-text="Screenshot showing the global option to create a new record.":::

1. In the **Choose which type of record to create** step, the following options are shown for the record types, based on the configuration of new record creation:

    - **Create**: This option is shown if both inline creation and creation in CRM are enabled for the record type. Select this option, and then select the appropriate action.
    - **Create record**: This option is shown if only inline creation is enabled for the record type.
    - **Create in CRM**: This option is shown if only creation in CRM is enabled for the record type.

    :::image type="content" source="media/choose-create-record.png" alt-text="Screenshot showing record types that can be created.":::

> [!NOTE]
> You can also create a new record when you search for a record to [save the email to](save-outlook-activities-crm.md).

## Create a new record from a related record card

Copilot for Sales shows records that are related to the saved contacts in the email on the appropriate record type cards. You can create a new record from a related record card. This capability is useful when you want to create a new record that is related to an existing record without having to go to the CRM system.

1. In the **Copilot for Sales** pane, go to the related record card that you want to create a new record for.
1. Select the plus sign (**+**) in the upper-right corner.

    :::image type="content" source="media/related-record-create.png" alt-text="Screenshot showing the option to create a new record from a related record card.":::

1. Based on the configuration of new record creation, the following behavior occurs:

    - If only inline creation or only creation in CRM is enabled for the record type, a new record is created based on the enabled configuration.
    - If both inline creation and creation in CRM are enabled for the record type, the following options are shown:

        - **Create record**: Create a new record inline in the **Copilot for Sales** pane.
        - **Create in CRM**: Create a new record in the CRM system.

### Related information

[Create a contact in your CRM from Copilot for Sales](create-contact-crm-sales-copilot.md)<br>
[Configure new record creation](customize-forms-and-fields.md#configure-new-record-creation)
