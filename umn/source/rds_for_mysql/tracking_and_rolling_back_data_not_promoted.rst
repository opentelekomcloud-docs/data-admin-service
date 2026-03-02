:original_name: das_04_0082.html

.. _das_04_0082:

Tracking and Rolling Back Data (Not Promoted)
=============================================

The data tracking and rollback function helps you track and roll back data changes. This section describes how to track and roll back data changes.

This function can be used to:

-  Audit core data changes, collect change statistics, and view sensitive information. For example, you can use this function to query bank statements, statistics on new orders, and key change history of a configuration table.
-  Roll back data misoperations, recover the data deleted by mistake, and restore changed data to the original status.

Prerequisites
-------------

-  You have enabled the data tracing and rollback function.
-  The binlog function has been enabled for the destination database.

Data Tracking
-------------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Data Scheme** > **Data Tracking and Rollback**.

   -  Search for a task by time range or database name.
   -  In the task list, locate the task and click its ID to view details.
   -  In the task list, click **View Task** in the **Operation** column. Then, you can view task information, search logs, and rollback tasks.
   -  If a task is not required any longer, you can select it and click delete in the upper lefter corner. Change history of the task will be deleted from the DAS storage.

   .. note::

      The default validity period of a data tracking task is 15 days. Once a task expires, the system automatically retrieves and deletes the changes in DAS.

#. On the displayed page, click **Create Tracking Task**.

#. In the displayed dialog box, configure required parameters.

   .. table:: **Table 1** Parameters for creating a tracking task

      +-----------------------------------+----------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                            |
      +===================================+========================================================================================+
      | Task Name                         | Task name, which is user-defined.                                                      |
      +-----------------------------------+----------------------------------------------------------------------------------------+
      | Time Range                        | Time range for data tracking. You are advised to select a time span less than 3 hours. |
      +-----------------------------------+----------------------------------------------------------------------------------------+
      | Database Name                     | Database whose data is to be tracked.                                                  |
      +-----------------------------------+----------------------------------------------------------------------------------------+
      | Table Name                        | Select a table to be searched. Multiple tables can be added.                           |
      +-----------------------------------+----------------------------------------------------------------------------------------+
      | Data Tracking Type                | You can select multiple tracking operations.                                           |
      |                                   |                                                                                        |
      |                                   | The following four options are supported:                                              |
      |                                   |                                                                                        |
      |                                   | -  **Update**                                                                          |
      |                                   | -  **Insert**                                                                          |
      |                                   | -  **Delete**                                                                          |
      |                                   | -  **DDL**                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------+

   .. note::

      Users who create a tracking task for the first time need to view and agree to the data security agreement.

#. Click **Precheck** to search for binlog files based on the selected time range.

   -  RDS instances with the backup function enabled periodically back up binlog files and store them to your OBS bucket. The backup delay is no more than five minutes.
   -  When you create a tracking task, there may be no changes in the latest five minutes. In this case, you can create a task again later.

#. After the precheck is successful, click **Read Logs** to obtain log details.

   When reading logs, the system initiates binlog parsing and stores log changes for filtering and displaying data.

   .. note::

      -  You can search for logs only after all logs are successfully read.
      -  If a new task is started before the last tracking task is completely read, it is normal that the log start time is later than the end time.

#. .. _das_04_0082__li1134813419527:

   After the logs are read, click **Log Search** to obtain details about change events.

   -  On the **Log Search** page, you can view information about the change events, such as event IDs, change time, change types, table names, impacted rows, and descriptions.
   -  You can also view data or rollback statements in the **Operation** column.

Rolling Back Data
-----------------

#. Log in to the OTC console.
#. Click |image3| in the upper left corner and select a region and project.
#. Click |image4| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Data Scheme** > **Data Tracking and Rollback**.
#. Locate the task you want to view and click **View Task** in the **Operation** column.
#. On the **Log Search** page, click **Create Rollback Task**. Alternatively, on the **Rollback Task List** page, click **Create Rollback Task**.
#. In the displayed dialog box, configure required parameters.

   .. table:: **Table 2** Parameters for creating a rollback task

      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                            |
      +===================================+========================================================================================================================================================================================================================================+
      | Start Event ID                    | The start event ID is the one in the task list and must be entered in ascending order. You can view the event ID by referring to :ref:`11 <das_04_0082__li1134813419527>`.                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | End Event ID                      | The end event ID is the one in the task list and must be entered in ascending order. You can view the event ID by referring to :ref:`11 <das_04_0082__li1134813419527>`.                                                               |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Rollback Statement Storage        | Enter an OBS bucket.                                                                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                        |
      |                                   | To keep your data secure, DAS stores rollback statements in the OBS bucket you provide. In this way, DAS automatically connects to your OBS bucket for in-memory reading. Your data will never be flushed to any storage media of DAS. |
      |                                   |                                                                                                                                                                                                                                        |
      |                                   | Creating OBS buckets is free of charge, but saving files will incur certain costs.                                                                                                                                                     |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Charset                           | Specify a character set.                                                                                                                                                                                                               |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Statement Type                    | -  **Generate event rollback SQL statements**: generates SQL statements for rolling back reverse changes based on the images before and after data change.                                                                             |
      |                                   | -  **Obtain the original data before changes**: generates rollback tables and insert statements by mirroring before data change.                                                                                                       |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Advanced Settings                 | You can also set **Data Tracking Type**, **Table Name**, **Field**, and **Field Content** under **Advanced Settings** as required.                                                                                                     |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   .. note::

      Changing a record (primary key) three consecutive times (for example, 1->2->3->4) equals the change of 1 to 4 (1->4).

#. Click **OK**.
#. In the rollback task list, view the created rollback task.

   -  Locate the rollback task you created and click **View Detail** in the **Operation** column.
   -  Click **Download** in the **Operation** column to download the original data before data change and event-based rollback SQL statements to your local PC.
   -  Enter a task ID in the search box in the upper right corner of the task list to search for the required task.
   -  In the **Operation** column, sort out tasks by task ID, start event ID, end event ID, file size, and status.

      .. note::

         Changes (such as insert->delete, delete->insert, update->update) on the same record will be combined or canceled. So, the generated file may have no rollback SQL statements or original data.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
.. |image3| image:: /_static/images/en-us_image_0000001694653209.png
.. |image4| image:: /_static/images/en-us_image_0000001694653201.png
