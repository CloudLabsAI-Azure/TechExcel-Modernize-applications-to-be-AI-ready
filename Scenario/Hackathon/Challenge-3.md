# Challenge 03: Split and repackage the Contoso Hotel app components and deploy the updated app

### Estimated Time: 45 minutes

## Introduction

To improve the scalability of the app, Contoso plans to split the front-end components (HTML, CSS, and JavaScript files) from back-end components (APIs). In this Challenge you’ll split the components and refactor some code. Then, you’ll deploy the front-end and back-end components to separate containers. Finally, you’ll push the containers to ACR and run the updated app.

## Challenge Objectives:

> **Important**: When deploying services in this challenge, please make sure to use the resource group named **Appmod** and use the same region as the resource group.

1. **Separate front-end components from back-end components:**

   - Create a folder named **UpdatedApp** with subfolders **FrontEnd** and **Backend**.
   - Copy all front-end files to the **FrontEnd** folder and all back-end files to the **Backend** folder.

1. **Refactor files:**

   - Open **views.py** from the FrontEnd folder in Visual Studio Code and remove the **Backend API endpoints** section.
   - Remove the **dblayer** reference from the **views.py Imports** section.
   - Remove the code from views.py that checks to see if the database is set up.
   - Update **Dockerfile** to remove the code that installs the **MSSQL ODBC driver**.
   - Update **requirements.txt** to remove references to the **pyodbc** and **psycopg2-binary** libraries.
   - Open **views.py** from the BackEnd folder in Visual Studio Code and remove the **Frontend API endpoints** section.

1. **Build the containers for front-end and back-end components and push the containers to Azure:**   

   - Build separate containers for front-end and back-end application components.
   - Run the **az containerapp env create** cmdlet to create an ACR environment for the app.
   - Create container apps for front-end and back-end components.
   - Run the **az containerapp ingress cors** command to manage Cross-Origin Resource Sharing (CORS) policies for the container apps.

## Success Criteria:

- You’ve created the UpdatedApp folder and the FrontEnd and Backend subfolders.
- You’ve copied the required files to the FrontEnd and Backend subfolders.
- You’ve updated views.py, Dockerfile, and requirements.txt files in the FrontEnd folder and removed back-end code and references to data libraries.
- You’ve updated views.py in the BackEnd folder and removed front-end code.
- You’ve created Docker containers for front-end and back-end application components.
- You’ve created an ACR environment and container apps.
- You’ve configured CORS policies.

## Additional Resources:

-  Refer [Decompose a monolithic application](https://learn.microsoft.com/en-us/training/modules/microservices-architecture/) to learn about decomposing a monolithic application into a microservices architecture

-  Refer to [az containerapp create](https://learn.microsoft.com/en-us/cli/azure/containerapp?view=azure-cli-latest#az-containerapp-create) to learn about creating az container app.

## Proceed with the next Challenge by clicking on **Next**>>.


