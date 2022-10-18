:original_name: das_04_0071.html

.. _das_04_0071:

InnoDB Lock Query
=================

Scenarios
---------

-  InnoDB lock status management allows you to diagnose conflicts during execution of transactions or sessions with a few clicks. By querying the lock status, you can obtain the lock-holding and lock-wait information of transactions, such as the transaction status, session ID, locked table, and locked data range.
-  InnoDB Lock Query is currently in open beta testing.

Procedure
---------

#. On the top menu bar, choose **Intelligent O&M** > **InnoDB Lock Query**. If there is no transaction waiting for a lock, click **Refresh** to view the latest lock query information.

#. On the displayed page, the lock-holding and lock-wait information is displayed if a transaction is waiting for a lock.

#. Move the cursor above an icon to view its detailed information.

#. Click the lock-holding or lock-wait icon. A dialog box for killing the session is displayed.

   .. note::

      -  The default lock wait timeout is 50s. You can modify the **innodb_lock_wait_timeout** parameter to change the timeout value.
      -  The SQL window execution timeout is 300s.
