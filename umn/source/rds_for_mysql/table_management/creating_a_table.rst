:original_name: das_04_0009.html

.. _das_04_0009:

Creating a Table
================

A data table consists of basic information, columns, generated columns, indexes, and foreign keys, among which generated columns, indexes, and foreign keys are optional. Configure these items as required.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Database Management**.

#. Click **Change** on the right of the current database to switch to the database where you want to create a table.

#. On the **Objects** tab page, choose **Tables**.

#. Click **Create Table**.

#. Configure basic information as follows:

   Enter a table name, specify the storage engine, character set, collation, and enter a comment in sequence. The table name is mandatory.

#. (Optional) Configure advanced settings.

   Specify parameters based on service requirements.

   To learn more about partitioned tables, see the following note:

   Table partitioning is used to divide a large table into several small tables based on conditions. Different rows in the table can be allocated to different physical partitions. Creating a partitioned table is not recommended because there are many constraints on MySQL partitioned tables.

   If you need to create a partitioned table, you can create one by referring to the following example. The supported partitioning methods are RANGE, LIST, COLUMNS, KEY, and HASH.

   For example, if you want to create partitioned table **employees**, enter the following content for **Partition Definition**:

   Creating a partitioned table:

   .. code-block:: text

      CREATE TABLE employees (
      id INT NOT NULL,
      fname VARCHAR(30),
      lname VARCHAR(30),
      hired DATE NOT NULL DEFAULT '1970-01-01',
      separated DATE NOT NULL DEFAULT '9999-12-31',
      job_code INT NOT NULL,
      store_id INT NOT NULL
      )
      PARTITION BY RANGE (store_id) (
      PARTITION p0 VALUES LESS THAN (6),
      PARTITION p1 VALUES LESS THAN (11),
      PARTITION p2 VALUES LESS THAN (16),
      PARTITION p3 VALUES LESS THAN (21)
      );

   Specifying a partition definition:

   .. code-block:: text

      PARTITION BY RANGE (store_id) (
      PARTITION p0 VALUES LESS THAN (6),
      PARTITION p1 VALUES LESS THAN (11),
      PARTITION p2 VALUES LESS THAN (16),
      PARTITION p3 VALUES LESS THAN (21)
      )

#. Click **Next**.

#. On the **Column** page, click **Add**.

   -  Set **Column Name**, **Type**, **Length**, **Nullable**, **Primary Key**, **Comment**, and **Extended Information** as needed.

      .. note::

         -  The length of a column name is limited. Enter no more than 64 characters for the MySQL engine.
         -  In the **Type** column, you can select only the parameters from the drop-down list box.
         -  In the **Length** column, retain the default value. For some columns whose length is variable, you can change their lengths.
         -  If **Primary Key** is selected, **Nullable** will be grayed out.
         -  **Auto Increment** can be set for one column only. When it is selected, **Primary Key** must be selected, and no default values can be set.

   -  If you do not need to add generated columns, indexes, or foreign keys, click **Create**.

      .. note::

         -  Only MySQL 5.6.5 and later versions support default DATETIME values.
         -  In versions earlier than MySQL 5.6.5, leave default values blank. Otherwise, an error may occur.

   -  If you need to add generated columns, indexes, and foreign keys, click **Next** until all your desired parameters are specified. After the setting is complete, click **Create**.

      .. note::

         When you create a foreign key, the type of columns in the referenced table must be the same as that of included columns, and must be the primary key or have a unique index.

#. In the **SQL Preview** dialog box, click **Execute**.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
