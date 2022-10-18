:original_name: das_13_0008.html

.. _das_13_0008:

Creating a Table
================

Scenarios
---------

A GaussDB(for MySQL) database table consists of basic information, fields or columns, virtual columns, indexes, and foreign keys, among which virtual columns, indexes, and foreign keys are optional. Configure these items as required.

Procedure
---------

#. On the top menu bar, choose **Database Management**. On the displayed **Objects** tab, choose **Tables** and click **Create Table**.
#. On the displayed page, specify the table details on the **Basic Information** page (**Table Name** is mandatory). Click **Next**.
#. On the **Column** page, click **Add** and set **Column Name**, **Type**, **Length**, **Nullable**, **Primary Key**, and **Extended Information** as needed.

   -  If you do not need to add virtual columns, indexes, or foreign keys, click **Create** at the bottom of the page. In the displayed **SQL Preview** dialog box, click **Execute**.

   -  If you need to add virtual columns, indexes, and foreign keys, click **Next**. Then, set the column name, type, length, nullable, primary key, expression, storage type, comment, and extended information. After the settings are complete, click **Create**.

   .. note::

      When you create a foreign key, the type of columns in the referenced table must be the same as that of included columns, and must be the primary key or have a unique index.

#. In the **SQL Preview** dialog box, click **Execute** to create a table.

.. note::

   -  The length of a column name is limited. Enter no more than 64 characters.
   -  In the **Type** column, you can select only the parameters from the drop-down list box.
   -  In the **Length** column, you can change the length for some types of columns.
   -  If **Primary Key** is selected, **Nullable** will be grayed out.
   -  **Auto Increment** can be set for one column only. When it is selected, **Primary Key** must be selected, and a default value cannot be set.
