:original_name: das_04_0023.html

.. _das_04_0023:

Altering a View
===============

This section describes how to modify the definition, security, and algorithm of a view on the DAS console.

Usage Notes
-----------

Improper alterations on a view will cause instance or service exceptions.

Procedure
---------

#. Log in to the OTC console.
#. Click |image1| in the upper left corner and select a region and project.
#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Database Management**.
#. Click **Change** on the right of the current database to switch to the database where you want to create a table.
#. On the **Objects** tab page, choose **Views**.
#. Locate the view you want to alter and click **Alter** in the **Operation** column.
#. On the displayed page, modify information of the view, including the security, algorithm, and view definition statement.

   .. table:: **Table 1** Parameter description

      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                             |
      +===================================+=========================================================================================================================================================================================================================================================+
      | Definer                           | Enter a definer.                                                                                                                                                                                                                                        |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Algorithm                         | (Optional) You can leave this parameter blank or set it to **MERGE**, **TEMPTABLE**, or **UNDEFINED**.                                                                                                                                                  |
      |                                   |                                                                                                                                                                                                                                                         |
      |                                   | -  **UNDEFINED**: The required algorithm is automatically selected.                                                                                                                                                                                     |
      |                                   | -  **MERGE**: A combination algorithm. Executing this algorithm will combine and execute SQL statements of the view and those of the external query view.                                                                                               |
      |                                   | -  **TEMPTABLE**: The result is stored in a temporary table for query.                                                                                                                                                                                  |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Security                          | (Optional) You can leave this parameter blank or set it to **DEFINER** or **INVOKER**.                                                                                                                                                                  |
      |                                   |                                                                                                                                                                                                                                                         |
      |                                   | -  **DEFINER**: When the view is executed, the user account specified by DEFINER will be used to check access privileges for the view.                                                                                                                  |
      |                                   | -  **INVOKER**: When the view is executed, the user account specified by INVOKER will be used to check access privileges for the view.                                                                                                                  |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Check Option                      | (Optional) You can leave this parameter blank or set it to **LOCAL** or **CASCADED**.                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                                         |
      |                                   | -  If you select **CASCADED** for **Check Option**, the view that the current view depends on will also have the check option.                                                                                                                          |
      |                                   | -  If you select **LOCAL** for **Check Option**, the system checks whether the view that the current view depends on has check options. If yes, the system checks the view that the current view depends on. If no, the system does not check the view. |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | View Definition Statement         | Enter a SQL statement for creating the view. You only need to enter the SELECT part.                                                                                                                                                                    |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **Alter** at the bottom of the page.
#. In the displayed dialog box, click **Execute**.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
