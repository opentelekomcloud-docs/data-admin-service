:original_name: das_15_0032.html

.. _das_15_0032:

User Management
===============

Multiple users with different permissions can be created to access a DB instance or database, but the permissions of these users cannot exceed the operation permissions of the account.

Creating a User
---------------

#. Log in to the OTC console.
#. Click |image1| in the upper left corner and select a region and project.
#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Account Management** > **User Management**.
#. Click **Create User**. On the displayed page, enter the user information, such as basic information, basic permissions, extended permissions, and schema (optional), and select the read policy type.

   .. note::

      DDM supports most of MySQL syntax and permissions. For more information about MySQL accounts and permissions, see `MySQL Documentation <https://dev.mysql.com/doc/refman/8.0/en/privileges-provided.html>`__.

#. Ensure that the settings are correct and click **Save**.

Editing a User
--------------

#. Log in to the OTC console.
#. Click |image3| in the upper left corner and select a region and project.
#. Click |image4| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Account Management** > **User Management**.
#. In the user list, locate the user whose information you want to edit and click **Edit** in the **Operation** column.
#. On the displayed page, edit basic information, basic permissions and extended permissions, and click **Save**.

Deleting a User
---------------

#. Log in to the OTC console.
#. Click |image5| in the upper left corner and select a region and project.
#. Click |image6| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Account Management** > **User Management**.
#. In the user list, locate the user that you want to delete and click **Delete** in the **Operation** column.
#. In the displayed dialog box, click **Yes**.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
.. |image3| image:: /_static/images/en-us_image_0000001694653209.png
.. |image4| image:: /_static/images/en-us_image_0000001694653201.png
.. |image5| image:: /_static/images/en-us_image_0000001694653209.png
.. |image6| image:: /_static/images/en-us_image_0000001694653201.png
