:original_name: das_04_0121.html

.. _das_04_0121:

Scheduled Backup
================

Scenarios
---------

Scheduled backup allows you to back up important database tables and data or SQL result sets so that data can be restored timely in case of a data loss.

Procedure
---------

#. On the top menu bar, choose **Background Tasks** > **Scheduled Backup**.
#. On the task list page, click **Set AK/SK** in the upper left corner.

   .. note::

      **Storage**: The system stores encrypted files in OBS buckets.

      **AK** and **SK**: Access key ID (AK) and secret access key (SK) are required when cloud services are accessed using development tools (APIs, CLI, and SDKs).

#. Select an OBS bucket, enter the AK and SK, and click **Test AK/SK**.
#. After the test succeeded, click **OK**.
#. On the task list page, click **Create DB Backup Task**.
#. Enter a task name, select a task type, and select the database and storage information.
#. Confirm the settings and click **OK**.
#. On the task list page, click **Details** to view the task details.
#. On the task list page, click **Create SQL Result Set Backup Task**.
#. Enter a task name, select a task type, and set the time, backup file format, database, and storage information.
#. Confirm the settings and click **OK**.
#. On the task list page, click **Execution Records** to view the backup status.
#. Click **Details** to view the backup logs.
#. Click **Download** to download the backup file.
#. On the task list page, click **Terminate** or **Pause** to stop or pause a task.
