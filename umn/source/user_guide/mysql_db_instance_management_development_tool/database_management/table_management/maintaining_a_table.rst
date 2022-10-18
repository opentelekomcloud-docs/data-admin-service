:original_name: das_04_0069.html

.. _das_04_0069:

Maintaining a Table
===================

Scenarios
---------

While working with MySQL databases, you do a lot of changes such as data insert, update, and deletion, which may cause table fragmentation. As a result, the database server performance is deteriorated. To handle this, periodic maintenance is required.

Functions
---------

-  Check

   The CHECK TABLE statement adds a read-only lock to the table.

   Allows you to check whether there are errors in database tables using the CHECK TABLE statement. You can check a table with any of the following methods:

   -  **Check**: Scan rows to verify that deleted links are valid. Alternatively, calculate a key checksum for the rows and verifies the validity using the obtained checksum.
   -  **Fast**: Check only tables that have not been closed properly.
   -  **Quick**: Do not scan rows or check for incorrect links.
   -  **Changed**: Check only tables that have been changed since the last check or tables that have not been closed properly.
   -  **Extended**: Search for keywords in each row. This ensures that the table is 100% consistent, but takes a long time.

-  Repair

   Allows you to use the REPAIR TABLE statement to repair possibly corrupted or incorrect tables. You can repair tables using any of the following three methods:

   -  **Check**: a simple repair, which repairs data and index files.
   -  **Quick**: the quickest repair, which repairs only index files, but not data files.
   -  **Extended**: the slowest repair, which creates indexes row by row to repair data and index files.

Procedure
---------

The following uses the **Check** operation as an example to explain how to maintain tables.

#. On the top menu bar, choose **Database Management**.
#. On the displayed **Objects** page, select **Tables**, locate the target table, and choose **More** > **Maintain** > **Check** in the **Operation** column.
#. In the displayed dialog box, click **Yes**.
