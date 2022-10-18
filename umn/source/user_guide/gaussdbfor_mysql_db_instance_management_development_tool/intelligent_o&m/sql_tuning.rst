:original_name: das_11_0060.html

.. _das_11_0060:

SQL Tuning
==========

Procedure
---------

#. On the top menu bar, choose **Intelligent O&M** > **SQL Tuning**.
#. In the displayed dialog box, select an instance and click **OK**.
#. On the **SQL Tuning** page, click **Add SQL Performance Tuning**. In the displayed dialog box, enter the SQL statements to be diagnosed and click **OK**.
#. Click **View Details** in the **Operation** column to view tuning details.
#. Under **Tuned SQL List**, click **View Tuning Result Detail** in the **Operation** column to view tuning details.

   .. note::

      -  The SQL tuning function obtains the table structure and data distribution information (non-original). The obtained data is only for logic diagnosis, but not stored on the DAS server.
      -  Obtaining table structure and data distribution information may add additional loads to the DB instance, but has little impact on its performance.
      -  Only the SQL diagnosis history is stored on the DAS server. You can delete it from the server permanently.
