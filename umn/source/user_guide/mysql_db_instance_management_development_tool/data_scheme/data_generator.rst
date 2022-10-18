:original_name: das_04_0058.html

.. _das_04_0058:

Data Generator
==============

Scenarios
---------

During the functional testing of a program, a large amount of test data complying with specific rules needs to be inserted into the database. DAS allows you to automatically, efficiently generate test data based on specific rules.

Procedure
---------

#. On the top menu bar, choose **Data Scheme** > **Data Generator**.
#. On the displayed page, click **Create Task**. In the displayed dialog box, configure the required parameters.

   -  Rows to Generate

      A maximum of 1,000,000 rows of data can be generated.

   -  Conflict Policy

      If you select **Skip**, the system skips data rows in conflict and continues generating data. If you select **Replace**, the system replaces existing rows with new ones that have the same primary key.

   -  Generation type

      You can set the rules for randomly generated data based on the column settings. For example, if the column type is time, you can set the start time, end time, and format, or set the value to the current time.

#. Click **Preview** to check whether the generated data is as expected. If not, modify the settings. Then, click **Generate**. Alternatively, directly click **Generate**.
#. In the task list, locate the created task and click **Details**. You can also delete the task as required.
