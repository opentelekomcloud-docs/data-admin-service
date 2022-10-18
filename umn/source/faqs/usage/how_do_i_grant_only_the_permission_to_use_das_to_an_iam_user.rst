:original_name: das_10_0030.html

.. _das_10_0030:

How Do I Grant Only the Permission to Use DAS to an IAM User?
=============================================================

#. Create a user-defined policy for DAS.

   On the management console, choose **Service List** > **Management & Governance** > **Identity and Access Management**. On the displayed page, select **Permissions** and click **Create Custom Policy**.

#. Select the rds:instance:list permission of RDS and das:connections:list permission of DAS.

   .. note::

      You can also select **JSON** for **Policy View** and enter the following statements in **Policy Content**.

      .. code-block:: text

         {
             "Version": "1.1",
             "Statement": [
                 {
                     "Action": [
                         "rds:instance:list"
                     ],
                     "Effect": "Allow"
                 },
                 {
                     "Action": [
                         "das:connections:list"
                     ],
                     "Effect": "Allow"
                 }
             ]
         }

#. Create a DAS user group. Then, click **Manage Permissions** in the **Operation** column to select the custom permissions.

#. Create an IAM user and add it to the user group.
