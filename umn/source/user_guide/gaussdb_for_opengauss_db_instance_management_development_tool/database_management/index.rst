:original_name: das_16_0034.html

.. _das_16_0034:

Database Management
===================

Function Overview
-----------------


.. figure:: /_static/images/en-us_image_0000001337271948.png
   :alt: **Figure 1** Database Management


   **Figure 1** Database Management

.. table:: **Table 1** Functions

   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Function                          | Description                                                                                                                                                        |
   +===================================+====================================================================================================================================================================+
   | Database information              | Displays the name, IP address, character set, and SQL window of the current database.                                                                              |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Schema list                       | Allows you to manage data with different schemas in a database.                                                                                                    |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Object list                       | Consists of five types of objects, respectively tables, views, stored procedures, triggers, and sequences.                                                         |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Metadata collection               | Allows DAS to automatically collects only the data such as database names, table names, and field names in an instance (user data in your tables is not included). |
   |                                   |                                                                                                                                                                    |
   |                                   | .. note::                                                                                                                                                          |
   |                                   |                                                                                                                                                                    |
   |                                   |    If there are too many tables, the system will not collect the metadata and display the table list to mitigate the impact on database performance.               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | List details                      | Displays the operation area for each type of object.                                                                                                               |
   +-----------------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. note::

   You can go to the **Database Management** page in either of the following ways:

   -  Choose **Database Management** on the top menu bar.
   -  In the database list of the **Home** page, locate the target database and click **Manage** in the **Operation** column.

Object List
-----------

You can manage tables, views, stored procedures, triggers, and sequences of GaussDB(for openGauss) databases. Graphical windows for creating objects are not available. To create new objects, execute SQL statements in the SQL window.

-  For details on how to manage tables, see :ref:`Table Management <das_16_0035>`.
-  For details on how to manage views, see :ref:`View Management <das_16_0038>`.
-  For details on how to manage stored procedures, see :ref:`Stored Procedure Management <das_16_0041>`.
-  For details on how to manage triggers, see :ref:`Trigger Management <das_16_0043>`.
-  For details on how to manage sequences, see :ref:`Sequence Management <das_16_0045>`.

-  :ref:`Table Management <das_16_0035>`
-  :ref:`View Management <das_16_0038>`
-  :ref:`Stored Procedure Management <das_16_0041>`
-  :ref:`Trigger Management <das_16_0043>`
-  :ref:`Sequence Management <das_16_0045>`

.. toctree::
   :maxdepth: 1
   :hidden: 

   table_management/index
   view_management/index
   stored_procedure_management/index
   trigger_management/index
   sequence_management/index
