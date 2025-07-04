:original_name: das_01_0004.html

.. _das_01_0004:

DAS and Other Services
======================

With DAS, you can access cloud databases with a few clicks instead of through clients.

-  You can securely access data anytime and anywhere.
-  You can directly manage and modify the data directory structure on the web-based console.

Relational Database Service (RDS)
---------------------------------

DAS can manage RDS instances.

-  You have the username and password for logging in to the target database.
-  RDS instances and DAS are in the same region.

.. table:: **Table 1** DAS functions available to RDS instances

   ============================================== =====
   Module                                         MySQL
   ============================================== =====
   Database Management                            Y
   SQL Window                                     Y
   SQL History                                    Y
   Import                                         Y
   Export                                         Y
   Table Structure Comparison and Synchronization Y
   Data Generator                                 Y
   Task Scheduling                                Y
   Real-Time Performance                          Y
   Real-Time Sessions                             Y
   SQL Diagnosis                                  Y
   Diagnosis Report                               Y
   InnoDB Lock Query                              Y
   User Management                                Y
   ============================================== =====

Distributed Database Middleware (DDM)
-------------------------------------

DAS supports the management of DDM instances. To manage DDM instances, the following requirements must be met:

-  You have the username and password for logging in to the target database.
-  DDM instances and DAS are in the same region.

.. table:: **Table 2** DAS functions available to DDM instances

   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
   | Module                            | DDM                                                                                                             |
   +===================================+=================================================================================================================+
   | Database Management               | Y                                                                                                               |
   |                                   |                                                                                                                 |
   |                                   | .. note::                                                                                                       |
   |                                   |                                                                                                                 |
   |                                   |    Databases cannot be created or modified. Only the structure of broadcast and unsharded tables can be edited. |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
   | SQL Query                         | Y                                                                                                               |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
   | SQL History                       | Y                                                                                                               |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
   | Real-Time Sessions                | Y                                                                                                               |
   +-----------------------------------+-----------------------------------------------------------------------------------------------------------------+
