## Task 1: Generate NGC API KEY

> **Note:** This process of getting the NGC API key is no longer recommended. The participant is recommended to get the API key through build.nvidia.com as mentioned on the Scenario page.

The NVIDIA API key is a unique identifier used to authenticate requests to NVIDIA's APIs, such as the NGC (NVIDIA GPU Cloud) services. This key allows developers to access various resources, including pre-trained models, GPU-accelerated software, and container images. Obtaining an API key typically involves creating an account on NVIDIA's developer portal and generating the key within the account settings. It is important to keep this key secure, as it grants access to your NVIDIA resources and can be used for billing purposes.

1. **Go to [build.nvidia.com](https://build.nvidia.com)**

1. **Login or Create an Account**:
Click on the **Login** button in the top-right corner to create a new account. Enter your organization email to receive free credits to use NVIDIA NIM and click **Next**.

   ![build.nvidia.com](../media/nvaie-1.png)

   >**Note**: We recommend using your Email to log in, as this will provide you with 1,000 free credits. Alternatively, you can use the Username and Password available in the Environment tab to create an account; however, this option does not include free credits.

1. **Create Your NVIDIA Account**:
You will be redirected to a page where you can create your NVIDIA account. Provide your **Personal email address** **(1)** and then click on **Create (2)**.This account is required to download NIMs and start using them in your Azure platform.

   ![](../media/i-13.png)

1. On the **Create your Account**, page provide the following details and then click on **Create account (6)**.  

   - Email: Provide your **Personal email address (1)**
   - Password: Provide your **Password (2)**
   - Confirm password: Enter your password again **(3)**
   - Stay logged in: Check the box **(4)**
   - Enable **I am human** check box **(5)**

     >**Note:** You may be asked to choose the pictures. If requested, please complete and verify.

   ![](../media/i-14.png)

1. **Verify Your Email Address**:
Log into your **email** and you will get a verification code to your email to complete the verification process.

1. Enter the **code (1)** and click on **Continue (2)**.

   ![](../media/i15.png)

1. **Privacy Settings**:
Once verification is complete, you'll be redirected to a page with privacy-related questions. Choose your privacy settings and click **Submit**.

   ![](../media/nvaie-5.png)

1. **Create Your NGC (NVIDIA GPU Cloud) Account**:
In the next step, create your NGC account by providing your NVIDIA cloud account name. Provide any name for Account name and click on **Create NVDIA Cloud Account**.

   ![](../media/nvaie-6.png)

### Success!

You have successfully created your NVIDIA NVAIE and NVIDIA Cloud accounts. Verify that you are provided with free 1000 credits to try out NIMs.

   ![](../media/nvaie-credits.png)

### Explore NIMs:

- Now you can explore all available NIMs! Use the search bar at the top to search for any model or LLM task (e.g., search for "Llama" or "Retrieval").
- Explore the search results, open the NIM of interest, and experiment with it.
- You are provided with **1000 free credits**, each translating into one API call. Therefore, you have **1000 API calls** to try out the NIMs.

   ![](../media/nvaie-7.png)
  
- You can also call these NIMs in your Python application using the OpenAI library (refer to the Python code on the right) or using [NVIDIA LangChain endpoints](https://python.langchain.com/docs/integrations/chat/nvidia_ai_endpoints/).

   ![](../media/nvaie-8.png)

### Generate API Key

1. Now log in to [nvidia](https://ngc.nvidia.com/signin) account using your credentials to proceed. 

1. Enter your **Email address (1)** and click on **Continue (2)**.

   ![](../media/i-16.png)

1. On the **Set Your Profile** page, fill in your details and click **Submit**.

   ![](../media/i17.png)

1. If you receive a pop-up for **Set Email Preferences For Your Services**, simply click on **Close**.

   ![](../media/nvidia10.png)

1. Once your account is created or you've successfully logged in.

1. You will see a pop-up. On the **Set Email Preferences For Your Services** page, you can either **close** it or click **Set Email Preferences** to receive updates regarding security, announcements, and maintenance for all your services.

   ![](../media/nv8.png)

1. In the search bar, look for **Llama-3.1-8b-instruct**.

   ![](../media/nv7.png)

1. Scroll down and select **Llama-3.1-8b-instruct**. 

   ![](../media/nv6.png)

1. On the left-hand side, click **Get Container**.

   ![](../media/nv5.png)

1. A pop-up will appear on the **Approval Required** page. Click **Join** for the **NVIDIA Developer Program**, and it will redirect you to the NVIDIA Developer Portal.

   ![](../media/nv4.png)

1. On the **NVIDIA Developer Portal**, under **Integrate NIM into your application**, provide the necessary details (you can also provide random details) and click **Join**.

   ![](../media/nv3.png)

1. Navigate back to your **NVIDIA Account**. Select  **Organization**.

   ![](../media/i19.png)

1. click **Subscriptions (1)** on the left. Here, you will see the **Active (2)** status for the NVIDIA Developer Program.

   ![](../media/i20.png)

    >**Note**: Click on **Close**, if **Set Email Preferences For Your Services** pop up appears. 

1. Click on **Account** at the top of the page and navigate to the **Setup** section.

   ![](../media/nvidia4.png)

1. Click on **Generate API Key** to create a new key for accessing the necessary services.

   ![](../media/nvidia5.png)

1. From the top, click on **+ Generate API Key** to create a new API key.

   ![](../media/nvidia8.png)

1. Click on **Confirm** to generate your new API key.

   ![](../media/nvidia9.png)

1. Carefully copy and paste your generated **API key** in a notepad, essential for accessing various services and features paste the API key in the notebook. Ensure you store it securely, as it may not be displayed again after you leave the page.

   ![](../media/nvidia7.png)
