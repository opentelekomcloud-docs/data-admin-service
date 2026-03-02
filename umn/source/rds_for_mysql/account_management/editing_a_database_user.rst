:original_name: das_04_0061.html

.. _das_04_0061:

Editing a Database User
=======================

This section describes how to edit user information, including the username, password, global permissions, object permissions, advanced settings, and roles.

Usage Notes
-----------

Improper database user settings will cause instance or service exceptions.

Procedure
---------

#. Log in to the OTC console.
#. Click |image1| in the upper left corner and select a region and project.
#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.
#. In the navigation pane on the left, choose **Development Tool**.
#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.
#. On the top menu bar, choose **Account Management** > **User Management**.
#. In the user list, locate the user whose information you want to edit and click **Edit** in the **Operation** column.

   -  Permissions for multiple users cannot be modified at the same time. For example, if two users with the same username and different host addresses of 192.% and 193.% are created, modifying permissions of the user with the host address of 192.% does not affect permissions of the other user.

   -  When you edit a user, adding host addresses to the user does not create multiple users. For example, if a user already has a host address, 192.%, adding host address 194.% to it does not create another user with the host address of 194.%. This operation only changes the host address of the user from 192.% to 192.%,194.%.

      |image3|

   -  For details about how to configure other parameters, see :ref:`Table 2 <das_04_0060__table83726102050>` in :ref:`Creating a Database User <das_04_0060>`.

#. After configuring required parameters, click **Save**. In the preview dialog box, click **OK**.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
.. |image3| image:: /_static/images/en-us_image_0000001646334314.png
