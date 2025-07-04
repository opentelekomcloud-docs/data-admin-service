:original_name: das_01_0005.html

.. _das_01_0005:

Basic Concepts
==============

Metadata Collection
-------------------

DAS originally allowed you to query metadata of databases, tables, and fields in each instance, but now it can also periodically collect metadata and store it in the DAS database.

Selecting an AZ
---------------

When determining whether to deploy resources in the same AZ, consider your applications' requirements on disaster recovery (DR) and network latency.

-  For robust DR, deploy clusters in different AZs within the same region.
-  For lower network latency, deploy resources in the same AZ.
