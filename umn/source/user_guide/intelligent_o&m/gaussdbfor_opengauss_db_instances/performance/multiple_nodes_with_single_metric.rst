:original_name: das_18_0038.html

.. _das_18_0038:

Multiple Nodes with Single Metric
=================================

Intelligent O&M allows you to view the performance of the same metric on multiple instances so that you can compare the metric performance.

Procedure
---------

#. Log in to the GaussDB(for openGauss) console.
#. Apply for Intelligent O&M according to :ref:`Intelligent O&M <das_18_0097>`.
#. Locate your desired instance and click **Details** to go to the Intelligent O&M overview page.
#. Choose **Performance** > **Multiple Nodes with Single Metric**.
#. Click **Select Node** to select instances. A maximum of 5 instances can be selected, and the type of the selected instances must be the same.
#. Click **Select Metric** and select the instance metrics to display.

   .. table:: **Table 1** Instance metrics

      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      | Category      | Metric                    | Description                                                                                             |
      +===============+===========================+=========================================================================================================+
      | CPU           | CPU Usage                 | CPU usage of the monitored object (Unit: %)                                                             |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      |               | CPU Load                  | Average CPU load over the past 1, 5, and 15 minutes. The value is obtained using the w command.         |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      |               | CPU Load in Past 1 Minute | Average CPU load over the past 1 minute. The value is obtained using the w command.                     |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      | Memory        | Memory Usage              | Memory usage of the monitored object (Unit: %)                                                          |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      |               | Available Memory          | Memory available to the operating system (Unit: GB)                                                     |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      | Network       | Data Transfer In          | Average number of bytes sent by the VM of the monitored object in a measurement period (Unit: KB/s)     |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      |               | Data Transfer Out         | Average number of bytes received by the VM of the monitored object in a measurement period (Unit: KB/s) |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+
      | Other Metrics | -                         | -                                                                                                       |
      +---------------+---------------------------+---------------------------------------------------------------------------------------------------------+

#. Click **OK**.
#. Click **Performance History** and specify a time range in the upper right corner to view metric details in the past last 1 hour, 12 hours, 1 day, 2 days, or 7 days.
#. Click the **Performance Trends Comparisons** tab, select the desired metrics, and click **OK**.
#. View the metric details in a specified time range within the past week.
#. Click **Full Screen** for a clear view.
