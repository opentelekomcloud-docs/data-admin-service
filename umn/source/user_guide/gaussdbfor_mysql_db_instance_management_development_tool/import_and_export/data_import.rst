:original_name: das_13_0048.html

.. _das_13_0048:

Data Import
===========

Scenarios
---------

Import data into a table for backup or data migration. The table structure to be imported must be the same as that of the target table. If you import a CSV or SQL file, the data type of the target table must be the same. The imported file should be no larger than 10 GB.

Procedure
---------

#. On the top menu bar, choose **Import and Export** > **Import**.

#. Import a file from your local PC or an OBS bucket.

   -  From your local PC

   In the upper left corner, click **Create Task**. On the displayed page, select an import type, select **Upload file** for **File Source**, set the attachment storage, and upload the file. Then, set other parameters as required.

   For security purposes, imported files are stored in OBS buckets.

   .. note::

      -  To keep your data secure, provide your own OBS bucket to store the attachments you upload. In this way, DAS automatically connects to your OBS bucket for in-memory reading.
      -  If you select **Delete the uploaded file upon an import success**, the file you upload will be automatically deleted from the OBS bucket after being imported to the destination database.

   -  From an OBS bucket

      In the upper left corner, click **Create Task**. On the displayed page, select an import type, select **Choose from OBS** for **File Source**, and select a file from the bucket. Then, set other parameters as required.

   .. note::

      The file uploaded from an OBS bucket will not be deleted upon an import success.

#. After setting the import parameters, click **Create**. Confirm the information again before you click **OK** because original data may be overwritten after data import.

#. View the import progress in the task list or check task details.
