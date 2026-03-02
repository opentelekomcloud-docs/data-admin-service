:original_name: das_04_0042.html

.. _das_04_0042:

Importing Data
==============

This section describes how to import data from your local PC or an OBS bucket for data backup and migration.

Usage Notes
-----------

-  Import data into a table for backup or migration. If you import a CSV or SQL file, the file must have the same data type as the target table.
-  Only one file that is no larger than 1 GB can be imported at a time.
-  Only data files in the CSV or SQL format can be imported. If the number of MySQL 8.0 instance tables exceeds 100,000 (more than 10,000 in MySQL 5.7 and 5.6), the CSV format cannot be used.
-  Binary fields such as BINARY, VARBINARY, TINYBLOB, BLOB, MEDIUMBLOB, and LONGBLOB are not supported.
-  The size of a single SQL statement to be imported must be less than 100 MB.
-  If a SQL file containing binary data is exported using the mysqldump tool, the file cannot be imported.
-  Only OBS buckets of the current IAM account can be imported.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Import and Export** > **Import**.

#. Click **Create Task**.

   .. table:: **Table 1** Parameter description

      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                          |
      +===================================+======================================================================================================================================================================================================================================================================+
      | Import Type                       | Set **Import Type** to **sql** or **CSV**.                                                                                                                                                                                                                           |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | File Source                       | Import a file from your local PC or an OBS bucket.                                                                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   | -  Upload file                                                                                                                                                                                                                                                       |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   |    If you select **Upload file** for **File Source**, you need to set **Attachment Storage** and upload the required file.                                                                                                                                           |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   |    To keep your data secure, provide your own OBS bucket to store the file you uploaded. In this way, DAS automatically connects to your OBS bucket for in-memory reading. No data is stored on DAS.                                                                 |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   |    Creating OBS buckets is free of charge, but saving files will incur certain costs.                                                                                                                                                                                |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   |    If you select **Delete the uploaded file upon an import success**, the file you uploaded will be automatically deleted from the OBS bucket after being imported to the destination database.                                                                      |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   | -  Choose from OBS                                                                                                                                                                                                                                                   |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   |    If you select **Choose from OBS** for **File Source**, you need to select a file from the bucket.                                                                                                                                                                 |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   |    The file uploaded from an OBS bucket will not be deleted upon an import success.                                                                                                                                                                                  |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Attachment Storage                | Select an OBS bucket to store the file. Click **Bucket ACL Info** to check whether a public OBS bucket is selected.                                                                                                                                                  |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   | -  **SAFE**: The bucket ACL permission set does not contain ALL USERS.                                                                                                                                                                                               |
      |                                   | -  **WARN**: The bucket ACL permission set contains ALL USERS.                                                                                                                                                                                                       |
      |                                   | -  **UNKNOWN**: The bucket ACL permission set is unknown, maybe due to the lack of IAM permissions. You are advised to go to the OBS page to view the bucket ACL configuration.                                                                                      |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Database                          | Select the database that you want to import the file to.                                                                                                                                                                                                             |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Charset                           | Select a charset as needed.                                                                                                                                                                                                                                          |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Options                           | If you select **Ignore errors, that is, skip the step where the SQL statement fails to be executed**, the system will skip any errors detected when SQL statements are being executed.                                                                               |
      |                                   |                                                                                                                                                                                                                                                                      |
      |                                   | If you select **Delete the uploaded file upon an import success**, the file you uploaded will be automatically deleted from the OBS bucket after being imported to the destination database. This option is only available to the files uploaded from your local PC. |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Remarks                           | Enter remarks as required.                                                                                                                                                                                                                                           |
      +-----------------------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. After setting import parameters, click **Create**.

   Confirm the information again before you click **OK** because original data may be overwritten after data import.

#. On the displayed page, view import progress in the task list.

   Click **Details** in the **Operation** column to view task details.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
