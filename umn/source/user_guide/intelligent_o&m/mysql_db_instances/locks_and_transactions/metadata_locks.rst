:original_name: das_03_0043.html

.. _das_03_0043:

Metadata Locks
==============

Overview
--------

-  Metadata locks (MDLs) are used to ensure consistency between DDL and DML operations. Usually, DDL operations require MDL write locks. Once a DML lock occurs, it can have a significant impact on the database because all subsequent operations (SELECT, DML, and DDL operations) on the table will be blocked, causing a backlog of connections.
-  The system displays the database MDL locks in real time. With these locks, you can quickly locate MDL problems and terminate the sessions holding MDL locks, so that blocked operations can be restored.

   .. note::

      -  This feature does not support DML locks. You can view and analyze them on the **InnoDB Locks** page.
      -  Currently, this feature is available for only MySQL 5.6 and 5.7.
      -  A maximum of 1,000 records can be displayed.
      -  GaussDB(for MySQL) DB instances are currently not supported.

Procedure
---------

#. Log in to the DAS console using your username and password.
#. On the **Overview** page, click **Go to Intelligent O&M**.
#. Locate your desired instance and click **Details** to go to the Intelligent O&M overview page.
#. Choose **Locks and Transactions** > **Metadata Locks**.
#. Select a lock status and type, and enter a database name, table name, and session ID as needed. Then, click **Query** to query required sessions.
#. In the query result, check whether there are sessions that hold MDL locks. If so, select the sessions as required and click **Kill Session**.
