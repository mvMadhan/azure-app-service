# HTTP-Triggered Email Workflow Using Azure Logic App

## Overview

In this scenario, you will create a Logic App using the Azure Portal that is triggered by an HTTP request. When the Logic App receives the request, it will automatically send an email using a configured email connector such as Outlook or Gmail. This demonstrates how Logic Apps can be used to create simple yet powerful automated workflows that integrate webhooks and communication tools without writing code.

## Prerequisites

  - An Azure account with an active subscription. [Create/Login Azure account](https://portal.azure.com/#home)

## Getting Started With Lab

1. Click on this link to [Login to azure account](https://portal.azure.com/#home)

2. You'll see the **Sign into Microsoft Azure** tab. Here, enter your credentials
   
      - **Email/username:** `madhanmv580@gmail.com`
      
        ![azurelogin](../functionapp/images/3.png)

3. Next, Provide your password

   - **Password:** `azurepswd!`
     
     ![azurelogin](../functionapp/images/4.png)

4. If prompted to stay signed in , click **NO**

5. In the Azure Portal, use the **search bar** at the top. Type **Logic app** (1) From the search results, click on **Logic app** (2) under the Services section.

   ![search](images/1.png)

6. From the **Logic apps** page, click on **+ Add** (1) on top left.

   ![select](images/2.png)

7. Under hosting options , select **Workflow service Plan** **(2)** From Standard and click on **select** **(3)**.

   ![select](images/3.png)

8. Create a new **Logi app** with an Workflow service Plan. Use the folling details.

   |Label|Name|
   |---|---|
   |**Subscription**|Innova8 Training|
   |**Resource group**|shiva.kumarmv|

   ![sub](images/4.png)

9. Under **Instance Details**. Fill the following details.

   |Label|Name|
   |---|---|
   |**Logic app Name**|logicapplatest|
   |**region**|west us 2|
   |**Windows Plan**|logicappwinplan|

   - Click on **OK** **(5)**


   ![name](images/5.png)

10. Leave Zone redundancy as default and click on **Next : Storage** **(6)**

   ![zone](images/6.png)

11. Under storage fill the following details and click on **Review + Create** **(5)**

   - **Storage type** : Azure storage
     
   - Click on **Create new**

     - **Name** : logicappsstoragelatest
    
     - Click on **OK** **(4)**
    
     ![val](images/7.png)

12. After Validation click on **Create**.

    ![img](images/8.png)

13. Once deployment is done, click **Go to Resource**  In the new page.

    ![go](images/9.png)

14. In the Overview of Logic app Click the workflow and select **workflows** **(1)** in the left side bar.

    - Click on **+ Add** **(2)** and select **Add** **(3)**

      ![select](images/10.png)

15. A new workflow will open in right-side and fill the following details.

    - **Workflow Name** : workflownew
      
    - **state type** : stateful
   
    - **click** : create

      ![img](images/11.png)

16. After creating Blank Workflow You should now see an "Add a trigger" (1) option. Click on it.

    ![img](images/trigger.png)
    
18. Click on Add a trigger , a new add trigger will open on right side.

    - Navigate to search bar and search request (1) and click on request app.
   
      ![nav](images/12.png)

19. Click on Plus button **+** **(1)** below the Http Request **Add an action** **(2)** will pops click on it.

    ![req](images/13.png)

20. A new **add an action** will open on right side.

    - Navigate to search bar and search **outlook** (1) and click on **send an email**.

      ![out](images/14.png)

    - Click on **Sign in**
   
      ![sign](images/15.png)

21. Enter username and password or click on already existing account.

    ![img](images/16.png)

22. Enter the following details to send mail and click on **save** **(8)**.

     - **To** : madhanmv580@outlook.com
   
     - **subject** : message from logic app
   
     - **Body** : Hi this is automated message from azure logic app
   
       ![img](images/logic.png)

23. On top left click on **Run** **(9)**.

    ![img](images/18.png)

24. check mail to verify the message.

    ![img](images/logicapp.png)
    





    
    


