:original_name: das_04_0086.html

.. _das_04_0086:

Table Structure Comparison and Synchronization (Not Promoted)
=============================================================

This section describes how to check the structure difference by comparing and synchronizing table structures when you perform a migration or verification.

Prerequisites
-------------

To create a table structure comparison and synchronization task, you need to toggle on **Save SQL** first so that DAS can store your data. If you do not toggle on **Save SQL**, you cannot create table structure comparison and synchronization tasks.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Structure Management** > **Table Structure Comparison and Synchronization**.

#. On the displayed page, click **Create Task**.

#. On the **Create** page, configure required parameters and click **Next**.

   .. table:: **Table 1** Parameter description

      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                              |
      +===================================+==========================================================================================================================================================================================================================================+
      | Source Instance                   | The DB instance that you have logged in to by default.                                                                                                                                                                                   |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Source Database                   | Select a source database.                                                                                                                                                                                                                |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Target Instance                   | Select **Current instance** or **Another instance**.                                                                                                                                                                                     |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Target Database                   | Select a target database to be compared with.                                                                                                                                                                                            |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Error Tolerance                   | Configuring this parameter is recommended.                                                                                                                                                                                               |
      |                                   |                                                                                                                                                                                                                                          |
      |                                   | After this parameter is configured, if a comparison or synchronization error occurs during task execution, the system ignores the error and continues the execution.                                                                     |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Sync Type                         | -  **Global**: synchronizes all tables with the same name from the source database to the target one.                                                                                                                                    |
      |                                   | -  **Specified**: synchronizes specific tables with the same name from the source database to the target one.                                                                                                                            |
      |                                   | -  **One-to-one**: allows you to specify a source table and target table for synchronization. The two tables can have different names.                                                                                                   |
      |                                   | -  **One-to-more**: synchronizes the structure of a table in the source database to multiple tables in the target database. This option is usually selected when you want to change table structures during database and table sharding. |
      +-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **Next** to go to the **Compare** page, check task information and comparison items, and click **Compare**.

   You can also select the items you want to skip and click **Skip** to cancel the comparison.

#. View comparison progress.

   In the comparison item list, click **View Logs** in the **Operation** column to obtain comparison details. You can also click **Download DDL** as needed.

#. After comparison is complete, click **Next**. On the **Synchronize** page, view basic information about this comparison task, such as the source instance, source database, target instance, target database, and synchronization type, and in the synchronization item list, specify the items to be synchronized.

   Skip synchronization items that may cause high risks and then click **Synchronize**.

#. After synchronization is complete, click **View Logs** in the **Operation** column to obtain comparison details.

   You can download DDL as required.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
