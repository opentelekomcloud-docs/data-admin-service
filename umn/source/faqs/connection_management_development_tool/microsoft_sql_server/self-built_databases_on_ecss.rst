:original_name: das_20_0051.html

.. _das_20_0051:

Self-Built Databases on ECSs
============================

1. Error message: **The TCP/IP connection to the host 100.xxx.xx.xx, port xxx has failed.**

Error cause: The port number of the self-built database is incorrect, or the network is disconnected.

Solution: Ensure that the port number of the self-built database is correct and that the port is included in the security group rule and firewall whitelist. For details, see :ref:`Modifying ECS Security Group Rules <das_20_0028>` and :ref:`Modifying Firewall Rules <das_20_0029>`.
