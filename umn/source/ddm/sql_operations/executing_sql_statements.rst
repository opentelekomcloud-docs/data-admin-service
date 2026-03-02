:original_name: das_15_0034.html

.. _das_15_0034:

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

#. Select a database from the navigation tree on the left.

#. Enter a SQL statement in the SQL window and click **Execute SQL**.

   -  Enabling **SQL Input Prompt** is recommended. It helps you select the required database, table, or field name when you enter a SQL statement in the SQL window.
   -  You can execute multiple SQL statements at a time. Separate them using semicolons (;). You can click **Full Screen** to view logics in SQL statements clearly.

      -  To execute some of the SQL statements, select the statements before executing them.
      -  To execute all SQL statements, do not select any SQL statements or select all SQL statements.

#. View execution details of the current SQL statement and previously executed SQL statements in the lower part of the page.

#. Click the **Messages** tab, view SQL execution details, including affected rows, progress, and time required.


   .. figure:: /_static/images/en-us_image_0000001694653313.png
      :alt: **Figure 1** Viewing messages

      **Figure 1** Viewing messages

#. On the **Result Set** tab, view SQL execution results. You can perform the following operations on the result sets:

   -  **Copy Row**/**Copy Column**: Copy a row or column for reuse.
   -  **Column Settings**: Customize columns to be displayed when there are a large number of columns in the query result.
   -  **Refresh**: Refresh changed data.
   -  **Row Details**: View the column field name, value, and type of the selected row.
   -  **Export**: The SQL, CSV, and Excel files are supported. No more than 7.84 MB of data with 10,000 records can be exported. The actual size of an Excel file may exceed 7.84 MB due to its format.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
