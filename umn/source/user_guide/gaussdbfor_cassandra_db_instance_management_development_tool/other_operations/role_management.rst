:original_name: das_16_0019.html

.. _das_16_0019:

Role Management
===============

Procedure
---------

#. On the top menu bar, choose **Account Management** > **Role Management**.

#. On the role management page, click **Create Role** in the upper left corner.

#. .. _das_16_0019__li1344204304915:

   Set the parameters on the **Basic Information**, **Data Permissions**, and **Role Permissions** tab pages.

   On the **Basic Information** tab, enter a role name (mandatory), set a password, and confirm the password. You can select a role name from role members to assign the permissions of an existing role to the current role. If you do not need to set data permissions and role permissions for the role, click **Save** in the lower part of the page and then click **OK** in the displayed **SQL Preview** dialog box.

   .. note::

      If no password is set for the role (for example, role_03) or **Allow Login** is not selected for the role, role_03 cannot be used to log in to the database. If the permissions of role_03 are then assigned to another role (for example, test_02), test_02 will have all the permissions of role_03.

#. (Optional) On the **Data Permissions** tab, click **Add**. On the displayed page, set parameters as required, and then click **OK**. If you do not need to set other options, click **Save** in the lower part of the page and then click **OK** in the displayed **SQL Preview** dialog box.

#. .. _das_16_0019__li2400155210220:

   (Optional) On the **Role Permissions** tab, click **Add**. On the displayed page, select a resource type, role name, and permissions as required, and then click **OK**. If you do not need to set other options, click **Save** in the lower part of the page and then click **OK** in the displayed **SQL Preview** dialog box.

#. On the role management page, edit existing roles if needed. For how to edit a role, see :ref:`3 <das_16_0019__li1344204304915>` to :ref:`5 <das_16_0019__li2400155210220>`. Delete existing roles if needed. Deleted roles cannot be restored. Exercise caution when performing this operation.

   .. note::

      The admin, monitor, backupuser, and rwuser roles are system roles and cannot be edited or deleted.
