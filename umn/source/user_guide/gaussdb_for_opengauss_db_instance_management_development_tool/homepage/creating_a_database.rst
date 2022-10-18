:original_name: das_16_0026.html

.. _das_16_0026:

Creating a Database
===================

Procedure
---------

#. In the database list of the **Home** page, click **Create Database**.
#. In the displayed dialog box, enter a database name and specify the character set, template, and other required options.

   .. note::

      You can execute the following SQL statement to query system table **pg_collation** and view character sets and their corresponding collations and collation types:

      select pg_encoding_to_char(collencoding) as encoding,collname,collcollate,collctype from pg_collation ;

#. Click **OK**. The database you create appears in the database list.
