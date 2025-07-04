:original_name: das_04_0041.html

.. _das_04_0041:

Exporting Data
==============

DAS allows you to export a large amount of data at a time to facilitate data query or to back up data for migration. This section describes how to export data.

DAS allows you to export an entire database, some data tables, or result sets of SQL statements.

Usage Notes
-----------

-  If you do not select **Generate a file for each table** when exporting data, the exported data file is in **.zip** format. Data files in this format cannot be directly imported. You need to decompress the file before importing it again.
-  If **Generate a file for each table** is selected during data export, the exported data file is in **.sql** or **.csv** format. In this case, the exported data file can be directly imported again.
-  If the :ref:`Exporting a Database <das_04_0041__section1694424814218>` function is used to export over 100,000 MySQL 8.0 instance tables (more than 10,000 in MySQL 5.7 and 5.6), an error message will be displayed indicating that the number of tables is too large and data cannot be exported. In this case, use the :ref:`Exporting SQL Results <das_04_0041__section173457819313>` function instead.
-  Only OBS buckets of the current IAM account can be exported.

Prerequisites
-------------

You have created a user database on the DAS console. For details, see :ref:`Creating a Database <das_08_0014>`.

.. _das_04_0041__section1694424814218:

Exporting a Database
--------------------

#. Log in to the OTC console.
#. Click |image1| in the upper left corner and select a region and project.
#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Import and Export** > **Export**.
#. In the upper left corner of the page, click **Create Task** and choose **Export Database**.
#. In the displayed dialog box, configure basic information and advanced settings as required.

   -  If you select **Export all tables**, data in an entire database or in specific tables will be exported.
   -  Databases are classified into user databases and system databases. System database cannot be exported. If system database data is required, deploy system database services in a user database, so that you can export the system database data from the user database.
   -  DAS connects to your standby database to export data. This prevents the primary database from being affected by data export. However, if the standby database has a high replication delay, the exported data may not be the latest.
   -  DAS does not store any user data. The exported data files are stored in the OBS bucket that you have created. You can specify the storage path. You can click **Bucket ACL Info** in the **Create Task** dialog box to check whether a public OBS bucket is selected.
   -  Creating OBS buckets is free of charge, but saving files will incur certain costs.

#. After settings are complete, click **OK**.
#. In the task list, locate the created task and view the task ID, type, status, and progress.
#. Click **Details** in the **Operation** column to view task details.

.. _das_04_0041__section173457819313:

Exporting SQL Results
---------------------

#. Log in to the OTC console.
#. Click |image3| in the upper left corner and select a region and project.
#. Click |image4| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Import and Export** > **Export**.
#. In the upper left corner of the page, click **Create Task** and choose **Export SQL Result**.
#. In the displayed dialog box, configure basic information and advanced settings as required.

   -  In a SQL result export task, the executed SQL statements cannot exceed 5 MB.
   -  To export multiple SQL result sets at a time, enter SQL statements in the SQL text box. Enter each SQL statement on a separate line and add a semicolon (;) at the end. After the export task is complete, SQL files are generated. One SQL statement corresponds to one file.
   -  DAS does not store any user data. The exported data files are stored in the OBS bucket that you have created.
   -  You can click **Bucket ACL Info** in the **Create Task** dialog box to check whether a public OBS bucket is selected.
   -  Creating OBS buckets is free of charge, but saving files will incur certain costs.

#. After settings are complete, click **OK**.
#. In the task list, locate the created task and view the task ID, type, status, and progress.
#. Click **Details** in the **Operation** column to view task details.

Downloading Data Files
----------------------

Data exported using the data export function is stored in the OBS bucket you created. You can download exported data files in any of the following ways:

-  Download on the DAS Console.
-  Download on the OBS management console.

Quick Export (Not Promoted)
---------------------------

#. Log in to the OTC console.

#. Click |image5| in the upper left corner and select a region and project.

#. Click |image6| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Import and Export** > **Export**.

#. In the upper left corner of the page, click **Quick Export** and select the database that you want to export data from.

   .. note::

      A maximum of 200,000 rows can be quickly exported from a single table. To export more data, choose **Create Task** > **Export Database**.

#. On the **Quick Export** page, select a storage path and click **OK**.

#. In the task list, view the export task you created.

   In the row that contains the export task, you can click **Details** in the **Operation** column to view execution details of the task and information about exported tables.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
.. |image3| image:: /_static/images/en-us_image_0000001694653209.png
.. |image4| image:: /_static/images/en-us_image_0000001694653201.png
.. |image5| image:: /_static/images/en-us_image_0000001694653209.png
.. |image6| image:: /_static/images/en-us_image_0000001694653201.png
