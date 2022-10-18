:original_name: das_03_0017.html

.. _das_03_0017:

Slow Query Logs
===============

Procedure
---------

#. Log in to the DAS console using your username and password.
#. On the **Overview** page, click **Go to Intelligent O&M**.
#. Locate your desired instance and click **Details** to go to the Intelligent O&M overview page.
#. On the **SQL** tab page, click **Slow Query Logs** to view the slow SQL trend of the current instance.
#. Set your desired time range or select **Last 1 hour**, **Last 6 hours**, or **Last 1 day** to view the corresponding slow query logs, CPU usage, and archived slow query logs.
#. Click **Enable DAS Slow Query Log**. In the displayed dialog box, read and agree to the security agreement, and click **OK**.
#. On the lower part of the **Log Trends** tab page, view the statistics and details of slow query logs.

   -  Query and view slow query logs by database name.
   -  Click **Export Slow Query Log** to export the slow query logs.
   -  Click **Export History** to view the export history of slow query logs.

#. On the **Log Archiving** tab page, obtain the slow query log files of the current DB instance in either of the following ways: (The archiving function saves slow query log files generated in the last 10 days.)

   -  Click **Generate Latest Log File**.
   -  DAS automatically generates a slow query log every time the log data reaches 50 MB.

#. In the slow query log list, click **Download** to download and view log data.
