:original_name: das_10_0022.html

.. _das_10_0022:

How Do I Modify the Collation?
==============================

DAS does not support the SQL Server modification on the GUI. You can run commands to implement the modification.

Go to the SQL Window page of the database and run the following commands:

(In this example, the character set of the **test** database is set to SQL_Latin1_General_CP1_CI_AS.)

.. code-block::

   use root
   go
   ALTER DATABASE test COLLATE SQL_Latin1_General_CP1_CI_AS
