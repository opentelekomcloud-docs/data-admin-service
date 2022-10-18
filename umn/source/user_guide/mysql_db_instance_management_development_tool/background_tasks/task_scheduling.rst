:original_name: das_04_0120.html

.. _das_04_0120:

Task Scheduling
===============

Scenarios
---------

DAS allows you to execute SQL statements by scheduling tasks. Scheduling types include upon submission, scheduled, and periodic. You can select the scheduling type when creating a task. Error control and transaction control can be performed on SQL statements during scheduling, and task dependency chains can be set for dependent SQL statements.

Procedure
---------

#. On the top menu bar, choose **Background Tasks** > **Task Scheduling**.

   .. note::

      You can create a scheduling task only after agreeing to save the SQL statements in the database.

#. On the **Scheduling Tasks** page, click **Create Task**.

#. On the displayed page, set the task name, scheduling type, and execution time tolerance.

   **Upon submission**: Indicates that a scheduled task is executed immediately after being submitted. The task is executed only once.

   **Scheduled**: Indicates that a task is executed at a scheduled point in time after being submitted. The task is executed only once.

   **Periodic**: Indicates that a task is executed periodically at the specified time after being submitted.

   **Execution Time Tolerance**: Indicates the length of time (in seconds) to wait for a task to be executed before it is no longer scheduled. However, this will not affect the task if it is scheduled again later.

#. Under **Add SQL Statements**, click **Add**. On the displayed page, set parameters as needed and click **Save**. Then, submit the task.

   .. note::

      After a task is executed, it is automatically displayed in the list of finished tasks.

#. In the scheduling task list, view periodic tasks.

   You can search for tasks by status, scheduling type, task ID, or task name.

   -  **Details**: Click it to view the task information.

      View the execution logs and group details under the group list and view the SQL statements on the group details page.

      Click the name of a periodic task to go to the **Task Information** page. Then, click **Schedule Now** to trigger a scheduling immediately. Additionally, view the execution details on the **Scheduling Execution Records** page.

   -  **Execution Records**: Click it to view the task execution details and logs.

   -  **View Logs**: Click it to view log details.

   -  **Terminate**: Click it to stop a scheduled task. A stopped task will be moved to the **Finished Tasks** list.

   -  **Pause**: Click it to pause a task. The task status changes from **Scheduling** to **Paused**. You can also click **Resume** to restore the scheduling.

#. On the **Finished Tasks** page, view tasks that are executed upon submission or at scheduled points in time.

   You can search for tasks by status, scheduling type, task ID, or task name.

   -  **Details**: Click it to view the task information.

      View the execution logs and group details under the group list, and view or modify the SQL statements on the group details page.

   -  **Execution Records**: Click it to view the task execution details, group execution status, SQL statements, and group logs.

   -  **View Logs**: Click it to view log details.

   -  **Delete**: Click it to delete a task from the database.
