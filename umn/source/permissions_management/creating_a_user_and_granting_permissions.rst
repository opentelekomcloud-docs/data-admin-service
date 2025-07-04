:original_name: das_08_0003.html

.. _das_08_0003:

Creating a User and Granting Permissions
========================================

You can use IAM to implement refined permission control for DAS resources. To be specific, you can:

-  Create IAM users for employees from different departments of your enterprise. In this way, each IAM user has unique security credentials and can use DAS resources.
-  Grant only the permissions required for users to perform a specific task.
-  Entrust an account or cloud service to perform professional and efficient O&M on your DAS resources.

If your account does not need individual IAM users, then you may skip over this section.

:ref:`Figure 1 <das_08_0003__fig1111310313463>` describes how to grant permissions to a user group.

Prerequisites
-------------

Before assigning permissions to user groups, you should learn about DAS system policies and select policies based on service requirements.

Process Flow
------------

.. _das_08_0003__fig1111310313463:

.. figure:: /_static/images/en-us_image_0000001694533621.jpg
   :alt: **Figure 1** Flowchart for granting DAS permissions

   **Figure 1** Flowchart for granting DAS permissions

#. .. _das_08_0003__li102021954124416:

   Create a user group and assign permissions to it.

   Create a user group on the IAM console and attach the **DAS FullAccess** policy to the group.

#. Create a user and add it to a user group.

   Create a user on the IAM console and add the user to the group created in :ref:`1 <das_08_0003__li102021954124416>`.

#. Log in and verify permissions.

   In the service list, choose **Data Admin Service**. On the displayed page, click **Add DB Instance Connection**. If a database connection can be created, the DAS permissions have taken effect.
