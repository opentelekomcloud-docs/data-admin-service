:original_name: das_16_0029.html

.. _das_16_0029:

SQL Window
==========

Procedure
---------

#. Log in to the GaussDB(for openGauss) management homepage.
#. On the top menu bar, choose **SQL Operations** > **SQL Window**.
#. Check whether there are any schemas other than system schemas exist.
#. If not, create a schema according to :ref:`Creating a Schema <das_19_0015>` and then perform SQL operations.

   .. note::

      After a database is created, you need to create a schema before performing any SQL operations.

#. In the navigation pane, select a database, and then specify a table or view.

   -  **Execute SQL**: executes SQL statements.

   -  **Execute SQL Plan**: reports the execution of SQL statements to facilitate troubleshooting and optimize SQL processing performance.

   -  **SQL Favorites**: allows you to add, view, and manage frequently used SQL statements.

   -  **Format SQL**: improves the readability of SQL statements. Formatting SQL statements enables statements to be displayed in line break mode, but does not change their logic and semantics.

      The formatting takes effect for all the SQL statements in the SQL window. You cannot format only the selected statements.

   -  **SQL Input Prompt**: helps you to select your desired database, table, or field name as prompted to quickly enter statements in the SQL window.

   -  Overwrite/Append Mode:

      -  **Append Mode:** Each time a SQL statement is executed, the new result set is appended to the previous one.
      -  **Overwrite Mode**: Each time a SQL statement is executed, the new result set overwrites the previous one.

   -  **Full Screen**: shows SQL statements on a full screen.

#. After SQL statements are executed, view SQL execution status on the **Executed SQL Statements**, **Messages**, and **Result Set** tab pages.
