# Building an Event-Driven Azure Function for Blob Storage Triggers

## Overview

In this scenario, you will create an Azure Function App using Visual Studio Code (VS Code) and integrate it with an Azure Storage Account. The Storage Account will have a container named "images" where uploaded files will be stored. The Azure Function will be configured to trigger automatically whenever a new image is uploaded to the container. Upon triggering, the function will display the name and size of the uploaded image, demonstrating how serverless functions can process events in real-time.

## Objective

This exercise is designed to provide hands-on experience in setting up an event-driven Azure Function and integrating it with Azure Storage. By completing this task, you will learn to:

  - Create an Azure Function App: Develop a serverless function using VS Code and deploy it to Azure.
  - Integrate with Azure Storage: Connect the function to a Storage Account container to monitor for new uploads.
  - Trigger and Process Events: Configure the function to automatically trigger when an image is uploaded and extract metadata (name and size).
  - Validate the Solution: Verify that the function executes correctly by uploading an image and checking the logs for the expected output.

## Prerequisites

  - An Azure account with an active subscription. [Create/Login Azure account](https://portal.azure.com/#home)
  - Visual Studio Code. [Download visual studios code](https://code.visualstudio.com/)

## Getting Started With Lab

1. Click on this link to [Login to azure account](https://portal.azure.com/#home) and enter following details.

   **Username** :`madhanmv580@gmail.com`
   
   **Password** : `azurepswd!`

2. Go to the bottom-left corner of your screen and click the **Start** (Windows) button **(1)**. In the search bar, type **Visual Studio Code** **(2)**. When you see **Visual Studio Code** in the search results, click **(3)** it to open the VSCode.

   ![vscode](images/vscode1.png)

3. On the **left sidebar**, click on the **Azure** **(1)** icon (it looks like an "A" or a cloud).
       - If you don't see it, press `Ctrl+Shift+X` to open the **Extensions** tab, search for `Azure Tools`, and install it.
   
4. After clicking the Azure icon, you'll see a panel labeled **Account & Tenants** **(2)** click it and Click on **"Sign in to Azure..."** **(3)** button. Now a pop message will come just click **Allow**.

   ![azure](images/2.png)

5. A browser window will open. Enter **Email** **(1)** and click **Next** **(2)**

   ![azurelogin](images/3.png)

   - Enter Password **(3)** and click on **sign in** **(4)**

   ![select](images/4.png)

7. In Visual Studio Code, press **Ctrl+Shift+P** to open the command palette, Enter **Azure Functions: Create Function...** **(1)** , and select **Create new project** **(2)**.

   ![select](images/6.png)

8. When prompted to select a folder for your project, the **Select Folder** dialog will appear. From the left panel, click on **Desktop** **(3)**. Click the **New folder** **(4)** button at the top.
   
9. A new folder will be created with the default name `New folder`. Rename it to something meaningful, such as `Functionapp` **(5)** and then click the **Select** **(6)** button at the bottom right.

   ![folder](images/7.png)

10. From the "Select a language" dropdown, click on **Python** **(7)**. Now choose your Python interpreter. Click on **python3 3.11.9** **(8)**

   ![folder](images/8.png)
   
   ![folder](images/9.png)

11. Next, select a template for the function. Click on **Blob trigger** **(9)**. 

    ![folder](images/10.png)
    
  - Type Name of the function — for example: **functionblob_trigger1** **(10)**
    
    ![folder](images/11.png)

13. Enter the path your function will monitor in the storage container **images** **(11)** then press Enter.

    ![folder](images/12.png)

14. Select the storage account type. Click on **Use Azure Storage for remote storage** **(12)**.

    ![storage](images/13.png)
    
  - select the storage account form the drop down **funappstorage** **(13)**

    ![stoarges](images/14.png)
    
  - Finally click on **open in current windows** **(14)**
    
    ![curent](images/15.png)

15. In the Azure Portal, use the search bar at the top. Type **storage account** **(1)** From the search results, **click on Storage accounts** **(2)** under the Services section.

    ![azure](images/16.png)

16. From the storage account page select your account **funappstoarge** **(3)** and Go to **Security + networking** **(4)** > click  **Access keys** **(5)** and  Copy the **Connection string** **(6)** under `key1` for use in your application.

    ![key](images/17.png)

17. In **Visual Studio Code**, Open the **local.settings.json** **(7)** file in your Function App project. Paste the copied `connection string` into the **AzureWebJobsStorage** **(8)** field.

    ![csting](images/18.png)
    ![image](images/copy.png)
    
18. Press **Ctrl+Shift+A** to open the Azure extension in Visual Studio Code **Under Account and Tenant**  click the **checkbox** to select the appropriate **subscription** **(1)**. At the top, under the **Resources section** **(2)** (above "Account and Tenant"), **click on Subscription** **(3)** to list all associated resources.

    ![azure](images/19.png)

19. Under your selected Azure Subscription, expand the **Function app** **(4)** section. Right-click on Function App and select **create function app in Azure** **(5)** to begin the setup process.

    ![create](images/20.png)

20. Enter the **function app name** **(6)** as **newfuntrigger**, then select the **region** **(7)**from the drop down as **West us 2**

    ![name](images/21.png)

    ![region](images/22.png)

21. From the **Runtime stack** dropdown, choose **Python 3.11** **(8)** Next , select the **Instance memory size** form the drop down as **2048** **(9)**

    ![stack](images/23.png)

    ![memory](images/24.png)

22. Enter **maximum instance count** as **100** **(10)** and press Enter

    ![created](images/25.png)

23. Under your selected **Subscription** **(1)**, expand the **Function App** **(2)** section. Locate the newly created **Function App newfuntrigger** **(3)**, right-click on it, and select Deploy to **Function App** **(4)**.

    ![deploy](images/26.png)

24. A warning message will appear stating that deploying will overwrite any existing content. Ignore the warning and **click Deploy** **(4)** to proceed.

    ![warning](images/27.png)

25. After deployment is complete, Go to **function_app.py** **(1)** and select the connection variable name **funappstorages_STORAGE** **(2)** and copy.

    ![copyvar](images/var.png)

26. Go to Azure Portal, use the search bar at the top. Type **Function app** **(1)** From the search results, **click on Function app** **(2)** under the Services section.

    ![portal](images/var2.png)

27. Under Function App select the function app recently created **newfuntrigger** **(3)** ,In left-side actions Go to **settings** **(4)** under this click on **Environment Variables** **(5)** Now on top-right click on **+ ADD** **(6)**

    ![env](images/va3.png)

28. In **Add/Edit Application Settings**. Fill the following details and click on **Apply** **(9)**
    
    - Name : `funappstorages_STORAGE` **(7)**
    - Value : `DefaultEndpointsProtocol=https;AccountName=funappstorages;AccountKey=xfnFDMAHlOgTSnVxzs89U
    /kQm/CsgB3NkpimIF3njdJrwPRXU2BdLppR1uM6IS88UW0GQ+wpikEw+AStfWuzCw==;EndpointSuffix=core.windows.net` **(8)**

    ![fill](images/var4.png)
  
29. Click on **Apply** **(10)** and **Confirm** **(11)** Changes.

    ![apply](images/var5.png)

30. After saving changes, Go to **Visual studio code** and press **Ctrl+Shift+A**
    
31. **Navigate to the **Storage Account** **(1)** section and select the Storage Account linked to your Function App **funappstorages** **(2)**. Under the selected Storage Account, expand the **Blob Containers** **(3)** section. Open the **images container** **(4)**, **right-click**, and select** Upload Files** **(5)**.

    ![upload](images/28.png)

32. You will be prompted to select an image file. From the left panel, Navigate to your **Pictures folder** **(6)**, choose the desired **image** **(7)**, and click **Upload** **(8)** to complete the process.

    ![completed](images/29.png)

33. Go to Azure portal and Navigate to **Function app** and Under Function App select the function app recently created **newfuntrigger** **(1)** and click on **overview** **(2)** and  Navigate to **Function** on bottom right and click on **blob_trigger1** **(3)**

    ![img](images/ou.png)

34. Click on **Logs** **(4)**

    ![img](images/ou2.png)
    
    ![img](images/ou3.png)



    





    
