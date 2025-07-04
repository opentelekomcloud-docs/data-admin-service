:original_name: das_02_0002.html

.. _das_02_0002:

Logging In to a DB Instance
===========================

This section describes how to log in to a DB instance.

Usage Notes
-----------

The following DB instances are supported:

.. table:: **Table 1** Supported DB instances

   +-----------------------------------+-----------------------------------+
   | DB Instance Source                | Supported DB Engine               |
   +===================================+===================================+
   | DB instance                       | -  RDS for MySQL                  |
   |                                   |                                   |
   |                                   | -  DDM                            |
   +-----------------------------------+-----------------------------------+

-  The account used to create the current DB instance and the login account belong to the same account.
-  The created DB instance and DAS must be in the same region.


Logging In to a DB Instance
---------------------------

This section describes how to log in to a DB instance. After a DB instance is created, DAS automatically creates login information for an administrator.

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the target DB instance and click **Log In** in the **Operation** column.

   You need to enter the password at the first login. If **Remember Password** is selected at the first login, you do not need to enter the password again at subsequent logins.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
