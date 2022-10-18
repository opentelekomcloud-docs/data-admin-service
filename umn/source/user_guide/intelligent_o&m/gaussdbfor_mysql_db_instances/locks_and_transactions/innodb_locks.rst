:original_name: das_05_0042.html

.. _das_05_0042:

InnoDB Locks
============

Overview
--------

With this function, the system displays the lock waits generated before the DML operations on the database in real time. With these waits, you can quickly locate the session waits and blocks that happened when multiple sessions update the same piece of data at the same time, and can quickly terminate the source session that holds locks to restore blocked operations.

.. note::

   This feature does not support DDL locks. You view and analyze them on the **Metadata Locks** page.

Procedure
---------

#. Log in to the DAS console using your username and password.
#. On the **Overview** page, click **Go to Intelligent O&M**.
#. Select the required instance and click **Details** to go to the Intelligent O&M overview page.
#. Choose **Locks and Transactions** > **InnoDB Locks** to check whether there are lock waits.
