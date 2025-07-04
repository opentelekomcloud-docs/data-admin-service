:original_name: das_04_0120.html

.. _das_04_0120:

Scheduling Tasks (Not Promoted)
===============================

DAS allows you to execute SQL statements by scheduling tasks. Scheduling types include **immediate**, **scheduled**, and **periodic**. You can select a scheduling type when creating a task. Error control and transaction control can be performed on SQL statements during scheduling, and task dependency chains can be set for dependent SQL statements.

Concurrent tasks cannot be scheduled. To execute concurrent tasks, enable **Event Scheduler** to use the event capability provided by the database. For details, see .

Creating a Scheduling Task
--------------------------

#. Log in to the OTC console.
#. Click |image1| in the upper left corner and select a region and project.
#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Background Tasks** > **Task Scheduling**.

   .. note::

      You can create a scheduling task only after agreeing to save SQL statements in a database.

#. On the **Scheduling Tasks** tab, click **Create Task**.
#. On the displayed page, enter a task name and specify a scheduling type and execution time tolerance.

   .. table:: **Table 1** Parameter description

      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                             |
      +===================================+=========================================================================================================================================+
      | Task Name                         | Task name, which is user-defined.                                                                                                       |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
      | Type                              | The options can be **Immediate**, **Scheduled**, and **Periodic**. You can set a scheduling type as required.                           |
      |                                   |                                                                                                                                         |
      |                                   | -  **Immediate**: indicates that a scheduled task is executed immediately after being submitted. The task is executed only once.        |
      |                                   | -  **Scheduled**: indicates that a task is executed at a scheduled point in time after being submitted. The task is executed only once. |
      |                                   | -  **Periodic**: indicates that a task is executed periodically at the specified time after being submitted.                            |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------+
      | Execution Time Tolerance (s)      | Refers to how many seconds the system keep executing this task after the expected execution time comes.                                 |
      |                                   |                                                                                                                                         |
      |                                   | The default value is **3600**. The value ranges from **1** to **86,400**.                                                               |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------+

#. Under **SQL Statements**, click **Add**. On the displayed page, set parameters as needed and click **Save**.

   .. table:: **Table 2** Parameter description

      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                   |
      +===================================+===============================================================================================================================================================================================================================================================+
      | Group Name                        | Group name, which is user-defined.                                                                                                                                                                                                                            |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Instance                          | Target instance name.                                                                                                                                                                                                                                         |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Database                          | Associated database.                                                                                                                                                                                                                                          |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | SQL Statements                    | You can manually input SQL statements or import existing SQL files.                                                                                                                                                                                           |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Skip Errors                       | Configuring this parameter is recommended.                                                                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                                               |
      |                                   | After this parameter is configured, the system will skip any errors detected when SQL statements in the SQL group are being executed. If this function is disabled, the system will stop executing SQL statements.                                            |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Enable Transactions               | Configuring this parameter is recommended.                                                                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                                               |
      |                                   | After this parameter is configured, SQL statements in the current SQL group will be executed as a transaction, and if a DML error occurs, a rollback will be performed. If this function is disabled, each SQL statement in the group is executed separately. |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Dependent SQL Group               | The system executes all SQL statements in the dependent SQL group first and then those statements in the current group.                                                                                                                                       |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Allow Concurrent Execution        | Configuring this parameter is recommended.                                                                                                                                                                                                                    |
      |                                   |                                                                                                                                                                                                                                                               |
      |                                   | After this parameter is configured, the system will concurrently execute SQL statements in the current SQL group and other SQL groups, except for dependent SQL groups.                                                                                       |
      |                                   |                                                                                                                                                                                                                                                               |
      |                                   | .. caution::                                                                                                                                                                                                                                                  |
      |                                   |                                                                                                                                                                                                                                                               |
      |                                   |    CAUTION:                                                                                                                                                                                                                                                   |
      |                                   |    SQL statements in the current SQL group are executed still in serial mode.                                                                                                                                                                                 |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **Submit** at the bottom of the **Create Task** tab.

Managing Scheduling Tasks
-------------------------

Tasks are displayed on the **Scheduling Tasks** and **Finished Tasks** tab pages by status.

-  **Scheduling Tasks**: The scheduling tasks are periodic tasks that are being scheduled or paused.

   On the **Task Scheduling** page, click the **Scheduling Tasks** tab.

   You can search for tasks by status, scheduling type, task ID, or task name.

   You can also perform the following operations on scheduling tasks:

   -  **View Details**: Click it to view the task information.

      Click the name of a scheduling task to go to the **Task Info** page and click **Manually Execute** to trigger a scheduling immediately. After the task is successfully executed, view execution details on the **Scheduling Execution Records** page.

      In the **SQL Groups** area, click **View Details**. On the displayed page, view, modify, copy, and delete SQL statements.

   -  **View Execution Records**: Click it to view the task execution details and logs.

   -  **View Log**: Click it to view log details.

   -  **Terminate**: Click it to stop a scheduled task. A stopped task will be moved to the **Finished Tasks** list.

   -  **Pause**: Click it to pause a task. The task status changes from **Scheduling** to **Pause**. You can also click **Resume** to restore the scheduling.

-  **Finished Tasks**: Tasks in the **Finished Tasks** list are periodic tasks that have been terminated or immediate and scheduled tasks that have completed.

   On the **Task Scheduling** page, click the **Finished Tasks** tab.

   You can search for tasks by status, scheduling type, task ID, or task name.

   You can also perform the following operations on scheduling tasks:

   -  **View Details**: Click it to view the task information.

      Click the name of a finished task that is periodically scheduled or starts immediately. On the displayed page, click **Manually Execute**. After the task is successfully executed, view execution details on the **Scheduling Execution Records** page.

      In the **SQL Groups** area, click **View Details**. On the displayed page, view, modify, copy, and delete SQL statements.

   -  **View Execution Records**: Click it to view the task execution details, group execution status, SQL statements, and group logs.

   -  **View Log**: Click it to view log details.

   -  **Delete**: Click it to delete a task from the database.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
