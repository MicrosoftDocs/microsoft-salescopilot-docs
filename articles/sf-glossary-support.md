---
title: Set up glossary terms for Salesforce
description: Glossaries in Dataverse help Sales agents interpret user queries by mapping custom terms to data, improving response accuracy. Learn how to set up yours.
ms.date: 04/28/2026
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
---

# Set up glossary terms for Salesforce

A glossary term is a word or phrase that users may use in their prompts, mapped to a specific meaning in your Dataverse tables. Each term includes a description and is associated with a particular skill, which scopes the glossary to a specific Salesforce organization or environment.

The following table shows examples of how adding glossary definitions can give your agent valuable context and improve its responses.

| Scenario                | Glossary term        | Example description     |
|-------------------------|---------------------|----------------------|
| Acronym                 | VP                  | VP stands for Vice President and refers to the value in the **JobTitle** column of the **Contact** table.                                                     |
| Custom ownership        | activity owner      | The activity owner is determined by the **PartyId** column in the **ActivityParty** table.                                                                    |
| Custom field            | opportunity revenue | Opportunity revenue refers to the **Custom Revenue** column in the **Opportunity** table.                                                                     |
| Complex rules or filter | overdue task        | An overdue task is a record in the **Task** table where the **State code** column is set to open and the **Scheduled end date** column is earlier than today.    |

> [!NOTE]
> - The descriptions in the table are provided as examples. Test your own descriptions to see which ones produce the best results.
> - Updates to glossary terms and definitions may take up to 15 minutes to become available.

## Prerequisites

- Access to the target Dataverse environment in Power Apps where Sales agent is installed (msdyn_viva environment).
- Permission to view and create rows in the Copilot glossary table (CopilotGlossary Terms).

## Add a glossary to your Salesforce organization

Use the following steps to create and publish a model-driven app for managing glossary terms.

1. [Create a custom model-driven app solution in Power Apps](/power-apps/maker/model-driven-apps/build-first-model-driven-app).
	1. Select the `msdyn_viva` environment.
	1. In the left navigation, select **Solutions**.
	1. Select **Managed solutions** and then select **New solution** on the command bar.
	1. Enter a **Display name** for the solution, for example, **Sales agent glossary**.
	1. Select a publisher, such as **CDS Default Publisher**.
	1. Select **Create**.

1. Add the glossary table to the solution.
	1. Inside the solution, select **Add existing** > **Table**.
	1. Search for the **CopilotGlossaryTerms** table.
	1. Select **Next**, and add the table to the app you created.

1. Configure and publish the model-driven app.
	1. Select the **CopilotGlossaryTerms** table in the solution.
	1. On the command bar, select **Create app** to create a new model-driven app from the solution.
	1. In the model-driven app designer, select **Data**.
	1. In the **Data** pane, search for the **CopilotGlossaryTerms** table, and then select **Add to app**.
	1. Publish the app.

1. Run the app and create glossary terms.
	1. Run the app you created.
	1. Open the **Active CopilotGlossaryTerms** view.
	1. On the command bar, select **New**.
	1. Enter the following values:
	  1. **Term**: The word or phrase users might use in prompts.
	  1. **Description**: The meaning of the term.
	  1. **Skill**: The skill this term is scoped to. Glossary terms are stored in Dataverse and associated with a specific skill name. Use the instructions in [Identify the skill name for glossary setup](#identify-the-skill-name-for-glossary-setup) and [Enter the skill name in the glossary term form](#enter-the-skill-name-in-the-glossary-term-form) to find and enter the correct value.


## Identify the skill name for glossary setup

Each Salesforce organization has a unique skill name suffix. You need to find the skill name that corresponds to the Salesforce organization you're setting up glossary terms for.

1. In Power Apps, open the environment where Sales agent is configured (the `msdyn_viva` environment).
1. Go to **Tables** > **All** and open the **msdyn_vivaorgsettings** table.
1. Look for rows where **FeatureName** starts with "SalesChatConfig". There may be multiple rows.
1. Find the row where **OrgId** matches your Salesforce Instance.
1. Copy the value from the **QnASearchConfigName** column. This is the value you enter in the **Skill** field when creating glossary terms.



## Enter the skill name in the glossary term form

When creating a glossary term, use the following steps to select the correct skill and save the term.

1. In the **Skill** field, select the search icon.
1. Select **Advanced**.
1. Under the advanced search bar, select the dropdown icon, then select **Default**.
1. Search for the skill name (for example, `SalesChatSalesforceQnA <yoursuffix>`), select the correct skill name, and select **Done**.
1. Once all fields are filled in, save the glossary term.
1. Repeat these steps to add as many glossary terms as needed for your Salesforce organization.

