---
title: Save Outlook activities to your CRM
description: Learn how to save your Outlook emails and meetings to your Dynamics 365 or Salesforce CRM with Copilot for Sales.
ms.date: 02/20/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Save Outlook activities to your CRM

Sellers often need to capture emails and meetings that are related to their sales activities. In the past, you might have recorded the details in a paper notebook. Today, you're more likely to use a customer relationship management (CRM) system like Dynamics 365 or Salesforce. However, it's still tedious and time-consuming to manually update the CRM with the details of your Outlook interactions with leads and customers. Fortunately, Copilot for Sales can do it for you so that you can focus on selling.

When an email or meeting is saved to the CRM, the Copilot for Sales side pane shows the following information:

- The **Connected to** card shows the connected record and its type.
- The attachment icon shows the number of attachments that were saved to the CRM.
- The tag icon shows the number of categorization fields, if any, that you selected.

:::image type="content" source="media/saved-email.png" alt-text="Screenshot showing an email that was saved to the CRM.":::

Copilot for Sales can save emails and meetings to your CRM from the highlight card, from a related record card, or through quick CRM actions in email banner messages. However, you can't save activities from shared mailboxes, and you can't save recurring meetings. If you use Dynamics 365 as your CRM, you can edit saved activities and remove saved emails from the CRM.

Here's the video that shows how to save an email to CRM using Copilot for Sales:

> [!VIDEO 58889511-ae98-4933-a317-204bfda884b6]

## Save from the highlight card

1. Open the email or meeting, and then open Copilot for Sales.

1. In the Copilot for Sales side pane, select **Save**.

    :::image type="content" source="media/highlights-save.png" alt-text="Screenshot showing the Save email to CRM highlight card in the Copilot for Sales side pane.":::

1. Under **Connect to a record**, select a record to connect the email or meeting to.

    - Select a suggested record: Copilot for Sales uses AI to suggest accounts and opportunities that are related to contacts in the activity. Some suggestions for opportunities are provided only when the email or meeting content is in English.

    - Search for a record to select: Use the search box to find and connect to a record of any type that your administrator added to Copilot for Sales.

    - Save without selecting a record: Select **Save without connecting** to save the email or meeting to the CRM without connecting it to a record. It's still associated with contacts in the **To**, **Cc**, and **Bcc** fields.

    > [!NOTE]
    > - When you search for a record to connect to, the search results show the record name and the [key fields that your administrator selected](customize-forms-and-fields.md#select-key-fields-for-the-mini-view).
    > - You can connect to all [record types that your administrator enabled for activities and added to Copilot for Sales](customize-forms-and-fields.md#add-a-new-record-type-or-a-salesforce-object).

    The **Related contacts** card shows the contacts that are in the email or meeting because the activity appears in their timeline.

    :::image type="content" source="media/connect-record.png" alt-text="Screenshot showing suggested connections and related contacts under Connect to a record.":::

1. If your CRM has fields for categorizing saved emails and meetings, you can select one or more under **Add email categories**.

1. If your CRM allows you to save files that are attached to an email or meeting, you can select the ones you want to save with the activity. [Can't save an attachment?](#limitations-when-saving-attachments)

    :::image type="content" source="media/save-attachments.png" alt-text="Screenshot of the Save attachments option in the Copilot for Sales side pane.":::

1. Select **Save**.

## Save from a related record card

Copilot for Sales shows records that are related to contacts that are saved in the CRM. All records of the same type, such as accounts or opportunities, appear on a card for that type. You can save the email or meeting to your CRM from these cards. If you already saved it to the CRM from the highlight card, you can't save it again from a related record card.

1. Open the email or meeting, and then open Copilot for Sales.

1. Hover over a record and select **More actions** (**&hellip;**) > **Save and connect email**.

    Alternatively, select a record to open its details. From the details, select **More actions** (**&hellip;**) > **Save and connect email**.

The email or meeting is connected to the selected record and saved to the CRM. The **Connected to** card shows the connected record and its type.

Attachments are handled differently when you save an activity from a related record card:

- If your CRM is set up to save all attachments by default, then all attachments that can be saved to the CRM are saved automatically.

- If your CRM isn't set up to save all attachments by default, or to save any attachments at all, then no attachments are saved to the CRM.

## Save from quick CRM actions in an email banner message

When you read an email from an external contact and you haven't already saved it, a banner message at the top includes a quick action that you can use to save the email to your CRM.

1. Open an email that you haven't saved to your CRM and that has at least one external contact.

1. In the banner message, select **Save this email**.

1. In the Copilot for Sales side pane, under **Connect to a record**, select a record.

    :::image type="content" source="media/banner-save-email.png" alt-text="Screenshot of an email with a quick CRM actions banner message and the Copilot for Sales side pane.":::

1. If your CRM allows you to save files that are attached to an email, you can select the ones you want to save with the activity. [Can't save an attachment?](#limitations-when-saving-attachments)

1. Select **Save**.

Copilot for Sales can show a banner message that includes quick CRM actions in up to two of your external emails per day. If you don't want these banners to appear, ask your administrator to turn them off for your mailbox.

## Open saved activities in your CRM

After you save an email or meeting to your CRM, you can open it from the **Email from** or meeting title card in the Copilot for Sales side pane. This helps you quickly find the activity in your CRM if you want to see more details or make changes.

1. Open the email or meeting, and then open Copilot for Sales.
1. On the **Email from** or **meeting title** card, select **More actions** (**&hellip;**) > **Open in (CRM)**.

    :::image type="content" source="media/open-in-crm.png" alt-text="Screenshot of the Email from card in the Copilot for Sales side pane, showing the More actions menu with the Open in Dynamics 365 option highlighted.":::

## Edit activities saved to Dynamics 365

If you use Dynamics 365 as your CRM, you can change some of the details of a saved email or meeting in Copilot for Sales and then save the changes to the CRM. You can change the record the activity is connected to, its email categories, and related contacts. If you use Salesforce as your CRM, you can't edit saved activities in Copilot for Sales.

1. Open an email or meeting, and then open Copilot for Sales.

1. On the **Connected to** card, select **More actions** (**&hellip;**) > **Edit saved email details**.

    :::image type="content" source="media/change-email-fields.png" alt-text="Screenshot of the Connected to card in the Copilot for Sales side pane, showing the More actions menu with the edit option highlighted.":::

## Remove emails saved to Dynamics 365

If you use Dynamics 365 as your CRM, you can use Copilot for Sales to remove saved emails and meetings that are no longer relevant, keeping the CRM clean and up to date. If you use Salesforce as your CRM, you can't remove saved activities in Copilot for Sales.

1. Open an email or meeting, and then open Copilot for Sales.

1. On the **Connected to** card, select **More actions** (**&hellip;**) > **Remove email from Dynamics 365**.

    :::image type="content" source="media/remove-email-from-crm.png" alt-text="Screenshot of the Connected to card in the Copilot for Sales side pane, showing the More actions menu with the remove option highlighted.":::

## Limitations when saving attachments

If your CRM administrator has turned on the capability to save attachments, then when you save an email or a meeting to your CRM, you can also save its attachments. However, keep the following limitations in mind:

- Your CRM administrator determines the file types and maximum allowed size of attachments that can be saved to the CRM. Attachments that are of a disallowed file type or too large can't be saved.

- Inline attachments can't be saved to the CRM. Inline attachments are images or files that are displayed or pasted in the body of an email.

## Differences between Dynamics 365 and Salesforce

Copilot for Sales works a little differently depending on which CRM you use. The differences are described in the following sections.

### When you save activities to Dynamics 365

- If a notification about server-side synchronization appears when you try to save an email or meeting, it means that your mailbox isn't set up to save Outlook activities to Dynamics 365. Select **Turn on** to turn on server-side synchronization for your mailbox. Learn more in [Use server-side synchronization with Copilot for Sales](use-server-side-sync.md).

    :::image type="content" source="media/highlight-save-server-side-sync-notice.png" alt-text="Screenshot showing the server-side sync notice in the Copilot for Sales side pane.":::

- Replies to a saved email are also saved automatically *if* both of the following conditions are true:

  - [Server-side synchronization](./use-server-side-sync.md) is turned on for your mailbox.
  - **No email messages** is *not* selected on the **Email** tab in your [Dynamics 365 personalization settings](/power-apps/user/set-personal-options#email-tab-options).

- You can save a meeting to Dynamics 365 only if the meeting time is within the working hours of *all* participants. Learn how to set your own working hours in [Personailze sales accelerator](/dynamics365/sales/personalize-sales-accelerator#configure-your-work-availability). Sales managers can [set the availability](/dynamics365/sales/manage-seller-availability) of sellers who report to them.

- If saving attachments to meetings is turned off in server-side synchronization settings, meeting attachments can't be saved to the CRM from Copilot for Sales.

- You can save draft emails to Dynamics 365; however, a draft email is saved only after it's sent.

- You can save draft meetings to Dynamics 365. Draft meetings are saved immediately. If you update a meeting after it's saved, the changes are automatically saved to the CRM.

- Only activities that you save using Copilot for Sales appear in the Copilot for Sales side pane. If you used [Dynamics 365 App for Outlook](/dynamics365/outlook-app/user/track-message-or-appointment) to connect an email or a meeting to a record in your CRM, it isn't shown as saved in Copilot for Sales. If you use Copilot for Sales to save the activity, a duplicate record is created in the CRM.

- You can [edit saved activities](#edit-activities-saved-to-dynamics-365) in Outlook and save your changes to Dynamics 365.

### When you save activities to Salesforce

- You can't save draft emails or draft meetings to Salesforce.

- Replies to saved emails and updates to saved meetings aren't automatically saved.

- When you save an email or a meeting to Salesforce, it's shown as saved for you only. Other participants must save the email or meeting to Salesforce separately.

- You can't edit saved activities.

- [Attachments are saved as files in activity records](https://help.salesforce.com/s/articleView?id=000387434&type=1).

- If a notification to update settings in Salesforce appears when you try to save an Outlook activity, it means that Enhanced Email is turned off in Salesforce. Learn more in [Can't save an email to CRM when Enhanced Email isn't enabled in Salesforce CRM](https://go.microsoft.com/fwlink/p/?linkid=2243672).

    If Enhanced Email is turned on, an activity is saved as an email record in Salesforce. If your administrator contacted Microsoft Support to allow Outlook activities to be saved without turning on Enhanced Email, an activity is saved as a task record.

- If an email that you save has more characters in the message body than the [maximum number of characters that can be stored in Salesforce email records](https://help.salesforce.com/s/articleView?id=000392839&type=1), the email is truncated and then saved. The **Connected to** card includes a notice to that effect.

    :::image type="content" source="media/truncate.png" alt-text="Screenshot of the Connected to card in Copilot for Sales, showing that an email saved to Salesforce was truncated.":::
