# Challenge 04: Set up Azure resources and extract data from hotel brochures
### Estimated Time: 45 minutes
## Introduction
When people are making travel plans, they often select a hotel based on the location of the hotel or the amenities that the hotel offers. Most hotel websites make it easy to search their hotels by date and location. However, it can be challenging to narrow down the list so that only hotels with specific amenities display.

Contoso wants to build a chatbot that helps potential guests find a hotel that meets their needs. For this solution, you’ll upload PDF versions of the Contoso Hotel brochures to an Azure Storage account. Then, you’ll use Azure Search service and Azure OpenAI service to scan the PDFs and extract information that a chatbot can use to respond to guest inquiries.

Here's a simple overview of each service used:

- **Azure Blob Storage:** Azure Blob Storage to contain the brochures for the hotels. Storing the brochures in Azure Blob Storage ensures that the brochures are available for searching by Azure AI Search Service.

- **Azure AI services:** Azure AI services is a set of cloud-based APIs that you can use in AI applications and data flows.

- **Azure AI Search:** Azure AI Search includes a wizard that allows you to import and vectorize data. You’ll use the wizard to extract and vectorize data from the hotel brochures.

## Challenge Objectives:

> **Important**: When deploying services in this challenge, please make sure to use the resource group named **Appmod** and use the same region as the resource group.

1. **Create Azure services:**

   - Create an **Azure Storage account** and **container**.
   - Clone the GitHub repository `https://github.com/microsoft/TechExcel-Modernize-applications-to-be-AI-ready.git`, which contains hotel brochures, into your folder named **AssetsRepo**.
   - Upload the brochures to the storage container.
   - Create an **Azure AI Search Service** instance.

1. **Configure managed identities for deployed Azure resources:**  

   - Configure the **Azure OpenAI** and **Azure AI Search** instances to use **system-assigned managed identities**.
   - Configure a managed identity to allow the **Azure AI Search** and **Azure OpenAI** instances to access the **Azure Blob Storage** account.
   - Configure a managed identity to allow **Azure AI Search** instance to access the **Azure OpenAI Service** instance.
   - Configure a managed identity to allow **Azure OpenAI Service** instance to access the **Azure AI Search** instance.

1. **Configure Azure AI Search to extract data from the brochures and test the search index:**

   - Launch the **import and vectorize data** and connect to **Azure Blob Storage**.
   - Create an **Azure OpenAI Service** instance and deploy models to the instance.
   - Vectorize text from the brochures.
   - Index the data.
   - Test the index by searching for `Skiing`. The results should list data about **skiing** and should also contain a text vector 

     <validation step="932c0914-39fe-4f3b-b876-6d0169c84b56" />   

## Success Criteria:

- You’ve uploaded the hotel brochures to the container in the Azure Storage account.
- You’ve created an Azure AI Search Service instance.
- You’ve configured managed identities so that the Azure Blob Storage account, Azure AI Search instance, and Azure OpenAI Service instance can communicate with each other.
- You’ve successfully completed all steps in the Import and vectorize data wizard.
- You’ve deployed models to an Azure OpenAI instance.
- You’ve tested the search index by using Search Explorer and can view results.

## Additional Resources:

- Refer to the [Implement managed identities](https://learn.microsoft.com/en-us/training/modules/implement-managed-identities/) to learn how managed identities can help you deploy secure solutions on Azure without the need to manage credentials.
- Refer to the [Azure Search Overview](https://learn.microsoft.com/en-us/azure/search/search-what-is-azure-search) to get additional information about Azure search.

## Proceed with the next Challenge by clicking on **Next**>>.   
