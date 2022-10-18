:original_name: das_18_0034.html

.. _das_18_0034:

Single Node with Multiple Metrics
=================================

Intelligent O&M allows you to view the performance of multiple metrics on a single instance so that you can compare the metric performance.

Procedure
---------

#. Log in to the GaussDB(for openGauss) console.
#. Apply for Intelligent O&M according to :ref:`Intelligent O&M <das_18_0097>`.
#. Locate your desired instance and click **Details** to go to the Intelligent O&M overview page.
#. Choose **Performance** > **Single Node with Multiple Metrics**.
#. Click **Change Node** to change the instance node if needed.
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
#. Click **Detail** to the upper right corner of each graph to view the metric details. You can also view the metric details in the last 1 hour, 12 hours, 1 day, 2 days, 7 days, or customize a time range.
#. Click the **Performance Trends Comparisons** tab, select the desired metrics, and click **OK**.
#. Click **Detail** to the upper right corner of each graph to view the metric details. You can also view the metric details in a specified time range within the past week.
#. Enable **Interactive Graph** to view the performance of other metrics at the same time.
#. Click **Full Screen** for a clear view.
