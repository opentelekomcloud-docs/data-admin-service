:original_name: das_03_0100.html

.. _das_03_0100:

Logging In to Databases Shared by Others
========================================

Scenarios
---------

You have a database instance and want to share it with another account or another user of the same account, but you do not want this other account or user to know the password of the shared login, or view your database instances besides the shared one.

Prerequisites
-------------

-  There are two accounts, or one account and two IAM users.
-  You have obtained the UID (user ID) of the IAM user.
-  You have logged in to the DAS console.

Usage Restrictions
------------------

-  Users having shared database logins cannot add databases or users.
-  Shared databases do not have the data tracking, rollback, and background task features.

Procedure
---------

#. Log in to the DAS console using the username and password of an IAM user.
#. On the overview page, click **Go to Development Tool**.
#. In the right pane, click the **Database Logins Shared by Others** tab.
#. Click **View My User ID**. On the displayed page, copy the UID.
#. Log in to the DAS console using the username and password of the account.
#. On the overview page, click **Go to Development Tool**.
#. On the **My Database Logins** tab, locate the login you want to share and click the number in the **Additional Users** column.
#. On the displayed **View Additional Users** page, click **Add User**.
#. On the displayed **Add User** page, select the adding method.

   -  **Manual input**: Enter the UID of user to whom you want to share your database login. If multiple users need to be added, separate their UIDs with semicolons (;).
   -  **Synchronize IAM account**: Select another IAM user of the current account.
   -  **Synchronize EPS user**: Select the target users from the group of the enterprise project.

#. Confirm the settings and click **OK**.
#. Return to the DAS console and check whether the users are successfully added.
#. Click **Log In** to log in to the shared database.
