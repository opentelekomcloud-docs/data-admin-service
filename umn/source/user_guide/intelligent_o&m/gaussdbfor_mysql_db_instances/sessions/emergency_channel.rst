:original_name: das_05_0016.html

.. _das_05_0016:

Emergency Channel
=================

Scenarios
---------

-  Emergency Channel

   -  If the maximum number of sessions for an instance has been reached and the instance cannot be logged in to, you can view and kill unnecessary sessions through the emergency channel.
   -  Emergency channel is available to only RDS MySQL and GaussDB(for MySQL) instances currently, but not to self-built DB instances on ECSs and instances in the creating, frozen, or abnormal state.
   -  Do not kill sessions unless you really need to. All your kill operations will be logged.
   -  If your instance can be logged in to on the DAS console, log in to the instance and perform the required operations through **Real-Time Sessions**.
   -  Sessions of sensitive users such as **rdsadmin**, **rdsbackup**, **rdsmetric**, and **rdsRepl** cannot be killed.

-  History Logs

   On the **History Logs** tab page, you can view all your sessions killed through the emergency channel.

Prerequisites
-------------

The DB engine must be MySQL. The MySQL 5.6 version must be 5.6.43.3 or later, and MySQL 5.7 version must be 5.7.25.3 or later.

Procedure
---------

#. Log in to the DAS console using your username and password.
#. On the **Overview** page, click **Go to Intelligent O&M**.
#. Select the required instance and click **Details** to go to the Intelligent O&M overview page.
#. Choose **Sessions** > **Emergency Channel**, and select the sessions you want to kill. Sessions are sorted in descending order by duration.
#. Click **Kill**. In the displayed dialog box, click **Yes**.
#. Click **History Logs** to view the sessions killed through the emergency channel.
