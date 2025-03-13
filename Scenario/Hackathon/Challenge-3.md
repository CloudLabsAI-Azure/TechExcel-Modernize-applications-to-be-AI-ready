# Challenge 04: Split and Repackage the Contoso Hotel App Components and Deploy the Updated App

### Estimated Time: 45 Minutes

## Introduction

To improve the app's scalability, Contoso plans to split the frontend components (HTML, CSS, and JavaScript files) from backend components (APIs). In this challenge, you will split the components and refactor some code. Then, you will deploy the frontend and backend components to separate containers. Finally, you will push the containers to ACR and run the updated app.

## Challenge Objectives:

> **Important**: When deploying services in this challenge, please make sure to use the resource group named **Appmod** and use the same region as the resource group.

1. **Separate frontend components from backend components:**

   - Create a folder named **UpdatedApp** with subfolders **Frontend** and **Backend**.
   - Copy all frontend files to the **Frontend** folder and all backend files to the **Backend** folder.

1. **Refactor Files:**

   - **Frontend Folder**:

      - Open **views.py** from the Frontend folder in Visual Studio Code and remove the **Backend API endpoints** section.
      - Remove the **dblayer** reference from the **views.py Imports** section.
      - Remove the code from **views.py** that checks to see if the database is set up.
      - Update the **Dockerfile** to remove the code that installs the **MSSQL ODBC driver**.
      - Update **requirements.txt** to remove references to the **pyodbc** and **psycopg2-binary** libraries.

   - **Backend Folder**:   

      - Open **views.py** from the Backend folder in Visual Studio Code and remove the **Frontend API endpoints** section.

1. **Build the containers for frontend and backend components and push the containers to Azure:**   

   - Build separate containers for frontend and backend application components.
   - Run the **az containerapp env create** cmdlet to create an ACR environment for the app.
   - Create container apps for frontend and backend components.
   - Run the **az containerapp ingress cors** command to manage Cross-Origin Resource Sharing (CORS) policies for the container apps.

     <validation step="207cf525-c031-4b78-87e0-309f7f9f3b25" />   

## Success Criteria:

- You have created the UpdatedApp folder and the frontend and backend subfolders.
- You have copied the required files to the frontend and backend subfolders.
- You have updated the views.py, Dockerfile, and requirements.txt files in the Frontend folder and removed backend code and references to data libraries.
- You have updated views.py in the Backend folder and removed the frontend code.
- You have created Docker containers for frontend and backend application components.
- You have created an ACR environment and container apps.
- You have configured CORS policies.

## Additional Resources:

-  Refer to [Decompose a monolithic application](https://learn.microsoft.com/en-us/training/modules/microservices-architecture/) to learn about decomposing a monolithic application into a microservices architecture.

-  Refer to [az containerapp create](https://learn.microsoft.com/en-us/cli/azure/containerapp?view=azure-cli-latest#az-containerapp-create) to learn how to create an az container app.

## Proceed with the next challenge by clicking on **Next**>>.


