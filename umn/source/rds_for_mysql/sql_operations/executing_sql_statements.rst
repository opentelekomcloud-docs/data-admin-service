:original_name: das_04_0047.html

.. _das_04_0047:

Executing SQL Statements
========================

This section describes how to execute various SQL statements.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **SQL Operations** > **SQL Query**.

#. In the upper left corner of the page, select a database from the drop-down list.

#. Enter a SQL statement in the SQL window and click **Execute SQL**.

   -  Enabling **SQL Input Prompt** is recommended. It helps you select the required database, table, or field name when you enter a SQL statement in the SQL window.
   -  To protect query result sets from being displayed as garbled characters, select an encoding format other than the default encoding format, UTF-8.
   -  You can execute multiple SQL statements at a time. Separate them using semicolons (;). You can click **Full Screen** to view logics in SQL statements clearly.

      -  To execute some of the SQL statements, select the statements before executing them.
      -  To execute all SQL statements, do not select any SQL statements or select all SQL statements.

#. View execution details of the current SQL statement and previously executed SQL statements in the lower part of the page.

#. Click the **Messages** tab, view SQL execution details, including affected rows, progress, and time required.

#. On the **Result Set** tab, view SQL execution results.

   You can also perform the operations described in :ref:`Table 1 <das_04_0047__table116726193219>` on result sets.

   .. _das_04_0047__table116726193219:

   .. table:: **Table 1** Operations

      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Function                      | Description                                                                                                                                                                           |
      +===============================+=======================================================================================================================================================================================+
      | Copy Row and Copy Column      | Copies a row or column for reuse.                                                                                                                                                     |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Column Settings               | Customizes the display of columns when there are a number of columns in the query result.                                                                                             |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Convert binary to hexadecimal | Converts binary data in the result set into hexadecimal data for display.                                                                                                             |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Refresh                       | Refreshes changed data.                                                                                                                                                               |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Row Details                   | Displays the column field name, type, and data of the selected row.                                                                                                                   |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Add Row                       | Adds an empty row to the result set.                                                                                                                                                  |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Submit                        | Allows you to view the SQL statements to be modified. After you click **OK**, the result set is updated.                                                                              |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Delete Row                    | Deletes the selected row, including data.                                                                                                                                             |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Export                        | The SQL, CSV, and Excel files are supported. No more than 7.84 MB of data with 10,000 records can be exported. The actual size of an Excel file may exceed 7.84 MB due to its format. |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Export More                   | Redirects you to the data export page and allows you to export over 10,000 rows of data.                                                                                              |
      +-------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

   .. note::

      -  If the result set involves a view, data in the result set cannot be edited.
      -  If the type of the result set is metadata, the data cannot be edited or displayed on multiple pages.
      -  If the result set involves multiple tables, data in the result set cannot be edited.
      -  If only one table is in the result set and does not contain all primary key columns or any primary keys, you cannot edit the data.
      -  Data in virtual tables (for example, tables generated during execution of a stored procedure) cannot be edited.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
