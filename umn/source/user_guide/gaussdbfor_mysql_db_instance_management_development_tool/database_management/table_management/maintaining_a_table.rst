:original_name: das_13_0015.html

.. _das_13_0015:

Maintaining a Table
===================

Scenarios
---------

While working with a database, you do a lot of changes to tables such as inserting, updating and deleting data. This occupies disk space and deteriorates database performance. To handle this, periodic maintenance is required.

Functions
---------

-  Optimize

   Allows you to optimize tables using the OPTIMIZE TABLE statement and sort out fragmented files for later use.

   During the optimization, a read-only lock will be added to target tables. Therefore, optimizing tables during off-peak hours is recommended.

-  Check

   Allows you to check whether there are errors in database tables using the CHECK TABLE statement. You can check a table with any of the following methods:

   -  **Check**: Scan rows to verify that deleted links are valid. Alternatively, calculate a key checksum for the rows and verifies the validity using the obtained checksum.

   -  **Quick**: Do not scan rows or check for incorrect links.

   -  **Fast**: Check only tables that have not been closed properly.

   -  **Changed**: Check only tables that have been changed since the last check or tables that have not been closed properly.

   -  **Extended**: Search for keywords in each row.

      The CHECK TABLE statement adds a read-only lock to the table.

-  Repair

   Allows you to use the REPAIR TABLE statement to repair possibly corrupted or incorrect tables. You can repair tables using any of the following three methods:

   -  **Repair**: a simple repair, which repairs data and index files.
   -  **Quick**: the quickest repair, which repairs only index files, but not data files.
   -  **Extended**: the slowest repair, which creates indexes row by row to repair data and index files.

-  Analyze

   Allows you to use the ANALYZE TABLE statement to analyze tables. During the analysis, read-only locks are added to tables. Tables can only be read during the analysis.

   .. note::

      Temporary files will be generated during table optimization. These files may occupy twice the disk space of the current table data.

Procedure
---------

The following uses the **Check** operation as an example to explain how to maintain tables.

#. On the top menu bar, choose **Database Management**.
#. On the displayed **Objects** page, select **Tables**, locate the target table, and choose **More** > **Maintain** > **Optimize** in the **Operation** column.
#. In the displayed dialog box, click **Yes**.
