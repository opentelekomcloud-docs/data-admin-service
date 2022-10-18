:original_name: das_05_0100.html

.. _das_05_0100:

SQL Diagnosis
=============

Procedure
---------

#. Log in to the DAS console using your username and password.
#. On the **Overview** page, click **Go to Intelligent O&M**.
#. Select the required instance and click **Details** to go to the Intelligent O&M overview page.
#. Choose **SQL** > **SQL Diagnosis**. On the displayed page, select the required database, enter the SQL statements to be diagnosed, and click **Diagnose**. The diagnosis result page is displayed.
#. On the **SQL Diagnosis** page, enter SQL statements and click **Execute**. The system automatically executes the statements and displays a result set.
#. On the **SQL Diagnosis** page, enter multiple SQL statements and click **Format**. The system automatically formats all SQL statements.
#. On the **SQL Diagnosis** page, enter multiple SQL statements and click **View Execution Plan**. The system automatically executes all SQL statements in sequence.

   .. note::

      -  Only MySQL InnoDB is supported.

      -  Only the diagnosis of SELECT, INSERT, UPDATE, and DELETE statements is supported. An INSERT statement must contain a SELECT clause.

      -  SQL statements for querying system databases information_schema, test, and mysql are not supported.

      -  SQL statements that use views are not supported.

      -  The SQL diagnosis function obtains the table structure and data distribution information (non-original). The obtained data is only for logic diagnosis, but not stored on the DAS server.

      -  Obtaining table structure and data distribution information may add additional loads to the DB instance, but has little impact on its performance.

      -  Only the SQL diagnosis history is stored on the DAS server. You can delete it from the server permanently.

      -  SQL formatting improves the readability of SQL statements. Formatting SQL statements enables statements to be displayed in line break mode, but does not change their logic and semantics.

         The formatting takes effect for all the SQL statements in the SQL window. You cannot format only the selected statement.
