:original_name: das_04_0074.html

.. _das_04_0074:

Tuning SQL Statements
=====================

Scenarios
---------

SQL tuning helps you identify the SQL statements that are executed frequently or slowly, and consume large volumes of resources. You can optimize the database according to the diagnosis suggestions to ensure database stability.

Prerequisites
-------------

There is at least one SQL statement or character in the SQL window.

Procedure
---------

#. On the top menu bar, choose **SQL Operations** > **SQL Window**. In the SQL window, click **Tune SQL**.

#. View the tuning result on the displayed **SQL Tuning** page, which is opened after the system automatically tunes the SQL statements.

#. Click **View Details** to view diagnosis information.

#. On the **SQL Tuning** page, click **Add SQL Performance Tuning** to add a SQL tuning task.

#. On the displayed page, enter the SQL statements or upload a SQL file.

   .. note::

      Separate multiple SQL statements with semicolons (;) if you choose to enter SQL statements. Upload a file of no more than 100 MB if you choose to upload a SQL file.

#. Click **OK**.

#. In the SQL tuning task list, select a database, specify a time range, and click **Search** to filter tuning reports.

#. Click **View Details** in the **Operation** column to view tuning details.

   On the displayed diagnosis details page, view the tuning details, including the basic information, tuning status preview, tuning task list, and optimization suggestions.

   .. note::

      -  SQL tuning has the following constraints:

         -  Only MySQL InnoDB is supported.
         -  Only the diagnosis of the SELECT, INSERT, UPDATE, and DELETE statements is supported. An INSERT statement must contain a SELECT clause.
         -  Querying stored SQL statements such as information_schema, test, mysql, is not supported.
         -  View statements are not supported.

      -  The SQL tuning function obtains the table structure and data distribution information (non-original). The obtained data is only for logic diagnosis, but not stored on the DAS server.
      -  Obtaining table structure and data distribution information may add additional loads to the DB instance, but has little impact on its performance.
      -  Only the SQL diagnosis history is stored on the DAS server. You can delete it from the server permanently.
