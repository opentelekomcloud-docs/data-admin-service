:original_name: das_04_0058.html

.. _das_04_0058:

Data Generator (Not Promoted)
=============================

During the functional testing of a program, a large amount of test data complying with specific rules needs to be inserted into the database. DAS can help you generate test data based on specific rules. This section describes how to generate test data on the DAS console.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Data Scheme** > **Data Generator**.

#. On the displayed page, click **Create Task**.

#. In the displayed dialog box, configure required parameters

   -  Rows to Generate

      A maximum of 1,000,000 rows of data can be generated.

   -  Conflict Policy

      If you select **Skip**, the system skips data rows in conflict and continues generating data.

      If you select **Replace**, the system replaces existing rows with new ones that have the same primary key.

   -  Generation Mode

      You can set the rules for randomly generated data based on the column settings. For example, if the column type is time, you can set the start time, end time, and format, or select **Based on current time**.

#. Click **Preview** to check whether the data that will be generated can meet your requirements. If not, adjust the generation rules.

#. Click **Generate**.

#. In the task list, locate the created task and click **Details**.

   You can also delete the task as required.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
