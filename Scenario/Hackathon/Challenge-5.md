# Challenge 05: Configure an AI Hub and Promptflow
### Estimated Time: 60 minutes
## Introduction

There are a lot of ways to create a chatbot. For this Challenge, you’ll use Prompt Flow within Azure AI Studio. Azure OpenAI Prompt Flow is a development tool designed to streamline the entire lifecycle of AI applications powered by Large Language Models (LLMs). Prompt Flow simplifies the process of prototyping, experimenting, iterating, and deploying AI applications.

Here's a simple overview of each service used:

- An **Azure AI Studio Hub** is a central resource within Azure AI Studio that helps teams manage, collaborate, and organize their AI projects.
- A **flow** encapsulates the logic that tells the chatbot what it can do and how to do things. Creating a flow can be complicated. For this challenge, you’ll use a pre-built flow. The flow uses the OpenAI API to directly query the Azure Search index.

## Challenge Objectives:

> **Important**: When deploying services in this challenge, please make sure to use the resource group named **Appmod** and use the same region as the resource group.

1. **Create a postgresql user and set up an AI Hub and Prompt Flow:**

   - Naviagte to **Cloud Shell** terminal in Azure portal and select **Bash**.
   - Enter the given commands at the Cloud Shell prompt to connect to the **database**.
   - Create a user for the **PostgreSQL database** that allows the chatbot read-only access to the Hotels, Visitors, and Bookings tables.
   -  Creates a unique name for an **AI Hub**. Set up and configure an **AI Studio Hub**.
   - Create a **project** in the **hub**.
   - Assign the **Storage Blob Data Owner** role to the newly created Storage account.
   - Assign the **Storage Blob Data Reader** role to the **AI Hub**.

1. **Import and configure a flow:** 

   - Create a New project named **contosopf** on the AI hub.
   - Navigate to **Prompt flow**, create a new flow by uploading **chatflow-oai-datasources..zip** zip file.
   - Import a pre-built flow into the project. 
   - Add a new connection to the external assets using **Custom keys** and **Azure AI Search**.
   - Configure the flow by starting the **Compute session** and adding the Connection details such as AI search name, OpenAI name and search_index name.
   - Test the flow by entering the prompts `Where can I ski?` and `How many free rooms do hotels in Switzerland have grouped by hotel on 2024-10-10?` in the chat. View the results returned by the flow.

## Success Criteria:

- You’ve successfully created a user in the PostgreSQL database.
- You’ve created a new AI Studio Hub and created a project.
- You’ve imported and configured a pre-built flow.
- You’ve tested the flow and confirmed that the flow returns appropriate results.

## Additional Resources:

-  Refer to the  [Secure Azure Database for PostgreSQL](https://learn.microsoft.com/en-us/training/modules/secure-azure-database-for-postgresql/) to learn about the security features of Azure Database for PostgreSQL.
-  Refer to the  [Get started with prompt flow](https://learn.microsoft.com/en-us/training/modules/get-started-prompt-flow-ai-studio/) to learn about how to use prompt flow to develop applications that leverage language models in the Azure AI Foundry.

