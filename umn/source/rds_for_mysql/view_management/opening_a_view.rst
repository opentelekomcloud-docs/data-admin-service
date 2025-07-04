:original_name: das_04_0022.html

.. _das_04_0022:

Opening a View
==============

This section describes how to view details of a view on the DAS console.

Usage Notes
-----------

Views do not have primary keys and their data can only be queried but not edited.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Database Management**.

#. Click **Change** next to **Current Database** to switch to the target database.

#. On the **Objects** tab page, choose **Views**.

#. Locate the view you want to open and click **Open** in the **Operation** column.

#. On the displayed page, check view details and query view information using a Where condition.

   You can also perform operations described in :ref:`Table 1 <das_04_0022__table48931828115911>` on the view.

   .. _das_04_0022__table48931828115911:

   .. table:: **Table 1** UI operations

      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Name                          | Description                                                                                                                                  |
      +===============================+==============================================================================================================================================+
      | Where Condition               | Filters records.                                                                                                                             |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Copy Row                      | Allows you to copy data of a selected row. Specifically, select the row you want to copy and click **Copy Row**.                             |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Copy Column                   | Allows you to copy data of a selected column. Specifically, click **Copy Column** and select a column from the drop-down list.               |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Copy                          | Allows you to copy a piece of data. Specifically, hover the cursor on the data and click **Copy**.                                           |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Column Settings               | Allows you to set the columns you want to display.                                                                                           |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Convert binary to hexadecimal | Prevents binary data in columns from being displayed as garbled characters. If there is binary data in columns, you must select this option. |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Refresh                       | Allows you to update table data manually.                                                                                                    |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Row Details                   | Shows details of a specified row.                                                                                                            |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Add Row                       | Allows you to add rows.                                                                                                                      |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Submit                        | Allows you to submit and save the changes to data.                                                                                           |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Delete Row                    | Allows you to delete the selected rows.                                                                                                      |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+
      | Export                        | Exports a maximum of 10,000 data records to a CSV or SQL file.                                                                               |
      +-------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------+

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
