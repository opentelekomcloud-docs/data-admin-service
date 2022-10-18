:original_name: das_20_0029.html

.. _das_20_0029:

Modifying Firewall Rules
========================

#. In the ECS list, locate the required ECS and click **Remote Login**.

#. Enter the username and password. After the login is successful, run the following command to check the iptables configuration:

   .. code-block::

      iptables -S

   |image1|

   .. note::

      -  The port next to **--dport** indicates the port that can be accessed.
      -  Perform the following operations to ensure that the port can be accessed:

         -  Add an iptables rule to allow access to the port.

         -  Run the following command to disable the firewall:

            .. code-block::

               systemctl stop iptables

.. |image1| image:: /_static/images/en-us_image_0000001387792089.png
