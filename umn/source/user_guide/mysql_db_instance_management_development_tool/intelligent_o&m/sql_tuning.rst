:original_name: das_04_0072.html

.. _das_04_0072:

SQL Tuning
==========

Scenarios
---------

SQL tuning helps you identify the SQL statements that are executed frequently or slowly, and consume large volumes of resources. You can optimize the database according to the diagnosis suggestions to ensure database stability.

Prerequisites
-------------

-  You have tuned SQL statements in the SQL window.

Procedure
---------

#. On the top menu bar, choose **Intelligent O&M** > **SQL Tuning**.

#. On the **SQL Tuning** page, click **Add SQL Performance Tuning** to add a SQL tuning task. In the displayed dialog box, enter SQL statements or upload a SQL file as required, and then click **OK**.

#. In the SQL tuning task list, select a database, specify a time range, and click **Search** to filter tuning reports. Click **View Details** in the **Operation** column to view tuning details.

   On the **View Details** page, you can view basic information of the tuning task, turning statuses, and tuned SQL statements.

   In the tuned SQL list, locate the required SQL and click **View Tuning Result Detail**.

   .. note::

      -  Only MySQL InnoDB is supported.
      -  Only the diagnosis of the SELECT, INSERT, UPDATE, and DELETE statements is supported. An INSERT statement must contain a SELECT clause.
      -  Querying stored SQL statements such as information_schema, test, mysql, is not supported.
      -  View statements are not supported.
      -  The SQL tuning function obtains the table structure and data distribution information (non-original). The obtained data is only for logic diagnosis, but not stored on the DAS server.
      -  Obtaining table structure and data distribution information may add additional loads to the DB instance, but has little impact on its performance.
      -  Only the SQL diagnosis history is stored on the DAS server. You can delete it from the server permanently.
