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

   - Create a user for the PostgreSQL database that allows the chatbot read-only access to the Hotels, Visitors, and Bookings tables.
   - Set up and configure an AI Studio Hub.
   - Create a project in the hub.

1. **Import and configure a flow:** 

   - Import a pre-built flow into the project. 
   - Configure the flow.
   - Test the flow.

## Success Criteria:

- You’ve successfully created a user in the PostgreSQL database.
- You’ve created a new AI Studio Hub and created a project.
- You’ve imported and configured a pre-built flow.
- You’ve tested the flow and confirmed that the flow returns appropriate results.

## Additional Resources:

-  Refer to the  [Secure Azure Database for PostgreSQL](https://learn.microsoft.com/en-us/training/modules/secure-azure-database-for-postgresql/) to learn about the security features of Azure Database for PostgreSQL.
-  Refer to the  [Get started with prompt flow](https://learn.microsoft.com/en-us/training/modules/get-started-prompt-flow-ai-studio/) to learn about how to use prompt flow to develop applications that leverage language models in the Azure AI Foundry.

