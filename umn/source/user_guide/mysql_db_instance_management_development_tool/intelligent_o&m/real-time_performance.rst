:original_name: das_04_0081.html

.. _das_04_0081:

Real-Time Performance
=====================

Scenarios
---------

With Intelligent O&M, you can comprehensively analyze DB instances to understand their performance and operating statuses. It provides multi-dimensional and real-time performance monitoring information, including real-time performance of a single instance, performance comparisons of multiple instances, and performance dashboard of multiple instances.

Procedure
---------

#. On the top menu bar, choose **Intelligent O&M** > **Real-Time Performance**.
#. On the displayed page, view a variety of metrics, including slow SQL queries, connections, QPS/TPS. You can also pause or start the monitoring and set the monitoring interval (1 to 10 seconds).
#. In the upper right corner, click **Set Metric** to select required metrics.

   .. table:: **Table 1** Real-time performance metrics

      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Metric                                | Description                                                                                                                                                 |
      +=======================================+=============================================================================================================================================================+
      | Slow Queries                          | Difference between two adjacent slow query collection points.                                                                                               |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | QPS \| TPS                            | **QPS**: Number of SQL statement executions per second.                                                                                                     |
      |                                       |                                                                                                                                                             |
      |                                       | **TPS**: Number of transactions executed per second.                                                                                                        |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Connections                           | **Total**: Number of enabled connections.                                                                                                                   |
      |                                       |                                                                                                                                                             |
      |                                       | **Active**: Number of active connections among the enabled ones.                                                                                            |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | DML Executions                        | **select**: Number of SELECT statement executions per second.                                                                                               |
      |                                       |                                                                                                                                                             |
      |                                       | **insert**: Number of INSERT statement executions per second.                                                                                               |
      |                                       |                                                                                                                                                             |
      |                                       | **update**: Number of UPDATE statement executions per second.                                                                                               |
      |                                       |                                                                                                                                                             |
      |                                       | **delete**: Number of DELETE statement executions per second.                                                                                               |
      |                                       |                                                                                                                                                             |
      |                                       | **insert_select**: Number of INSERT and QUERY statement executions per second.                                                                              |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | InnoDB Cache                          | **Cache Hit Ratio**: Measures how many content requests a cache can deliver successfully from its cache storage, compared to how many requests it receives. |
      |                                       |                                                                                                                                                             |
      |                                       | **Cache Usage**: Usage of a cache.                                                                                                                          |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | InnoDB Accessed Rows                  | **rows_read**: Number of rows read from an InnoDB storage engine table.                                                                                     |
      |                                       |                                                                                                                                                             |
      |                                       | **rows_inserted**: Number of rows inserted into an InnoDB storage engine table.                                                                             |
      |                                       |                                                                                                                                                             |
      |                                       | **rows_updated**: Number of rows updated in an InnoDB storage engine table.                                                                                 |
      |                                       |                                                                                                                                                             |
      |                                       | **rows_deleted**: Number of rows deleted from an InnoDB storage engine table.                                                                               |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Logical Reads \| Physical Reads       | **Logic Reads**: Number of logical reads per second.                                                                                                        |
      |                                       |                                                                                                                                                             |
      |                                       | **Physical Reads**: Number of physical reads per second.                                                                                                    |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | InnoDB Average Row Lock Duration (ms) | Average locking time of InnoDB row locks (ms).                                                                                                              |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | InnoDB Row Lock Waits                 | **Average InnoDB Row Lock Waits**: Average wait times of InnoDB row locks.                                                                                  |
      |                                       |                                                                                                                                                             |
      |                                       | **Current InnoDB Row Lock Waits**: Number of current waits of InnoDB row locks.                                                                             |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Temporary Tables \| Files             | **Temporary tables**: Number of temporary tables that are automatically created during SQL statement execution.                                             |
      |                                       |                                                                                                                                                             |
      |                                       | **Temporary files**: Number of temporary files that are automatically created during SQL statement execution.                                               |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Network Traffic                       | **Total**: Total incoming and outgoing traffic of an instance.                                                                                              |
      |                                       |                                                                                                                                                             |
      |                                       | **Incoming**: Incoming traffic of an instance.                                                                                                              |
      |                                       |                                                                                                                                                             |
      |                                       | **Outgoing**: Outgoing traffic of an instance.                                                                                                              |
      +---------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------+
