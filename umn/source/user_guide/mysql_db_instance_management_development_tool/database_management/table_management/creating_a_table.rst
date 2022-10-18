:original_name: das_04_0009.html

.. _das_04_0009:

Creating a Table
================

Scenarios
---------

A MySQL data table consists of basic information, field/column information, virtual columns, indexes, and foreign keys. The virtual columns, indexes, and foreign keys are optional and can be configured based on service requirements.

Procedure
---------

#. On the top menu bar, choose **Database Management**. On the displayed **Objects** page, select **Tables** and click **Create Table**.
#. On the displayed page, specify the details under **Basic Information** (**Table Name** is mandatory). Click **Next**.
#. On the **Column** page, click **Add** and set **Column Name**, **Type**, **Length**, **Nullable**, **Primary Key**, **Comment**, and **Extended Information** as needed.

   -  If you do not need to add virtual columns, indexes, or foreign keys, click **Create** at the bottom of the page. In the displayed **SQL Preview** dialog box, click **Execute**.

   .. note::

      -  Only MySQL 5.6.5 and later support default DATETIME values.
      -  In versions earlier than MySQL 5.6.5, leave default values blank. Otherwise, an error occurs.

   -  If you need to add virtual columns, indexes, and foreign keys, click **Next**. Then, set the column name, type, length, nullable, primary key, expression, storage type, comment, and extended information. If you need to set the table index or foreign key, click **Next**. After the setting, click **Create**.

   .. note::

      When you create a foreign key, the type of columns in the referenced table must be the same as that of included columns, and must be the primary key or have a unique index.

#. In the **SQL Preview** dialog box, click **Execute** to create a table.

.. note::

   -  The length of a column name is limited. Enter no more than 64 characters for the MySQL engine.
   -  In the **Type** column, you can select only the parameters from the drop-down list box.
   -  In the **Length** column, you can change the length for some types of columns.
   -  If **Primary Key** is selected, **Nullable** will be grayed out.
   -  **Auto Increment** can be set for one column only. When it is selected, **Primary Key** must be selected, and a default value cannot be set.
