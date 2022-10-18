:original_name: das_08_0010.html

.. _das_08_0010:

Database Management
===================

Function Overview
-----------------


.. figure:: /_static/images/en-us_image_0000001387791909.png
   :alt: **Figure 1** Database Management


   **Figure 1** Database Management

.. table:: **Table 1** Functions

   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Function                          | Description                                                                                                                                                        |
   +===================================+====================================================================================================================================================================+
   | Sidebar                           | Consists of six types of objects (tables, views, stored procedures, events, triggers, and functions).                                                              |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Database information              | Displays the name, IP address, character set, SQL window, and data dictionary of the current database.                                                             |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Metadata Collection               | Allows DAS to automatically collects only the data such as database names, table names, and field names in an instance (user data in your tables is not included). |
   |                                   |                                                                                                                                                                    |
   |                                   | .. note::                                                                                                                                                          |
   |                                   |                                                                                                                                                                    |
   |                                   |    If there are too many tables, the system will not collect the metadata and display the table list to mitigate the impact on database performance.               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | SQL tuning                        | Diagnoses SQL statements and SQL files.                                                                                                                            |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | List details                      | Displays the operation area for each type of object.                                                                                                               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. note::

   You can go to the **Database Management** page in either of the following ways:

   -  Choose **Database Management** on the top menu bar.
   -  In the database list of the **Home** page, locate the target database and click **Manage** in the **Operation** column.

Object List
-----------

You can manage tables, views, stored procedures, events, triggers, and functions of the MySQL DB instances. The main operations include creating, querying, and modifying objects.

-  For details on how to manage tables, see :ref:`Table Management <das_04_0008>`.
-  For details on how to manage views, see :ref:`View Management <das_04_0019>`.
-  For details on how to manage events, see :ref:`Event Management <das_04_0026>`.
-  For details on how to manage stored procedures, see :ref:`Stored Procedure Management <das_04_0030>`.
-  For details on how to manage functions, see :ref:`Function Management <das_04_0035>`.
-  For details on how to manage triggers, see :ref:`Trigger Management <das_04_0051>`.

-  :ref:`Table Management <das_04_0008>`
-  :ref:`View Management <das_04_0019>`
-  :ref:`Stored Procedure Management <das_04_0030>`
-  :ref:`Event Management <das_04_0026>`
-  :ref:`Trigger Management <das_04_0051>`
-  :ref:`Function Management <das_04_0035>`

.. toctree::
   :maxdepth: 1
   :hidden: 

   table_management/index
   view_management/index
   stored_procedure_management/index
   event_management/index
   trigger_management/index
   function_management/index
