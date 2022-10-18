:original_name: das_13_0049.html

.. _das_13_0049:

Data Export
===========

Scenarios
---------

DAS supports pagination query to meet your requirements for querying large amounts of data. You can export all the data at a time when backing up or migrating data.

Procedure
---------

#. On the top menu bar, choose **Import and Export** > **Export**.

#. On the displayed page, click **Create Task** and choose **Export Database** or **Export SQL Result** as required. The following takes database export as an example.

   Alternatively, click **Quick Export** and select the target database. On the displayed page, select a storage path and click **OK**.

#. On the displayed page, set parameters as required in areas **Basic Information** and **Advanced Settings**. Then, select the tables to be exported on the right.

   .. note::

      DAS connects to your standby database to export data. This prevents the primary database from being affected by data export. However, if the standby database has a high replication delay, the exported data may not be the latest.

#. After settings are complete, click **OK**.

#. In the task list, view the task ID, type, status, and progress.

#. Click **Details** in the **Operation** column to view task details.
