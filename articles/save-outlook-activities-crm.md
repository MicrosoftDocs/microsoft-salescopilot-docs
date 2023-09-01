---
title: Save Outlook activities to your CRM
description: Learn how to save Outlook activities to your CRM.
ms.date: 08/28/2023
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Save Outlook activities to your CRM

As a seller, you can save all outgoing and incoming communication with your customers in the CRM system so that everyone in the company has full visibility in the CRM for relevant activities and to help your company build advanced services to maximize the value for sellers.

Updating the CRM with all your activities across all the communication channels you use is tedious, time-consuming work. However, Sales Copilot helps by allowing you to save your Outlook interactions (emails and meetings) to the CRM with a single click.

> [!NOTE]
>
> - If you are using Dynamics 365 as your CRM and have saved an email to Dynamics 365, any replies to the email are saved to CRM automatically if [server-side synchronization](/power-platform/admin/server-side-synchronization) is enabled and if any option other than **No email messages** is selected under the [Email tab in Personalization Settings](/power-apps/user/set-personal-options#email-tab-options) in Dynamics 365.
>
> - If you are using Dynamics 365 as your CRM, you can save draft emails to Dynamics 365. The email is not saved to the CRM immediately, but only after it is sent.
>
> - Saving Outlook activities from shared mailboxes is not supported.

1. Open the email or meeting you want to save to the CRM, and then open Sales Copilot.

1. On the **Highlights** tab, select **Save**.

    Alternately, you can also go to **Dynamics 365** or **Salesforce** tab, and then select **Save**.

   :::image type="content" source="media/highlights-save.png" alt-text="Screenshot showing the Save email to CRM button.":::

    If you've connected Sales Copilot to your Dynamics 365 environment and [server-side synchronization](/power-platform/admin/server-side-synchronization) is not enabled, you are prompted to enable server-side synchronization for your mailbox when you save an Outlook activity for the first time. More information: [Use server-side synchronization with Sales Copilot](use-server-side-sync.md)

1. Under **Connect to a record**, select the record you want to connect the activity to.

    By default, Sales Copilot displays the accounts and opportunities that are related to the contacts in the activity. You can choose one of the displayed records to connect to or use the search box to find and connect to another record of any record type added to Sales Copilot by your administrator.

    If you want to save the email or meeting to CRM without connecting to a record, select **Save without connecting**.

   > [!NOTE]
   >
   > - When you search for a record to connect to, the search results display the record name and the key fields selected by your administrator. For more information about key fields, see [Select key fields for the mini view](customize-forms-and-fields.md#select-key-fields-for-the-mini-view).
   >
   > - The record you can connect Outlook emails or meetings to may be limited by your CRM.
   >
      > - If you're using Dynamics 365 as your CRM, you can connect to all tables that are enabled for activities and added to Sales Copilot by your administrator.
   >
      > - If you're using Salesforce as your CRM, you can only connect to an object if it has been added to Sales Copilot by your administrator. The object can be of type Contract, Order, Campaign, Account, Opportunity, Product, Asset, Case, Solution, Quote, Work Order, Work Order Line Item, Entitlement, Service Contract, Contract Line Item, Location, Asset Relationship, List Email, Contact Request, Image, Work Plan, Work Plan Template, Work Plan Template Entry, Work Step, Work Step Template, Process Exception, Change Request, Incident, Problem, and Web Cart Document.

   The **Related contacts** card displays the contacts in the activity, as this activity will be displayed in their timeline.

   :::image type="content" source="media/connect-record.png" alt-text="Screenshot showing Connect to a record to save email.":::

1. Select **Save**.

    The email or meeting is connected to the selected record and saved in the CRM. The connected record and its type are displayed in the **Connected to** card.

   :::image type="content" source="media/saved-email.png" alt-text="Screenshot showing email saved to CRM.":::

   > [!NOTE]
   >
   > - If you're using Salesforce as your CRM, and enhanced email is turned off, you might see an error message when saving Outlook activities. For information on how to resolve the error, go to [Enhanced email turned off](https://go.microsoft.com/fwlink/p/?linkid=2243672). If you've contacted Microsoft Support to save Outlook activities without turning on enhanced email, the activity is saved as a task record in Salesforce. If enhanced email is turned on, the activity is saved as an email message record.
   >
   > - If you save an email to Salesforce CRM, and the number of characters in the Outlook email body (including HTML markup) exceeds the [maximum number of characters allowed to be stored in Salesforce email records](https://help.salesforce.com/s/articleView?id=000392839&type=1), the email is truncated and then saved. A message is displayed in the **Connected to** card about truncating the email.
   > :::image type="content" source="media/truncate.png" alt-text="Screenshot showing the email truncated message.":::

   If you need to change the record the activity is connected to, select **More actions** (**...**) > **Change connected record**, and then select another record to connect the email or meeting to.

   :::image type="content" source="media/change-connected.png" alt-text="Screenshot showing how to change the connected record.":::

   > [!NOTE]
   > If you save an email to Salesforce CRM, the option to change the connected record is not available.

## Remove saved email from CRM

If you've connected Sales Copilot to your Dynamics 365 environment and have [server-side synchronization](/power-platform/admin/server-side-synchronization) enabled, you can remove saved emails and meetings that are no longer relevant from the CRM using Sales Copilot. This helps you keep the CRM clean and current.

1. Open the email or meeting you saved to the CRM, and then open Sales Copilot.

1. Select the **Dynamics 365** tab.

1. In the **Connected to** card, select **More actions** (**...**) > **Remove email from Dynamics 365**.

   :::image type="content" source="media/remove.png" alt-text="Screenshot showing how to remove saved email from CRM.":::

    The email is deleted from Dynamics 365 and a confirmation message is displayed.
