:original_name: das_02_0005.html

.. _das_02_0005:

Step 2: Switch to Intelligent O&M
=================================

Procedure
---------

#. In the navigation pane, choose **Intelligent O&M**, on the **Instance Overview** page, click **Synchronize Instances** and then click **Refresh**.

   .. note::

      Instance synchronization is an asynchronous process, which takes several minutes.

#. Locate the instance you want to view and click **Details**.

   .. note::

      This section uses SQL Explorer as an example. For details about how to use each metric, see "Intelligent O&M for RDS for MySQL".

#. On the displayed page, choose **SQL** > **SQL Explorer**.

   .. note::

      -  **Enable DAS SQL Explorer** must be enabled so that the system can collect and analyze full SQL statements.
      -  With **Enable DAS SQL Explorer** enabled, the instance performance loss is within 5%.

#. Click the **SQL Statements** tab.

   .. note::

      -  A maximum of 10,000 data records can be displayed on the **SQL Statements** tab page. To view more records, export the records for view. Columns such as execution duration, elapsed time, scanned rows, and lock wait are also provided. Additionally, SQL statements can be searched by multiple dimensions, including keyword, time range, and number of updated rows.
      -  To view more records, click **Export** to create an export task. Click **Export History** to check whether the export task succeeded.
      -  After the export succeeded, download the file and view the records on the local PC.

#. Click the **SQL Templates** tab.

   .. note::

      -  By default, the SQL statement executions in the last 1 hour are displayed. You can also specify a time range as needed. Columns such as average duration, total duration, total executions, and average scanned rows are provided.

#. Click **Details** in the **Operation** column to view the SQL template details.
#. Click the **SQL Statement Types** tab.
#. Click **Details** in the **Operation** column to view SQL details.
