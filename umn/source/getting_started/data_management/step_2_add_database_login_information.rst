:original_name: das_02_0012.html

.. _das_02_0012:

Step 2: Add Database Login Information
======================================

Scenarios
---------

-  With DAS, you can create logins to manage databases using a GUI.
-  This section uses an RDS DB instance as an example to describe how to add a database login.

Adding RDS DB Instance Login Information
----------------------------------------

#. In the navigation pane on the left of the DAS console, choose **Development Tool** to go to the login list page.
#. Click **Add Login**.
#. On the displayed page, select the DB engine, source database, and target DB instance, enter the login username, password, and description (optional), and enable **Collect Metadata Periodically** and **Show Executed SQL Statements**.
#. Test the connection as needed. If a message indicating that the connection failed is displayed, modify the connection according to the failure causes contained in the message.

   .. note::

      -  The username and password required for adding the login are the database username and password.

      -  To delete a password, you can modify or delete the login information.

      -  You are advised to enable **Collect Metadata Periodically**. If it is disabled, DAS obtains only the structured data from databases in real time, and the performance of databases is affected.

         The collection time cannot be customized. Once **Collect Metadata Periodically** is enabled, DAS automatically collects metadata at 20:00 every day (UTC time). If you are not using a UTC time, convert the time according to your local time zone. You can also click **Collect Now** to collect metadata at any time you want.

      -  You are advised to enable **Show Executed SQL Statements**. With it enabled, you can view the executed SQL statements under **SQL Operations** > **SQL History** and execute them again without entering the SQL statements.

#. Click **OK**.
