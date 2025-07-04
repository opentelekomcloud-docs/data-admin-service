:original_name: das_04_0121.html

.. _das_04_0121:

Scheduled Backup (Not Promoted)
===============================

Scheduled backup allows you to periodically back up important database tables and data or SQL result sets so that data can be restored timely in case of data loss.

Configuring the AK/SK
---------------------

Configure AK and SK before you periodically back up database tables or SQL result sets.

#. Log in to the OTC console.
#. Click |image1| in the upper left corner and select a region and project.
#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Background Tasks** > **Scheduled Backup**.
#. On the **Task List** tab, click **Set AK/SK** in the upper left corner.
#. In the displayed dialog box, specify **Storage**, enter an AK and SK, and click **Test AK/SK**. After the test succeeds, click **OK**.

   .. table:: **Table 1** Parameter description

      +-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter | Description                                                                                                                                                                                                                                                                                                          |
      +===========+======================================================================================================================================================================================================================================================================================================================+
      | Storage   | The system stores encrypted files in OBS buckets.                                                                                                                                                                                                                                                                    |
      +-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | AK and SK | **AK** and **SK**: Access key ID (AK) and secret access key (SK) are required credentials for you to access cloud services using development tools like APIs, CLI, and SDKs. The system uses AKs to identify users and SKs to verify encrypted signatures, ensuring that requests are secret, complete, and correct. |
      +-----------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Creating a DB Backup Task
-------------------------

#. Log in to the OTC console.

#. Click |image3| in the upper left corner and select a region and project.

#. Click |image4| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Background Tasks** > **Scheduled Backup**.

#. On the task list page, click **Create DB Backup Task**.

#. Enter a task name, select a task type, backup file format, database, and storage path, and enter remarks.

#. Confirm the settings and click **OK**.

#. View that the status of the current backup task is **Scheduling** in the task list.

   You can also view task details and execution records and terminate or pause the task.

   -  You can click **Details** to view backup logs.
   -  You can click **View Execution Records** to view the backup status.
   -  You can click **Terminate** to end the backup task.
   -  You can click **Pause** suspend the backup task.

   You can also click **Download** to download backup data.

Creating a SQL Result Set Backup Task
-------------------------------------

#. Log in to the OTC console.

#. Click |image5| in the upper left corner and select a region and project.

#. Click |image6| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Background Tasks** > **Scheduled Backup**.

#. On the task list tab, click **Create SQL Result Set Backup Task**.

#. Enter a task name, select a task type, backup file format, database, and storage path, and enter SQL statements to be executed and remarks.

#. Confirm the settings and click **OK**.

#. View that the status of the current backup task is **Scheduling** in the task list.

   You can also view details and execution records and terminate or suspend a scheduling task.

   -  You can click **Details** to view backup logs.
   -  You can click **View Execution Records** to view the backup status.
   -  You can click **Terminate** to end the backup task.
   -  You can click **Pause** suspend the backup task.

   You can also click **Download** to download backup data.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
.. |image3| image:: /_static/images/en-us_image_0000001694653209.png
.. |image4| image:: /_static/images/en-us_image_0000001694653201.png
.. |image5| image:: /_static/images/en-us_image_0000001694653209.png
.. |image6| image:: /_static/images/en-us_image_0000001694653201.png
