:original_name: das_18_0035.html

.. _das_18_0035:

Instance Performance
====================

Procedure
---------

#. Log in to the GaussDB(for openGauss) console.
#. Apply for Intelligent O&M according to :ref:`Intelligent O&M <das_18_0097>`.
#. Locate your desired instance and click **Details** to go to the Intelligent O&M overview page.
#. Choose **Performance** > **Instance Performance**.
#. Click **Select Metric** and select the instance metrics to display.

   .. table:: **Table 1** Instance metrics

      +-----------------+-------------------------------------+--------------------------------------------------------------------------+
      | Category        | Metric                              | Description                                                              |
      +=================+=====================================+==========================================================================+
      | Disk Usage      | Instance Disk Used Space            | Real-time used space of data disks on the monitored instance (Unit: GB)  |
      +-----------------+-------------------------------------+--------------------------------------------------------------------------+
      |                 | Instance Disk Total Space           | Real-time total space of data disks on the monitored instance (Unit: GB) |
      +-----------------+-------------------------------------+--------------------------------------------------------------------------+
      |                 | Instance Disk Usage                 | Real-time data disk usage on the monitored instance (Unit: %)            |
      +-----------------+-------------------------------------+--------------------------------------------------------------------------+
      | Load            | Deadlocks                           | Incremental number of database transaction deadlocks (Unit: count)       |
      +-----------------+-------------------------------------+--------------------------------------------------------------------------+
      |                 | Response Time of 80% SQL Statements | Real-time response time of 80% of database SQL statements (Unit: μs)     |
      +-----------------+-------------------------------------+--------------------------------------------------------------------------+
      |                 | Response Time of 95% SQL Statements | Real-time response time of 95% of database SQL statements (Unit: μs)     |
      +-----------------+-------------------------------------+--------------------------------------------------------------------------+
      | Kernel Resource | Buffer Hit Rate                     | Buffer hit rate of the database (Unit: %)                                |
      +-----------------+-------------------------------------+--------------------------------------------------------------------------+

#. Click **OK**.
#. Click **Detail** to the upper right corner of each graph to view the metric details. You can also view the metric details in the last 1 hour, 12 hours, 1 day, 2 days, 7 days, or customize a time range.
#. Click the **Performance Trends Comparisons** tab, select the desired metrics, and click **OK**.
#. Click **Detail** to the upper right corner of each graph to view the metric details. You can also view the metric details in a specified time range within the past week.
#. Enable **Interactive Graph** to view the performance of other metrics at the same time.
#. Click **Full Screen** for a clear view.
