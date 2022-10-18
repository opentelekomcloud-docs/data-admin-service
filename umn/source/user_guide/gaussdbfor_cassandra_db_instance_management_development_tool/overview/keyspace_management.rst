:original_name: das_16_0004.html

.. _das_16_0004:

Keyspace Management
===================

Object List
-----------

.. note::

   If there are too many tables, the system will not collect the metadata and display the table list to mitigate the impact on database performance.

You can manage instance tables, views, and custom types, and perform operations including opening and viewing objects.

For details on how to manage tables, see :ref:`Table Management <das_16_0007>`.

Metadata Collection
-------------------

DAS periodically collects DB instance metadata and stores the collected data in the DAS database. In addition, it collects only structural metadata, but not data in user tables, which ensures data security. Metadata collection delivers the following advantages:

-  Reduces queries on user keyspaces and the impact on the performance of user databases.
-  Improves the search performance for DB instances that contain a large number of tables and supports pagination queries.

#. On the **Keyspace Management** page, click the **Metadata Collection** tab.
#. On the displayed page, click **Collect Now** to start the collection. You can also stop the collection or view collection details.

   -  **Clear Collected Data**: Clears the collected data such as metadata, keyspace structure, and table structure.
   -  **Delete Logs**: Deletes logs. Deleted logs cannot be restored. Exercise caution when performing this operation.
