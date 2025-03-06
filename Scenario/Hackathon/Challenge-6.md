# Challenge 07: Integrate the chatbot with the Contoso Hotel application
### Estimated Time: 30 minutes
## Introduction

At this point you have a chatbot that can query the hotel brochures. In this Challenge, you will integrate the chatbot into the updated Contoso Hotel application.

## Challenge Objectives:

> **Important**: When deploying services in this challenge, please make sure to use the resource group named **Appmod** and use the same region as the resource group.

1. **Set up Visual Studio Code and run the flow locally:**

   - Navigate to `C:\Users\demouser\AssetsRepo\Assets` folder in the File explorer and extract the **lab-6-promptflow.zip** file. 
   - Launch Visual Studio Code as an **administrator** from the desktop and open the folder **lab-6-promptflow**. 
   - Rename the `.env.sample` file to `.env`. Create an environment file for the chatbot.
   - Create a connection to **Azure OpenAI**.
   - Installs all dependencies listed in the **requirements.txt** file by running `pip install -r requirements.txt` command.
   - Run the chatbot locally using the command `pf flow test --flow . --interactive` by giving the prompts **Where can I ski?** and **How many free rooms do hotels in Switzerland have grouped by hotel on 2024-10-10?** to test the chatbot.

1. **Deploy the flow to Azure Container apps and test the app:** 

   - Login to the Azure portal using `az login` command.
   - Login to acr, create the flow, build the container, containerize the flow and push the flow to ACR.
   - Create a Container app named **chatbot**, then deploy the container to ACR and configure environmental variables.
   - Update the **frontend** and **backend** application.
   - Navigate to the **chatbot** Application URL, enter the queries `Where can I ski?` and `How many free rooms do hotels in Switzerland have grouped by hotel on 2024-10-10`. View the results. the Contoso Hotel app to display the chatbot page.
   - Open a new web browser tab and navigate to the **Application URL** for **front-end** container. This will allow you to display the **chatbot** from within the updated Contoso Hotel app

     <validation step="487703c2-6b5c-4059-ae13-a8898f10f02e" />      

## Success Criteria:

- You’ve set up your development environment.
- You’ve tested the chatbot locally.
- You’ve updated the app to include the chatbot feature.


## Additional Resources:

-  Refer to the  [Prompt flow documentation](https://microsoft.github.io/promptflow/reference/pf-command-reference.html#pf-flow) to learn about the Promt flow.
