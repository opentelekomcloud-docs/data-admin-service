:original_name: das_04_0047.html

.. _das_04_0047:

Executing SQL Statements
========================

Procedure
---------

#. On the top menu bar, choose **SQL Operations** > **SQL Window**. In the SQL window, select a database from the navigation pane.
#. Enter SQL statements in the SQL window and click **Execute SQL**.

   -  Enabling **SQL Input Prompt** is recommended\ **.** It helps you to select your desired database, table, or field name as prompted to quickly enter statements in the SQL window.
   -  To protect query result sets from being displayed as garbled characters caused by UTF-8, the default encoding format, select an encoding format as needed.
   -  To execute multiple SQL statements at a time, separate them using semicolons (;). In this case, click **Full Screen** to view the logics in SQL statements clearly.

      -  To execute some of the SQL statements, select the statements before executing them.
      -  To execute all the SQL statements, do not select any SQL statements or select all of them.

#. View the SQL execution details on **Executed SQL Statements** and **Messages** tab pages, including the SQL execution history, execution status, impact scope, execution progress, and elapsed time.
#. On the **Result Sets** tab, view the execution details. You can perform the following operations on the result sets:

   -  **Copy Row**/**Copy Column**: copies a row or column for reuse.
   -  **Column Settings**: customizes the columns to display when there are a large number of columns in the query result.
   -  **Binary to Hexadecimal**: converts the binary data in the result set into hexadecimal data for display.
   -  **Refresh**: refreshes the changed data.
   -  **Row Details**: displays the column field name, value, and type of the selected row.
   -  **Add**: adds an empty row to the result set.
   -  **Submit**: views the SQL statements to be modified. After you click **OK**, the result set is updated to the latest.
   -  **Delete Row**: deletes the selected row, including the data.
   -  **Export**: allows you to export the data in a SQL or CSV file. A maximum of 10,000 rows of data can be exported.
   -  **Export More**: redirects you to the data export page and allows you to export over 10,000 rows of data.

      .. note::

         -  If the result set involves a view, you cannot edit the data.
         -  If the type of the result set is metadata, the data cannot be edited or displayed on multiple pages.
         -  If the result set involves multiple tables, you cannot edit the data.
         -  If the result set involves only one table and does not include all the primary key columns of the table or no primary key is found, you cannot edit the data.
         -  Virtual tables (for example, tables generated during SQL execution) cannot be edited.
