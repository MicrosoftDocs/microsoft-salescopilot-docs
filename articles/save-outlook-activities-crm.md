---
title: Save Outlook activities to your CRM
description: Learn how to use Copilot for Sales to save your Outlook emails and meetings to Dynamics 365 or Salesforce CRM.
ms.date: 06/10/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Save Outlook activities to your CRM

As a seller, you can save all outgoing and incoming communication with your customers in the CRM system. This way, everyone in your company can see the relevant activities and use them to build advanced services that help you sell more.

But updating the CRM with all your activities across all the communication channels you use is tedious and time-consuming. Therefore, Copilot for Sales lets you save your Outlook interactions (emails and meetings) to the CRM with a single click.

> [!NOTE]
>
> - If you are using Dynamics 365 as your CRM and have saved an email to Dynamics 365, any replies to the email are saved to CRM automatically if [server-side synchronization](/power-platform/admin/server-side-synchronization) is enabled and if any option other than **No email messages** is selected under the [Email tab in Personalization Settings](/power-apps/user/set-personal-options#email-tab-options) in Dynamics 365.
> - If you are using Dynamics 365 as your CRM, you can save draft emails and appointments to Dynamics 365. The email is not saved to the CRM immediately, but only after it is sent. The appointment is saved immediately to the CRM. If you update the appointment after it is saved to the CRM, the changes are saved to the CRM automatically.
> - Saving Outlook activities from shared mailboxes is not supported.
> - If you are using Salesforce as your CRM, you can't save draft emails and appointments to Salesforce. Replies to saved emails and updates to saved events are not automatically saved either. 
> - Saving recurring meetings to your CRM is not supported.
> - If you've saved an Outlook activity (email or appointment) using Dynamics 365 App for Outlook, it's not shown as saved in Copilot for Sales. You must save the Outlook activity using Copilot for Sales. If you save the Outlook activity again using Copilot for Sales, a duplicate record is created in CRM.

## Save Outlook activities from the highlight card

To sync an email or meeting from Outlook with your CRM, follow these steps: 

1. Open the email or meeting you want to save to the CRM, and then open Copilot for Sales.

1. On the **Save email to (CRM)** card, select **Save**.

    :::image type="content" source="media/highlights-save.png" alt-text="Screenshot showing the Save email to CRM button.":::   

    If you connect Copilot for Sales to your Dynamics 365 environment and [server-side synchronization](/power-platform/admin/server-side-synchronization) isn't enabled, you're prompted to enable server-side synchronization for your mailbox when you save an Outlook activity for the first time. For more information, see [Use server-side synchronization with Copilot for Sales](use-server-side-sync.md)

    Alternatively, you can also [save an Outlook activity to CRM from a related record card](#save-outlook-activities-from-a-related-record-card). 

1. Under **Connect to a record**, select the record you want to connect the activity to.

    By default, Copilot for Sales displays suggestions for accounts and opportunities that are related to contacts in the activity. A few AI-powered suggestions are provided for opportunities only when the email and meeting content is in English.

   You can choose one of the suggested records to connect to. You can also use the search box to find and connect to another record of any record type added to Copilot for Sales by your administrator.

    If you want to save the email or meeting to CRM without connecting to a record, select **Save without connecting**. The email or meeting will still be associated with contacts on the To, Cc, and Bcc fields.

    > [!NOTE]
    > - When you search for a record to connect to, the search results display the record name and the key fields selected by your administrator. For more information about key fields, see [Select key fields for the mini view](customize-forms-and-fields.md#select-key-fields-for-the-mini-view).
    > - You can connect to all record types that are enabled for activities and added to Copilot for Sales by your administrator. For more information about adding record types, see [Add a new record type (or a Salesforce object)](customize-forms-and-fields.md#add-a-new-record-type-or-a-salesforce-object).

   The **Related contacts** card shows the contacts in the activity, as this activity is shown in their timeline.

   :::image type="content" source="media/connect-record.png" alt-text="Screenshot showing Connect to a record to save email.":::

1. In the **Add email categories** section, enter the information to categorize the email or meeting in the CRM. These fields are displayed only if your administrator has [configured the fields for categorization](save-additional-details-outlook.md).

1. (Optional) Select and save the attachments that you'd like to store in the CRM.
   :::image type="content" source="media/save-attachments.png" alt-text="Screenshot of the save attachment option in the Copilot for Sales side pane."::: 

    The attachments are saved to the activity record related to the email or meeting in the CRM. [Unable to save the attachment? Learn why](#attachment-considerations)

1. Select **Save**.

   The email or meeting is connected to the selected record and saved in the CRM.
    - The Connected to card shows the connected record and its type.
    - The attachment icon shows the number of attachments saved to the CRM.
    - The tag icon shows the categorization fields, if you selected any.
    
   :::image type="content" source="media/saved-email.png" alt-text="Screenshot showing email saved to CRM.":::

   > [!NOTE]
   >
   > - If you use Salesforce as your CRM, and enhanced email is turned off, you might see an error message when saving Outlook activities. For information on how to resolve the error, see [Enhanced email turned off](https://go.microsoft.com/fwlink/p/?linkid=2243672). If you've contacted Microsoft Support to save Outlook activities without turning on enhanced email, the activity is saved as a task record in Salesforce. If enhanced email is turned on, the activity is saved as an email message record.
   >
   > - If you save an email to Salesforce CRM, and the number of characters in the Outlook email body (including HTML markup) exceeds the [maximum number of characters allowed to be stored in Salesforce email records](https://help.salesforce.com/s/articleView?id=000392839&type=1), the email is truncated and then saved. A message is displayed in the **Connected to** card about truncating the email.
   >  
   > :::image type="content" source="media/truncate.png" alt-text="Screenshot showing the email truncated message.":::


## Save Outlook activities from a related record card

Copilot for Sales displays records that are related to the saved contacts in the email in their respective record type cards. You can save the email to the CRM from these cards.

> [!NOTE]
> If you already saved the email or meeting to CRM from the highlight card, you can't save it again from the related record card.

1. Open the email or meeting you want to save to the CRM, and then open Copilot for Sales.

1. In the (record type) card, hover over the record to which you want to save the email or meeting, select **More actions** (**...**), and then select **Save email to (CRM)**. For example, if you want to save the email to the account, hover over the account in the **Accounts** card, select **More actions** (**...**), and then select **Save email to (CRM)**.

    You can also select a record to open its details and then select **More actions** (**...**) > **Save email to (CRM)**.

1. The email or meeting is connected to the selected record and saved in the CRM. The **Connected to** card shows the connected record and its type.

> [!NOTE]
> Attachments can't be saved from the related record card.

## Save Outlook activities through quick CRM actions in email banners

When you read a customer email from external contacts and have not saved the email in your CRM, the banner message at the top of the email enables you to save the email through quick CRM actions.

1. Open or compose an email with at least one external contact.

2. In the banner message, select **Save this email**.

3. In the **Copilot for Sales** pane, under **Connect to a record**, select the record you want to connect the meeting to. 

    :::image type="content" source="media/banner-save-email.png" alt-text="Screenshot showing banner message with quick action to save an email.":::

4. (Optional) Select and save the attachments that you'd like to store in the CRM. 

   The attachments are saved to the activity record related to the email or meeting in the CRM. [Unable to save the attachment? Learn why](#attachment-considerations)

4. Select **Save**.

Currently, banner messages with quick CRM actions are available on up to two external emails per day. If you wish to disable these banners, [ask your administrator to disable them](m365-admin-setting.md).

> [!NOTE]
> This capability is being rolled out gradually and is expected to be available by the end of May 2024 to all users

### Attachment considerations

When saving an email or meeting to the CRM, you can also choose to save the attachments that are part of the email or meeting. Consider the following limitations related to attachments:

- Only file types that are allowed by the CRM can be saved. Attachments that are too large or of disallowed type are not saved. Your CRM administrator can configure the file type and size restrictions. Any changes to these settings can take up to an hour to take effect in Copilot for Sales. For more information about configuring file type and size, see:

    - [Dynamics 365](/dynamics365/customer-service/administer/enable-file-attachments#configure-file-size-limit-and-file-extensions)
    - [Salesforce](https://help.salesforce.com/s/articleView?id=sf.collab_files_size_limits.htm&type=5)

- Inline attachments can't be saved to the CRM. Inline attachments are images or files that are displayed in the body of the email. For example, email signatures, images, or files that are pasted into the email body.
- Saving an attachment is only supported for emails and meetings saved from the highlight card and email banner. It's not supported for emails and meetings saved from the related record card.
- In Salesforce, the attachments are saved as [files](https://help.salesforce.com/s/articleView?id=000387434&type=1) in activity records.

## Edit the activity in Outlook

If you'd like to update the activity details in Outlook after saving it to the CRM, you can edit them and save the changes to the CRM again.

You can update the following fields in the activity:

- Connected record
- Email categories
- Related contacts

> [!NOTE]
> Editing is only available for activities saved to Dynamics 365. 

To edit, select (**&hellip;**) in the **Connected to** section in the Copilot for Sales side pane and select **Edit saved email details**, and make the necessary changes. 

:::image type="content" source="media/change-connected.png" alt-text="Screenshot of the options in the Connected to drop-down.":::

## Remove saved email from CRM

If you connect Copilot for Sales to your Dynamics 365 environment and enable [server-side synchronization](/power-platform/admin/server-side-synchronization), you can remove saved emails and meetings that are no longer relevant from the CRM using Copilot for Sales. This step helps you keep your CRM clean and current.

> [!NOTE]
> Removal is only available for activities saved to Dynamics 365. 

1. Open the email or meeting you saved to the CRM, and then open Copilot for Sales.

1. Select the **Dynamics 365** tab.

1. In the **Connected to** card, select **More actions** (**&hellip;**) > **Remove email from Dynamics 365**.

   :::image type="content" source="media/change-connected.png" alt-text="Screenshot of the options in the Connected to drop-down.":::

    This step deletes the email from Dynamics 365 and a confirmation message is displayed.
