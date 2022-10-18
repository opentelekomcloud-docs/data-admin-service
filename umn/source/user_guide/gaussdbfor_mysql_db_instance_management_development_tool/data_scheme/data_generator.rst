:original_name: das_13_0053.html

.. _das_13_0053:

Data Generator
==============

Scenarios
---------

DAS can automatically generate test data according to certain rules. This test data can be inserted into a database to test program functions. This section describes how to generate test data according to the predefined rules.

Procedure
---------

#. On the top menu bar, choose **Data Scheme** > **Data Generator**.
#. On the displayed page, click **Create Task**. In the displayed dialog box, configure the required parameters.

   -  Rows to Generate

      A maximum of 1,000,000 rows of data can be generated.

   -  Conflict Policy

      If you select **Skip**, the system skips data rows in conflict and continues generating data. If you select **Replace**, the system replaces existing rows with new ones that have the same primary key.

   -  Generation Type

      On the **Create Task** page, double-click one column. Set rules for generating data randomly based on the column information. For example, if the column name is **time**, you need to specify start and end time and the generation format. Alternatively, select **Based on current time**.

#. Click **Preview** to check whether the generated data is as expected. If not, modify the settings. Then, click **Generate**. Alternatively, directly click **Generate**.
#. In the task list, locate the created task and click **Details**. You can also delete the task as required.
