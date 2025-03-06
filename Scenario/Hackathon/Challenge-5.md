# Challenge 06: Configure an AI Hub and Promptflow
### Estimated Time: 90 minutes
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
   - Configure the flow by starting the **Compute session** and adding the Connection details such as AI search name, OpenAI name, and search_index name.
   - Test the flow by entering the prompts `Where can I ski?` and `How many free rooms do hotels in Switzerland have grouped by hotel on 2024-10-10?` in the chat. View the results returned by the flow.

1. **Deploy of configured prompt flow**

   - Deploy the prompt flow as a managed online endpoint for real-time inference, with Virtual machine SKU of **Standard_D2a_v4**.

     > **Note**: This may take up to 5 minutes to deploy.   

   - Copy the endpoint **Target URI** and **Primary key** into a notebook.

1. **Configure Network Security Group Rules for External Access**

   - In the **Network Security Groups (NSG)** of GPU Virtual Machine, configure **Inbound Security Rules** to allow traffic for the hackathon setup:  

      - Open port `9000` with the `TCP` protocol and set the priority to `100`.  
      - Open port `50551` with the `TCP` protocol and set the priority to `101`.  

   - Copy the **Public IP** of GPU Virtual Machine into a notebook. 
     
   - Open a new tab in the browser and navigate to the following URL to verify if the service is ready to handle inference requests.

      ```
      http://<nvidia-gpu-public-ip>:9000/v1/health/ready
      ```

      ![](../../media/web-trigger.png)

1. **Setting Up and Running the AI-Powered Speech-to-Text and Chat Application** 

   - **Clone the repository** in Visual Studio Code `https://github.com/CloudLabsAI-Azure/NVIDIA-Speech-to-text.git`.  
      > **Hint**: You can use the provided repository https://github.com/CloudLabsAI-Azure/NVIDIA-Speech-to-text. to explore and perform the scenarios listed below.  

   - **Install the prerequisites** from `requirements.txt`.  
      > **Hint**: Use `pip` to install the dependencies from `requirements.txt`.  

   - **Update the `.env` file** with the following details:  
      - **Public IP** of the GPU Virtual Machine  
      - **Target URI** of the endpoint  
      - **Primary Key**  

   - **Run the application** by executing `app.py` using Python.  

   - This application **supports both Riva Speech-to-Text and Chat with Azure AI services** running in **Prompt Flow**, which has been deployed.  

   - You can use **pre-created sample audio** files from the `audio` folder, such as:  
      - `Sample 1.wav` with the question **"Where can I ski?"**  
      - `Sample 2.wav` with the question **"How many free rooms do hotels in Switzerland have, grouped by hotel, on 2024-10-10?"**  

   - Alternatively, you can **record your own audio** and send it.

1. **Containerizing and Deploying the AI-Powered Speech-to-Text and Chat Application**  (Optional task)

- Package the application into a container and push it to **Azure Container Registry (ACR)**.  
- Create **Container Apps** for the AI-Powered Speech-to-Text and Chat Application.

## Success Criteria:

- You’ve successfully created a user in the PostgreSQL database.
- You’ve created a new AI Studio Hub and created a project.
- You’ve imported and configured a pre-built flow.
- You’ve tested the flow and confirmed that the flow returns appropriate results.
- Configure the necessary network security group rules to allow external access.
- Deploy the configured prompt flow to a virtual machine.
- Configure the necessary network security group rules to allow external access.
- Verify that the NVIDIA Riva ASR service is running and can handle inference requests.

## Additional Resources:

-  Refer to the [Secure Azure Database for PostgreSQL](https://learn.microsoft.com/en-us/training/modules/secure-azure-database-for-postgresql/) to learn about the security features of Azure Database for PostgreSQL.
-  Refer to the [Get started with prompt flow](https://learn.microsoft.com/en-us/training/modules/get-started-prompt-flow-ai-studio/) to learn about how to use prompt flow to develop applications that leverage language models in the Azure AI Foundry.
-  Refer to the [Deploy a flow in prompt flow](https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/how-to-deploy-for-real-time-inference?view=azureml-api-2) to learn about how to Deploy a flow as a managed online endpoint for real-time inference
- [az network nsg rule](https://learn.microsoft.com/en-us/cli/azure/network/nsg/rule?view=azure-cli-latest#az-network-nsg-rule-create)

