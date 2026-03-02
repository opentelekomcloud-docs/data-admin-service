:original_name: das_04_0069.html

.. _das_04_0069:

Maintaining a Table
===================

While working with MySQL databases, you do a lot of changes such as data insert, update, and deletion, which may cause table fragmentation. As a result, the database server performance is deteriorated. To handle this, periodic maintenance is required.

Functions
---------

.. table:: **Table 1** Function description

   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Function                          | Description                                                                                                                                                                                                              |
   +===================================+==========================================================================================================================================================================================================================+
   | Check                             | Allows you to check whether there are errors in database tables using the CHECK TABLE statement. You can check a table with any of the following methods: **Check**, **Quick**, **Fast**, **Changed**, and **Extended**. |
   |                                   |                                                                                                                                                                                                                          |
   |                                   | The CHECK TABLE statement adds a read-only lock to the table.                                                                                                                                                            |
   |                                   |                                                                                                                                                                                                                          |
   |                                   | -  **Check**: scans rows to verify that deleted links are valid. Alternatively, calculate a key checksum for the rows and verifies the validity using the obtained checksum.                                             |
   |                                   | -  **Quick**: checks only tables that have not been closed properly.                                                                                                                                                     |
   |                                   | -  **Fast**: neither scans rows nor checks for incorrect links.                                                                                                                                                          |
   |                                   | -  **Changed**: checks only the tables that have been changed since the last check and the tables that have not been closed properly.                                                                                    |
   |                                   | -  **Extended**: searches for keywords in each row. This ensures that the table is 100% consistent, but takes a long time.                                                                                               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Repair                            | Allows you to use the REPAIR TABLE statement to repair possibly corrupted or incorrect tables. You can repair tables using any of the following three methods: **Check**, **Quick**, and **Extended**.                   |
   |                                   |                                                                                                                                                                                                                          |
   |                                   | -  **Check**: a simple repair, which repairs data and index files.                                                                                                                                                       |
   |                                   | -  **Quick**: the quickest repair, which repairs only index files, but not data files.                                                                                                                                   |
   |                                   | -  **Extended**: the slowest repair, which creates indexes row by row to repair data and index files.                                                                                                                    |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Checking a Table
----------------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Database Management**.

#. Click **Change** on the right of the current database to switch to the database where you want to create a table.

#. On the displayed **Objects** tab, choose **Tables** on the left.

#. Locate the table you want to check and choose **More** > **Maintain** > **Check** in the **Operation** column.

#. Select a check method as required.

   You can check a table with any of the following methods: **Check**, **Quick**, **Fast**, **Changed**, and **Extended**.

#. In the displayed dialog box, click **Yes**.

Repairing a Table
-----------------

#. Log in to the OTC console.

#. Click |image3| in the upper left corner and select a region and project.

#. Click |image4| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Database Management**.

#. Click **Change** on the right of the current database to switch to the database where you want to maintain a table.

#. On the displayed **Objects** tab, choose **Tables** on the left.

#. Locate the table you want to repair and choose **More** > **Maintain** > **Repair** in the **Operation** column.

#. Select a repair method as required.

   You can repair tables using any of the following three methods: **Check**, **Quick**, and **Extended**.

#. In the displayed dialog box, click **Yes**.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
.. |image3| image:: /_static/images/en-us_image_0000001694653209.png
.. |image4| image:: /_static/images/en-us_image_0000001694653201.png
