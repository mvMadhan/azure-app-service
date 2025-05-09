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

8. Leave Zone redundancy as default and click on **Next : Storage** **(6)**

   ![zone](images/6.png)

9. Under storage fill the following details and click on **Review + Create** **(5)**

   - **Storage type** : Azure storage
     
   - Click on **Create new**

     - **Name** : logicappsstoragelatest
    
     - Click on **OK** **(4)**
    
     ![val](images/7.png)

10. After Validation click on **Create**.

    ![img](images/7.png)

11. Once deployment is done, click **Go to Resource**  In the new page.

    ![go](images/8.png)

12. In the Overview of Logic app Click the workflow and select **workflows** **(1)** in the left side bar.

    - Click on **+ Add** **(2)** and select **Add** **(3)**

   ![select](images/9.png)

13. A new workflow will open in right-side and fill the following details.

    - **Workflow Name** : workflownew
      
    - **state type** : stateful
   
    - **click** : create

14. d

15. Click on Add a trigge , a new add trigger will open on right side and fill the blanks.

    - Navigate search bar and search request (1) and click on request app.
   
      ![nav](images/12.png)

16. 
    


