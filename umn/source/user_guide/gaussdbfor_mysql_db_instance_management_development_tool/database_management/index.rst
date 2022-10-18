:original_name: das_13_0004.html

.. _das_13_0004:

Database Management
===================

Function Overview
-----------------

You can go to the **Database Management** page in either of the following ways:

-  In the database list of the **Home** page, locate the target database and click **Manage** in the **Operation** column.
-  Choose **Database Management** on the top menu bar.


.. figure:: /_static/images/en-us_image_0000001337271904.png
   :alt: **Figure 1** Database management


   **Figure 1** Database management

.. table:: **Table 1** Functions

   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
   | No.                               | Description                                                                                                                          |
   +===================================+======================================================================================================================================+
   | 1                                 | Displays the name of the current database.                                                                                           |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
   | 2                                 | Allows you to switch between system and non-system databases.                                                                        |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
   | 3                                 | Displays the IP address, port number, and character set of the current DB instance.                                                  |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
   | 4                                 | Allows you to open the SQL window of the current database.                                                                           |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
   | 5                                 | Periodically collects metadata such as databases, tables, and fields of the DB instance and stores the data to the databases of DAS. |
   |                                   |                                                                                                                                      |
   |                                   | Advantages:                                                                                                                          |
   |                                   |                                                                                                                                      |
   |                                   | -  Reduces queries on user databases and the impact on the performance of user databases.                                            |
   |                                   | -  Improves the search performance for DB instances that contain a large number of tables and supports pagination queries.           |
   |                                   |                                                                                                                                      |
   |                                   | Only structural metadata is collected, which means that user's table data is not included.                                           |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
   | 6                                 | Database management consists of three functional modules: objects, SQL tuning, and metadata collection.                              |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+
   | 7                                 | Allows you to perform operations.                                                                                                    |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------+

Object List
-----------

.. note::

   If there are too many tables, the system will not collect the metadata and display the table list to mitigate the impact on database performance.

You can manage tables, views, stored procedures, events, triggers, and functions of databases. The main operations include creating, querying, and modifying objects.

SQL Tuning
----------

SQL tuning helps you query the SQL statements that are executed frequently, consume a large amount of resources, or take a long time to execute. Therefore, you can optimize operations according to the diagnosis results.

#. On the **Database Management** page, click the **SQL Tuning** tab. You can search for SQL tuning history by date to view details or you can add or delete SQL tuning records.

#. Click **Add SQL Performance Tuning**. In the displayed dialog box, set **Task Type** to **SQL statement** or **SQL file**. Then, edit the SQL statements under **SQL Statement** and click **OK**.

   .. note::

      -  The following types of statements will be changed to the SELECT statements for tuning:

         **SELECT ... FOR UPDATE**, **UPDATE ... SET ... WHERE ...**, **DELETE FROM ... WHERE ...**, **INSERT INTO ... SELECT ...**

      -  Apart from the statements mentioned above, other statements cannot be changed to SELECT statements for tuning. The tuning task that contains unsupported SQL syntax will fail.

      -  The following shows the unsupported syntaxes:

         -  alter table t add index idx_name(name);
         -  show databases;
         -  grant SELECT,PROCESS on d.t to 'am'@'%' with grant option;
         -  insert into t(i, v) values (1, 'a').

      -  Only the diagnosis of the SELECT, INSERT, UPDATE, and DELETE statements is supported. An INSERT statement must contain a SELECT clause.

      -  Querying stored SQL statements such as information_schema, test, mysql, is not supported.

      -  View statements are not supported.

#. In the SQL tuning list, locate the target task and click **View Details** in the **Operation** column.

   You can view the tuning details at the bottom of the task list.

Metadata Collection
-------------------

DAS periodically collects the metadata of DB instance databases, tables, and fields and stores the collected data in the DAS database. In addition, it collects only structural metadata, but not data in user tables, which ensures data security. Metadata collection delivers the following advantages:

-  Reduces queries on user databases and the impact on the performance of user databases.
-  Improves the search performance for DB instances that contain a large number of tables and supports pagination queries.

#. On the **Database Management** page, enable **Auto Metadata Collection** in the upper right corner and click the **Metadata Collection** tab.
#. On the displayed page, click **Collect Now** to start the collection. You can also stop the collection or view the collection details.

   -  **Clear Collected Data**: Clears the collected data such as metadata, database structure, and table structure.
   -  **Delete Logs**: Deletes logs. Deleted logs cannot be restored. Exercise caution when performing this operation.

-  :ref:`Table Management <das_13_0007>`
-  :ref:`View Management <das_13_0017>`
-  :ref:`Event Management <das_13_0022>`
-  :ref:`Stored Procedure Management <das_13_0026>`
-  :ref:`Function Management <das_13_0030>`
-  :ref:`Trigger Management <das_13_0035>`

.. toctree::
   :maxdepth: 1
   :hidden: 

   table_management/index
   view_management/index
   event_management/index
   stored_procedure_management/index
   function_management/index
   trigger_management/index
