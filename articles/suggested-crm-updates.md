---
title: View suggested CRM updates
description: Learn how to use AI to suggest CRM updates based on email conversations.
ms.date: 09/29/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:02/15/2024
---

# View suggested CRM updates

When interacting with your customers over email, you often need to update your CRM system with the latest information. Manually updating the CRM system every time you interact with customers via email can be time-consuming and error prone. 

Copilot for Sales uses AI to suggest CRM updates based on the email conversations. Suggestions include update to estimated revenue and close date of the opportunity to which the email is connected. If the email isn't connected to an opportunity, you can choose an opportunity you want to update with the suggestions.

The suggestions are displayed in the **Suggested actions** card in the Copilot for Sales pane. If there are no suggestions, the card isn't displayed. When you update a record with the suggested updates, the suggestion is marked as complete.

:::image type="content" source="media/suggested-actions-card.png" alt-text="Screenshot showing Suggested actions card.":::

Here's the video that shows [how to view the opportunity summary](view-opportunity-summary.md) and update the CRM based on suggested updates:

> [!VIDEO 8f9ab913-0eec-48f5-a4ad-a1e3236482bd]

## License requirements

- [Sales](https://www.microsoft.com/en-us/microsoft-365/copilot/copilot-for-sales#Pricing)

## Update CRM with suggested updates

Copilot for Sales scans the email conversations and compares the data with the data in the CRM system to suggest updates. The updates are suggested for the following fields in an opportunity record in CRM system:

| Suggested update | CRM field |
|------------------|-----------|
| Budget | Dynamics 365 Sales: Est. Revenue (logical name: [estimatedvalue](/dynamics365/sales/developer/entities/opportunity#BKMK_EstimatedValue)) <br>Salesforce: Amount     |
| Close date | Dynamics 365 Sales: Est. Close Date (logical name: [estimatedclosedate](/dynamics365/sales/developer/entities/opportunity#BKMK_EstimatedCloseDate)) <br>Salesforce: Close Date |

### Update CRM from the Suggested actions card

1. In the Copilot for Sales pane, go to the **Suggested actions** card.

1. Select **Update opportunity** for the update you want to apply. Based on whether the email is connected to an opportunity or not, the following happens:

    - If the email is connected to an opportunity, the opportunity form opens in the Copilot for Sales pane.

        :::image type="content" source="media/suggested-data-review.png" alt-text="Screenshot showing opportunity form to review suggested updates.":::

    - If the email isn't connected to an opportunity, you're prompted to select an opportunity to update. Select an opportunity and proceed to the next step.

        :::image type="content" source="media/suggested-select-oppty.png" alt-text="Screenshot showing form to select an opportunity to update.":::

1. To change the opportunity, select **Choose a different opportunity** and select the opportunity you want to update.

1. Review the suggested update and update the value, if necessary.

1. Accept or reject the update by selecting the **Accept** or **Reject** icon.

1. Select **Update**. You're navigated to the **Suggested actions** card.

1. Update the next available suggestion, if necessary.

### Update CRM from record details

You can also update an opportunity record with the suggested updates when viewing its details in the Copilot for Sales pane. The updates are displayed in highlight cards above the opportunity details.

1. In the Copilot for Sales pane, [view details of an opportunity](view-record-details.md).

1. In the highlight card, select **Update opportunity** for the update you want to apply.

1. Review the suggested update and update the value, if necessary.

1. Accept or reject the update by selecting the **Accept** or **Reject** icon.

    :::image type="content" source="media/suggested-oppty-details.png" alt-text="Screenshot showing option to update opportunity from details view.":::

1. Select **Save**.

### Related information

[View opportunity summary](view-opportunity-summary.md)
