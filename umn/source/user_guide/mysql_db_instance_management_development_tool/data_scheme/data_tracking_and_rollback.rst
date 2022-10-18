:original_name: das_04_0082.html

.. _das_04_0082:

Data Tracking and Rollback
==========================

Scenarios
---------

-  Audit core data changes, collect change statistics, and view sensitive information. For example, you can use this function to query bank statements, statistics on new orders, and key configuration changes.
-  Roll back the misoperation to the state before it is operated. For example, you can use the rollback function when the WHERE condition is not added during DBA configuration update, configuration data is deleted by mistake, or a large amount of dirty data and ripple effects are generated due to program bugs.

Procedure
---------

#. On the top menu bar, choose **Data Scheme** > **Data Tracking and Rollback**.

   -  Search for tasks by time range or database name.
   -  You can delete tasks as required by selecting check boxes next to task IDs. The deletion operation is synchronized to DAS.
   -  In the task list, click the task ID to view task details.
   -  In the task list, locate the target task and click **View Task** in the **Operation** column. Then, you can view task details under **Task Information**, **Log Search**, and **Rollback Task List**.

   .. note::

      A created task will expire in 15 days. Once the task expires, the system automatically retrieves and deletes the changes in DAS.

#. On the displayed page, click **Create Tracking Task**. In the displayed dialog box, specify task details, including the task name, time range, and database name.

   .. note::

      -  Users who create the tracking task for the first time need to agree to the agreement.
      -  Task tracking and rollback take three hours by default.

#. Click **Precheck** to obtain the operation details at a specific point in time.

   .. note::

      -  During the pre-check, binlog files are displayed based on time range. RDS DB instances with the backup function enabled periodically back up the binlog file to the OBS bucket. The backup delay is no more than five minutes.
      -  When you create a tracking task, there may be no changes in the latest five minutes. In this case, you can create a task again later.

#. Click **Read Logs** to obtain log details.

   When reading logs, the system initiates binlog parsing and stores log changes for filtering and displaying data.

   .. note::

      -  You can search for logs only after all logs are successfully read.
      -  If a new task is started before the last tracking task is completely read, it is normal that the log start time is later than the end time.

#. Click **Log Search** to obtain details about the event changes.

#. Create a rollback task if you need to roll back multiple events. Specifically, click **Create Rollback Task** on the **Log Search** tab page. In the displayed dialog box, specify event IDs and storage of rollback statements, set advanced settings as required, and click **OK**.

   .. note::

      -  The start and end event IDs are the ones in the task list and must be entered in ascending order.

      -  Combing changes

         Changing a record (primary key) three consecutive times (for example, 1->2->3->4) equals the change of 1 to 4 (1->4).

      -  Statement Type

         **Generate event rollback SQL statements**: generates SQL statements with reverse changes based on the images before and after data change.

         **Obtain the original data before changes**: generates rollback tables and insert statements by mirroring before data change.

#. In the rollback task list, view the current rollback task information or create a rollback task.

   -  Locate the target rollback task and click **View Details** in the **Operation** column to view task details.
   -  In the **Operation** column, click **Download** to download the compressed data package of the task.

      .. note::

         Changes (such as insert->delete, delete->insert, update->update) on the same record will be combined or canceled. Therefore, the generated file may have no rollback SQL statements or original data.
