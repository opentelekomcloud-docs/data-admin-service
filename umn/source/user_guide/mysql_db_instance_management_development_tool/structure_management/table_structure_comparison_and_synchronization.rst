:original_name: das_04_0086.html

.. _das_04_0086:

Table Structure Comparison and Synchronization
==============================================

Scenarios
---------

When you perform a migration or verification, you can check the structure difference by comparing and synchronizing table structures.

Procedure
---------

#. On the top menu bar, choose **Structure Management** > **Table Structure Comparison and Synchronization**.

   Search for tasks by task status and view task details.

#. On the displayed page, click **Create Task** in the upper left corner.

#. On the displayed page, specify the source database, target instance, target database, error tolerance, and synchronization type. Click **Next**.

#. View comparison objects and click **Compare**.

   You can also select the items you want to skip and click **Skip** to cancel the comparison.

#. View the comparison progress. In the comparison item list, click **View Logs** in the **Operation** column to obtain comparison details. You can also click **Download DDL** as needed.

#. Click **Next**. On the **Synchronize** page, view the basic information about this comparison task, such as the source instance, source database, target instance, target database, and synchronization type, and specify the items to be synchronized.

#. Skip synchronization items that may cause high risks and click **Synchronize**.

#. After synchronization is complete, click **View Logs** in the **Operation** column to obtain comparison details. You can download DDL as required.
