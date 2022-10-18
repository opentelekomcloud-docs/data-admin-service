:original_name: das_20_0098.html

.. _das_20_0098:

Self-Built Databases on ECSs
============================

1. Error message: **Connection refused (Connection refused).**

Error cause: The port number of the self-built database is incorrect, or the network is disconnected.

Solution: Ensure that the port number of the self-built database is correct and that the port is included in the security group rule and firewall whitelist. For details, see :ref:`Modifying ECS Security Group Rules <das_20_0028>` and :ref:`Modifying Firewall Rules <das_20_0029>`.
