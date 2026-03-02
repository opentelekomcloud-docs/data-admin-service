:original_name: das_01_2100.html

.. _das_01_2100:

Logging In to a DB Instance
===========================

This section describes how to log in to a DB instance on DAS.

After a DB instance is created, DAS automatically creates login information for an administrator.

If you want to use a non-administrator account to log in to the DB instance, you need to create a DB instance login first. For details, see :ref:`Configuring Login Information <das_01_2100__section12227732105612>`.

Usage Notes
-----------

-  RDS for MySQL and DDM instances are supported.
-  The created DB instance and DAS must be in the same region.


Logging In to a DB Instance
---------------------------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the target DB instance and click **Log In** in the **Operation** column.

   You need to enter the password at the first login. If **Remember Password** is selected at the first login, you do not need to enter the password again at subsequent logins.

.. _das_01_2100__section12227732105612:

Configuring Login Information
-----------------------------

#. Log in to the OTC console.

#. Click |image3| in the upper left corner and select a region and project.

#. Click |image4| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. On the **My DB Instance Connections** tab page, click **Add DB Instance Connection**.

#. Configure parameters for the new DB instance connection.

   .. table:: **Table 1** Description

      +------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter                    | Description                                                                                                                                                                                                                                                   | Example Value         |
      +==============================+===============================================================================================================================================================================================================================================================+=======================+
      | DB Engine                    | DB engine for the instance that you want to add login information for.                                                                                                                                                                                        | MySQL                 |
      +------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Source Database              | The source database depends on the DB engine that you select.                                                                                                                                                                                                 | RDS                   |
      |                              |                                                                                                                                                                                                                                                               |                       |
      |                              | After you select a source database, all instances of the current type under your account are displayed. You can select the instance that you want to add a login for.                                                                                         |                       |
      |                              |                                                                                                                                                                                                                                                               |                       |
      |                              | The following types of source databases are supported:                                                                                                                                                                                                        |                       |
      |                              |                                                                                                                                                                                                                                                               |                       |
      |                              | -  RDS                                                                                                                                                                                                                                                        |                       |
      |                              | -  DDM                                                                                                                                                                                                                                                        |                       |
      +------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Login Username               | Username for logging in to the selected DB instance.                                                                                                                                                                                                          | root                  |
      |                              |                                                                                                                                                                                                                                                               |                       |
      |                              | The user must have the permission to allow DAS to access the selected DB instance using an IP address.                                                                                                                                                        |                       |
      +------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Password                     | Password for logging in to the selected DB instance.                                                                                                                                                                                                          | ``-``                 |
      |                              |                                                                                                                                                                                                                                                               |                       |
      |                              | You can select **Remember Password**. With this function enabled, you do not need to enter the password when you want to log in to the DB instance later.                                                                                                     |                       |
      +------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Description                  | This parameter is optional.                                                                                                                                                                                                                                   | ``-``                 |
      +------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Show Executed SQL Statements | If this function is enabled, all the SQL statements executed in the SQL window will be saved.                                                                                                                                                                 | Enabled               |
      |                              |                                                                                                                                                                                                                                                               |                       |
      |                              | You are advised to enable **Show Executed SQL Statements**. With it enabled, you can choose **SQL Operations** > **SQL History** to see what SQL statements you have executed and can re-execute any executed SQL statements rather than entering them again. |                       |
      +------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

#. After the DB instance information is configured, click **Test Connection** on the right of the password text box.

   -  If the connection test is successful, go to :ref:`8 <das_01_2100__li77831545112>`.
   -  If a message is displayed indicating a connection test failure and failure causes, modify DB instance information based on the message and then go to :ref:`8 <das_01_2100__li77831545112>`.

#. .. _das_01_2100__li77831545112:

   After the connection test is successful, click **OK**.

#. On the **My DB Instance Connections** tab page, view information about the new DB instance connection.

   You can also click **Modify** in the **Operation** column to modify the instance login information, or click **Delete** to delete unnecessary instance login information.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
.. |image3| image:: /_static/images/en-us_image_0000001752041285.png
.. |image4| image:: /_static/images/en-us_image_0000001704241568.png
