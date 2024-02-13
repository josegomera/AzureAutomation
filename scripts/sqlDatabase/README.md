## Azure SQL database backup to Blob storage and deletes old backups from blob storage. 

> Original post: https://techcommunity.microsoft.com/t5/azure-database-support-blog/automate-exporting-of-azure-sql-database-as-bacpac-to-blog/ba-p/2409213

> Since the post is obsolete, I updated the login method to use **Manage Identity** instead of **Run as Account**.

The important part is to configure the **Automation Account** to use **System Assign** Manage Identity, then you can create your runbook uploading the script or coping and pasting the code.

- Go to your Automation Account resource.
- Go to Account Settings  > Identity option.
- In the System Assign tab, click on the **Azure Role Assignments** button.
- Click on **Add role assignment**
- Select the scope, subscription, and Role.
    - If you choose Resource Group as scope, select Resource Group where your Automation Account is located.
    - There are a few roles for automation depending on how much permission you want to give access. 
- Click Save

