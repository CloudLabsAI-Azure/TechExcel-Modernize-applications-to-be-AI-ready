# Challenge 02: Deploy and review the legacy Contoso Hotel app
### Estimated Time: 45 minutes
## Introduction

The legacy Contoso Hotel app was written by using Python code. App components run inside a Docker container. The app can connect to a SQL Server or PostgreSQL database (on-premises or online).

In this challenge, you will deploy a legacy application to a Docker container and run it successfully. The process begins with building a Docker container for the application by creating a Docker image. Next, you will create an Azure Container Registry (ACR) instance to securely store and manage the app’s container image before pushing the image to the registry. To support the application, you will provision a managed PostgreSQL database instance on Azure, ensuring the app has the necessary backend for data storage. Finally, you will run the containerized application, review its functionality, and test it by adding a new booking. This challenge provides hands-on experience with Docker, Azure Container Registry, and PostgreSQL while working on a practical deployment scenario.

Here's a simple overview of each service used by the app:

- **Docker:** Docker is an open-source platform that automates the deployment, scaling, and management of applications. It uses containerization technology to package an application and its dependencies into a container, ensuring that it runs consistently across different environments.
- **Azure Container Registry (ACR):** Azure Container Registry (ACR) is a managed, private Docker registry service provided by Microsoft Azure. It allows you to store and manage container images and artifacts in a secure and scalable manner.
- **PostgreSQL:** PostgreSQL is a powerful, open-source relational database management system (RDBMS). It’s known for its robustness, extensibility, and standards compliance. Azure Database for PostgreSQL Flexible Server is a fully managed database service designed to provide more granular control and flexibility over database management functions and configuration settings.

## Prerequisites

Make sure you have the following from the CloudLabs-provided integrated environment:

> Note: Prerequisites are already set up in the CloudLabs-provided environment. If you're using your personal computer or laptop, please make sure that all necessary prerequisites are installed to complete this hackathon.

  - [Azure Subscription](https://azure.microsoft.com/en-us/free/)
  - [Azure OpenAI](https://aka.ms/oai/access) access is available with the following models:
    - gpt-4o
    - text-embedding-ada-002
   - Bicep 
   - Az PowerShell module
   - Azure CLI
   - Git
   - Poweshell 7 
   - Prompt flow
   - Docker Desktop

## Challenge Objectives:

> **Important**: When deploying services in this challenge, please make sure to use the resource group named **Appmod**. 

1. **Clone the Repository:**
   - Clone the repository within Visual Studio Code: `https://github.com/qxsch/ContosoHotel.git`.
     > Hint : You can utilize the following repository, https://github.com/qxsch/ContosoHotel.git, to explore and perform the scenarios listed below.   

1. **Build a Docker container for the app:**

   - Launch Docker Desktop. Verify that the Docker engine is running.   
   - Builds the container for the app within the **ContosoHotel** folder, where the cloned repository resides.

1. **Create an Azure Container Registry (ACR) instance and push the app container to ACR:**

   - Creates an ACR instance with a basic SKU within the **Appmod** resource group inside the **ContosoHotel** folder.
   - Sign in to ACR. Creates a Docker tag for the app and then pushe the app container to ACR.

1. **Provision a PostgreSQL database to support the app:**   

   - Run the **Connect-AzAccount** cmdlet to connect Visual Studio Code to Azure with an authenticated account
   - Run the **manageIac.ps1** script from the **ContosoHotel\iac** folder to deploy an Azure Database for PostgreSQL Flexible Server instance.
   > **Note** : Ensure to use the same region as you used in the challenge 1.  
   > **Note**: Make sure to use **Appmod** resource group.

1. **Run the containerized app and add a booking:**

   - Run the containerized app on port 8000
   - Paste the following URL `http://localhost:8000/setup` in a web browser.
   - Run the setup process in the app to add records to the database.
   - Review the app pages.
   - Add the booking record.
   - Verify that the new record is saved and close the browser window.

## Success Criteria:

- Verify that the Docker engine is running.
- You’ve built a Docker container for the app.
- Created an Azure Container Registry instance.
- You’ve pushed the app container to ACR.
- You’ve provisioned an Azure Database for PostgreSQL Flexible Server instance.
- You can view the app in a web browser.
- You can add a booking record to the app and verify that the record is saved and is searchable.

## Additional Resources:

-  Refer to the  [Introduction to Docker container](https://learn.microsoft.com/en-us/training/modules/intro-to-docker-containers/) for detailed information on the Docker container.
-  [Build a containerized web application with Docker](https://learn.microsoft.com/en-us/training/modules/intro-to-containers/)
-  [Manage container images in Azure Container Registry](https://learn.microsoft.com/en-us/training/modules/publish-container-image-to-azure-container-registry/)
-  [Explore PostgreSQL architecture](https://learn.microsoft.com/en-us/training/modules/explore-postgresql-architecture/)


## Proceed with the next Challenge by clicking on **Next**>>.   

