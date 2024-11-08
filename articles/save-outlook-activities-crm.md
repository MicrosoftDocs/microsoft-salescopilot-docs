---
title: Save Outlook activities to your CRM
description: Learn how to use Copilot for Sales to save your Outlook emails and meetings to Dynamics 365 or Salesforce CRM.
ms.date: 11/08/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Save Outlook activities to your CRM

As a seller, you can save all outgoing and incoming communication with your customers to your customer relationship management (CRM) system. In this way, everyone in your company can view the relevant activities and use them to build advanced services that help you sell more.

However, it's tedious and time-consuming to update the CRM with all your activities across all the communication channels that you use. Fortunately, you can use Copilot for Sales to save your Outlook interactions (emails and meetings) to the CRM in a single tap or click.

> [!NOTE]
> - If you use Dynamics 365 as your CRM, note the following points:
>
>    - When you save an email to Dynamics 365, replies to that email are automatically saved to the CRM if [server-side synchronization](/power-platform/admin/server-side-synchronization) is enabled, and if any option except **No email messages** is selected on the [Email tab](/power-apps/user/set-personal-options#email-tab-options) in Dynamics 365 personalization settings.
>    - You can save draft emails and draft appointments to Dynamics 365. Emails aren't immediately saved to the CRM. They are saved only after they are sent. Appointments are immediately saved to the CRM. If you update an appointment after it's saved to the CRM, the changes are automatically saved to the CRM.
>    - You can save an appointment to Dynamics 365 only if the appointment time is within the working hours of all participants. If the appointment time is outside the working hours of any participant, the appointment can't be saved to Dynamics 365. For information about how to set working hours for a user in Dynamics 365, go to [Set work hours for a user](/dynamics365/field-service/set-work-hours-resource#set-work-hours-for-a-user).
>
> - If you use Salesforce as your CRM, note the following points:
>
>    - You can't save draft emails and draft appointments to Salesforce.
>    - Replies to saved emails and updates to saved events aren't automatically saved.
>    - When you save an email or a meeting to Salesforce, it's shown as saved only for you and not for other participants in the email or meeting. Other participants must save the email or meeting to Salesforce separately.
>
> - Saving Outlook activities from shared mailboxes isn't supported.
> - Saving recurring meetings to the CRM isn't supported.
> - If you save an Outlook activity (email or appointment) by using Dynamics 365 App for Outlook, it isn't shown as saved in Copilot for Sales. You must save the Outlook activity by using Copilot for Sales. If you save the Outlook activity again by using Copilot for Sales, a duplicate record is created in your CRM.

## Save Outlook activities from the highlight card

To sync an email or meeting from Outlook with your CRM, follow these steps:

1. Open the email or meeting that you want to save to the CRM, and then open Copilot for Sales.
1. On the **Save email to \<*type of CRM system*\>** card, select **Save**.

    :::image type="content" source="media/highlights-save.png" alt-text="Screenshot showing the Save button on the Save email to Dynamics 365 card.":::

    If you connect Copilot for Sales to your Dynamics 365 environment, and [server-side synchronization](/power-platform/admin/server-side-synchronization) isn't enabled, you're prompted to enable server-side synchronization for your mailbox when you save an Outlook activity for the first time. For more information, go to [Use server-side synchronization with Copilot for Sales](use-server-side-sync.md).

    Alternatively, you can [save an Outlook activity to the CRM from a related record card](#save-outlook-activities-from-a-related-record-card).

1. Under **Connect to a record**, you can select the record that you want to connect the activity to.

    - By default, Copilot for Sales shows AI-powered suggestions for accounts and opportunities that are related to contacts in the activity. Select one of the suggested records to connect to it.

        > [!NOTE]
        > Some AI-powered suggestions for opportunities are provided only when the email and meeting content is in English.
    
    - Alternatively, use the search box to find and connect to another record of any record type that your administrator added to Copilot for Sales.
    - To save the email or meeting to the CRM without connecting to a record, select **Save without connecting**. The email or meeting is still associated with contacts in the **To**, **Cc**, and **Bcc** fields.

    > [!NOTE]
    > - When you search for a record to connect to, the search results show the record name and the key fields that your administrator selected. For more information about key fields, go to [Select key fields for the mini view](customize-forms-and-fields.md#select-key-fields-for-the-mini-view).
    > - You can connect to all record types that your administrator enabled for activities and added to Copilot for Sales. For information about how to add record types, go to [Add a new record type (or a Salesforce object)](customize-forms-and-fields.md#add-a-new-record-type-or-a-salesforce-object).

    The **Related contacts** card shows the contacts in the activity, because the activity is shown in their timeline.

    :::image type="content" source="media/connect-record.png" alt-text="Screenshot showing AI-powered suggestions and related contacts under Connect to a record.":::

1. In the **Add email categories** section, enter information to categorize the email or meeting in the CRM. The fields are shown only if your administrator [configured the fields for categorization](save-additional-details-outlook.md).
1. (Optional) Select and save the attachments that you want to store in the CRM.

1. In the **Save attachments** section, select and save the attachments that you'd like to store in the CRM. This section appears only if your administrator has [enabled the capability to save attachments](save-additional-details-outlook.md#configure-attachment-saving-settings).
   
    :::image type="content" source="media/save-attachments.png" alt-text="Screenshot of the save attachment option in the Copilot for Sales side pane."::: 

    The attachments are saved to the activity record that is related to the email or meeting in the CRM. [Unable to save the attachment? Learn why.](#attachment-considerations)

1. Select **Save**.

    The email or meeting is connected to the selected record and saved to the CRM.

    - The **Connected to** card shows the connected record and its type.
    - The attachment icon shows the number of attachments that were saved to the CRM.
    - The tag icon shows the number of categorization fields, if you selected any.

    :::image type="content" source="media/saved-email.png" alt-text="Screenshot showing an email that was saved to the CRM.":::

> [!NOTE]
> If you use Salesforce as your CRM, note the following points:
>
> - If enhanced email is turned off, you might receive an error message when you save Outlook activities. For information about how to fix the error, go to [Enhanced email turned off](https://go.microsoft.com/fwlink/p/?linkid=2243672). If you contacted Microsoft Support to save Outlook activities without turning on enhanced email, the activity is saved as a task record in Salesforce. If enhanced email is turned on, the activity is saved as an email message record.
> - If you save an email to Salesforce CRM, and the number of characters in the Outlook email body (including HTML markup) exceeds the [maximum number of characters that can be stored in Salesforce email records](https://help.salesforce.com/s/articleView?id=000392839&type=1), the email is truncated and then saved. A message about the truncation is shown on the **Connected to** card.
>
>    :::image type="content" source="media/truncate.png" alt-text="Screenshot showing the email truncation message on the Connected to card.":::

## Save Outlook activities from a related record card

Copilot for Sales shows records that are related to the saved contacts in an email. All records of the same record type appear on a card for that record type. From the cards, you can save the email to your CRM.

> [!NOTE]
> If you already saved the email or meeting to CRM from the highlight card, you can't save it again from a related record card.

1. Open the email or meeting that you want to save to the CRM, and then open Copilot for Sales.

1. In the (record type) card, hover over the record to which you want to save the email or meeting, select **More actions** (**...**), and then select **Save and connect email**. For example, if you want to save the email to the account, hover over the account in the **Accounts** card, select **More actions** (**...**), and then select **Save and connect email**.

    Alternatively, select a record to open its details. From the details, select **More actions** (**...**) > **Save and connect email**.

    The email or meeting is connected to the selected record and saved to the CRM. The **Connected to** card shows the connected record and its type.

> [!NOTE]
> - If your administrator has enabled the capability to save all attachments by default, the eligible attachments are saved to the CRM automatically. 
> - If your administrator has disabled the capability to save attachments or turned off the capability to save all attachments by default, attachments are not saved to the CRM.

## Save Outlook activities through quick CRM actions in email banners

When you read a customer email from external contacts, if you didn't save the email to your CRM, the banner message at the top of the email includes a quick CRM action that you can use to save the email.

1. Open an email that has at least one external contact.
1. In the banner message, select **Save this email**.
1. In the **Copilot for Sales** pane, under **Connect to a record**, select the record that you want to connect the meeting to.

    :::image type="content" source="media/banner-save-email.png" alt-text="Screenshot showing a banner message with a quick action for saving an email.":::

1. (Optional) Select and save the attachments that you want to store in the CRM.

    The attachments are saved to the activity record that is related to the email or meeting in the CRM. [Unable to save the attachment? Learn why.](#attachment-considerations)

1. Select **Save**.

> [!NOTE]
> - Currently, banner messages that include quick CRM actions are available on up to two external emails per user per day. If you don't want these banners to appear, [ask your administrator to disable them](m365-admin-setting.md).

### Attachment considerations

When you save an email or meeting to your CRM, you can also save any attachments that are part of the email or meeting. However, consider the following limitations that are related to attachments:

- Attachments that are too large or of a disallowed file type can't be saved to the CRM. Your CRM administrator configures the file type and size restrictions. Any changes to that configuration can take up to an hour to take effect in Copilot for Sales. For more information about how to configure file type and size restrictions, go to:

    - For Dynamics 365: [Configure file size limit and file extensions](/dynamics365/customer-service/administer/enable-file-attachments#configure-file-size-limit-and-file-extensions)
    - For Salesforce: [File Size and Sharing Limits](https://help.salesforce.com/s/articleView?id=sf.collab_files_size_limits.htm&type=5)

- Inline attachments can't be saved to the CRM. Inline attachments are images or files that are displayed in the body of an email. Examples include email signatures, images, or files that are pasted into the email body.
- In Salesforce, attachments are saved as [files](https://help.salesforce.com/s/articleView?id=000387434&type=1) in activity records.
- In Dynamics 365, if attachment saving for appointments is turned off in server-side synchronization, attachments for meetings can't be saved to CRM from Copilot for Sales. Learn more about [syncing appointment attachments](/power-platform/admin/sync-logic#syncing-appointment-attachments).

> [!NOTE]
> The **Save attachments** section appears only if your administrator has [enabled the capability to save attachments](save-additional-details-outlook.md#configure-attachment-saving-settings).

## Edit activities in Outlook

If you want to update the details of an activity in Outlook after you save the activity to your CRM, you can edit them and then save the changes to the CRM again.

You can update the following fields in the activity:

- Connected record
- Email categories
- Related contacts

> [!NOTE]
> Editing is available only for activities that were saved to Dynamics 365.

To edit an activity, select the **More actions** button (**&hellip;**) on the **Connected to** card in the Copilot for Sales side pane, select **Edit saved email details**, and make the necessary changes.

:::image type="content" source="media/change-connected.png" alt-text="Screenshot showing the Edit saved email details option on the More actions menu on the Connected to card.":::

## Remove saved emails from your CRM

If you connect Copilot for Sales to your Dynamics 365 environment and enable [server-side synchronization](/power-platform/admin/server-side-synchronization), you can use Copilot for Sales to remove saved emails and meetings that are no longer relevant from your CRM. In this way, you help keep the CRM clean and current.

> [!NOTE]
> Removal is available only for activities that were saved to Dynamics 365.

1. Open the email or meeting that you saved to the CRM, and then open Copilot for Sales.
1. Select the **Dynamics 365** tab.
1. On the **Connected to** card, select the **More actions** button (**&hellip;**), and then select **Remove email from Dynamics 365**.

    :::image type="content" source="media/change-connected.png" alt-text="Screenshot showing the Remove email from Dynamics 365 option on the More actions menu on the Connected to card.":::

    The email is deleted from Dynamics 365, and you receive a confirmation message.

### See also

[Configure how Outlook emails and events are saved to CRM](save-additional-details-outlook.md)
