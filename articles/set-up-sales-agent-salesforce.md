---
title: Integrate Sales Agent (preview) with Salesforce
description: Learn how to integrate Sales Agent into Salesforce.
ms.date: 06/16/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Integrate Sales Agent (preview) with Salesforce

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/preview-note-d365.md)]

Sales Agent is a powerful tool that helps you automate your sales processes and improve your productivity. It helps sellers qualify leads by generating insights from research and generating personalized outreach emails tailored to the lead and its product of interest.

As an admin, you can set up Sales Agent to connect to your CRM and enable it for your users. Once set up, sellers can view summaries of the research within their CRM or browse the list of researched leads in the Copilot for Sales app.

These instructions cover the steps necessary to integrate the Sales Agent in Salesforce to give sellers the best experience in Salesforce.

## Prerequisites

- The Sales Agent has been configured and connected to Salesforce by following the steps to [set up the Sales Agent](set-up-sales-agent.md).
- You have access to environment-level settings in the [Copilot for Sales admin settings](administrator-settings-for-viva-sales.md).

## Create a link to Sales Agent research from leads

You can make it easy for Salesforce users to view the Sales Agent research by providing a direct link to the research from the CRM. Follow these steps to add a Sales Agent research link to Salesforce.

As an admin in Salesforce, open the **Setup** page and perform the following steps to add a link to research on the lead object:

1. In **Object Manager**, open the object that represents the leads researched by the Sales Agent For example, **Lead**.
1. Open **Fields & Relationships** and select **New** to create a new field.
1. Choose **Formula** as the Data Type and select **Next**
1. Configure the following field options and select **Next** when done:
    1. **Field Label**: Sales Agent Research
    1. **Field Name**: Sales_Agent_Research
    1. **Formula Return Type**: Text
1. Enter the following forumla into the formula text box and select **Next** when done:

    ```html
    HYPERLINK("https://teams.microsoft.com/v2/#/l/entity/c92c289e-ceb4-4755-819d-0d1dffdab6fa/homeTab?context=%7B%22subEntityId%22%3A%22%7B%5C%22route%5C%22%3A%5C%22/researchhub/lead/" & CASESAFEID(Id) & "%5C%22%7D%22%7D","Click here")
    ```

1. Set the visability to allow the field to be seen by the appropriate profile for your users. Set all profiles with visability to Read-Only. Select **Next**.
1. Add the field to the appropraite record pages and page layouts. Select **Next**.

## Show lead research summary on lead page

You can make a summary of the lead research available on each lead page. The summary provides a short summary of the information gathered about the lead, along with a link to view the full research details in the Copilot for Sales personal app.

> [!IMPORTANT]
> Sales Agent must be configured to [write summaries](set-up-sales-agent.md) into the **SalesAgentResearchSummaries** object and store a link to the summary from the lead in the **SalesAgentResearchSummary** field.

:::image type="content" source="./media/sales-agent-crm-summary.png" alt-text="Screenshot showing a CRM with the lead research summary card.":::

As an admin in Salesforce, open the **Setup** page and perform the following steps add the Sales Agent summary to your lead page.

### Upload Copilot for Sales logo
1. Navigate to **Custom Code** > **Static Resources** and select **New**.
1. Set the name of the resource to **copilot_for_sales_logo**.
1. Upload this image: :::image type="content" source="./media/copilot-for-sales-logo.png" alt-text="Copilot for Sales logo.":::

### Create Visualforce page for the Sales Agent summary
1. Navigate to **Custom Code** > **Visualforce Pages** and select **New**.
1. Set the label and name for the page as **Sales_Agent_Summary**.
1. Paste the following code into the **Visualforce markup** box:

    ```html
    <apex:page standardController="Lead" lightningStylesheets="true">
        <head>
            <script type="module" src="https://unpkg.com/@fluentui/web-components"/>
            <style>
              html * {
                font-size: 12px;
                line-height: 16px;
              }
              
              .title-text {
                font-weight: 600;
                text-align: left;
                color: #000000;
              }
              
              .summary-text {
                font-weight: 400;
                color: #424242;
    
              }
              
              .button-text {
                  font-weight: 600;
                  color: #242424;
                  margin-left: 5px;
              }
              
              .image {
                  width: 16px;
                  height: 16px;
                  vertical-align: middle
              }
            </style>
    
        </head>
        
        <apex:form >
            <div>
                <h3><apex:outputText value="Sales Agent" styleClass="title-text"/></h3>
            </div>
            <div>
                <apex:outputText value="{!Lead.SalesAgentResearchSummary__r.SummaryText__c}" styleClass="summary-text" escape="false"/>
            </div>
            <fluent-button onclick="window.open('https://teams.microsoft.com/v2/#/l/entity/c92c289e-ceb4-4755-819d-0d1dffdab6fa/homeTab?context=%7B%22subEntityId%22%3A%22%7B%5C%22route%5C%22%3A%5C%22/researchhub/lead/{!Lead.Id}%5C%22%7D%22%7D', '_blank')" title="Sales Agent">
                <apex:image value="{!$Resource.copilot_for_sales_logo}"
                    alt="logo"
                    styleClass="image"
                />
                <apex:outputText value="View research details" styleClass="button-text"/>
            </fluent-button>
        </apex:form>
    </apex:page>
    ```

1. Check the box to make the page **Available for Lightning Experience, Experience Builder sites, and the mobile app**.
1. **Save** the page.
1. From the list of pages, select **Security** for the **Sales Agent Summary** page and configure the page to be accessable to the appropriate profiles.

### Add the summary to the lead page
1. Open the **Lead Record Page** in the **Lightning App Builder** by navigating to a lead, selecting the setup icon, and choosing **Edit Page**.
1. In the left panel of the editor, search for the **Visualforce** component.
1. Drag the **Visualforce** component onto the canvas.
1. In the right panel of the editor, set the **Visualforce Page Name** to **Sales_Agent_Summary**
1. Deselect the **Show Label** checkbox.
1. Set the **Height (in pixels)** to **200**.
1. **Save** the page.

> [!TIP]
> If your leads are stored in an object other than the standard **Lead** object, you'll need to modify the code above to replace all references to the **Lead** object with the one that stores your leads.

## Related information

- [Set up Sales Agent](set-up-sales-agent.md)
- [Use Sales Agent](use-sales-agent.md)
