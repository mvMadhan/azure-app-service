# AZURE APP SERVICE CREATION

# OVERVIEW

This guide outlines the steps to create an Azure App Service and set up continuous deployment (CI/CD) using GitHub Actions. By integrating GitHub with Azure, you can        automate your application's deployment process, ensuring that updates to your codebase are seamlessly reflected in your live application.

## TASKS

1. Login to azure account
   
2. Click on **search** **(1)** bar.
   
   ![search](images/1.png)

3. Type **app services** **(1)** in the search. Under Services, select **App Services** **(2)**.

   ![select](images/2.png)

4. In the App Services page, click on **Create** **(1)** on top left.

   ![create](images/3.png)

5. Click on **Web App** **(2)**. The Create web app page opens.

   ![click](images/3.1.png)

6. Under **project details** , select **subscription** **(1)** `Innova8 Training` and create or select respective **resource group** **(2)** name `shiva.kumarmv`

   |Label|Name|
   |---|---|
   |Subscription|Innova8 Training|
   |Resource group| shiva.kumarmv|

   ![sub](images/4.png)

7. Under **Instance details**, enter a globally unique name for your web app `booksstore` for the name **(3)** and choose Publish **(4)** `code`, Under Runtime stack select java 17 **(5)** , for java web server stack select apache tomcat 10.1 **(6)**, Under Operating System, select Linux and choose region **(7)** `west us`

   |Label|Name|
   |---|---|
   |Name|booksstore|
   |Publish|code|
   |Runtime stack|java 17|
   |java web server stack|apache tomcat 10.1 |
   |Operating System|code|Linux|
   |region|west us|

   ![detials](images/5.png)

8. Under Pricing Plans, select Create new and type webonline for the name and clikc ok.
   
   |Label|Name|
   |---|---|
   |Linux plan|webonline|

   ![prize](images/6.png)

9. Under Pricing plan, Premium V3 P1V3 (195 minimum ACU/vCPU, 8 GB memory, 2 vCPU), and Click the next - Database (12) button at the bottom of the page.

    |Label|Name|
    |---|---|
    |Pricing plan|Premium V3 P1V3|

    ![selectprz](images/7.png)

10. Under databse leave evrything as default and select the next - Deployment (1) button at the bottom of the page.

    ![next](images/8.png)

11. In Deployment tab , Under Continuous deployment settings, set Continuous deployment to Enable.

    ![git](images/9.png)

12. Under GitHub Actions details, authenticate with your GitHub account, and click chnage account.

    ![git](images/10.png)

13. Configure your github account and click Authorize AzureAppService.

    ![auth](images/11.png)

14. Verfiy your git hub account name , enter github account password and click on confirm.

    ![vrf](images/12.png)

15. Under Github Settings, For Organization, select the organization name `mvMadhan`, For Repository, select the `onlinebookstore` and For Branch, select `master`.

    ![repo](images/13.png)

16. Under Authentication setting , set Basic Authentication to Enable and then select the Review + create **(4)** button at the bottom of the page.

    ![bauth](images/14.png)

17. After validation runs, select the Create (1) button at the bottom of the page

    ![val](images/15.png)

18. After deployment is complete, select Go to resource (1).

    ![go](images/16.png)

19. On the overview page for your App Services, Click on default domain name it will route to browser and If you see the message Your web app is running and waiting for your content, GitHub deployment is still running. Wait a couple of minutes and refresh the page.

    ![result](images/17.png)

    ![output](images/18out.png)

    
    



   

   
