:original_name: das_03_0016.html

.. _das_03_0016:

Emergency Channel
=================

Scenarios
---------

-  Emergency Channel

   -  If the maximum number of sessions for an instance has been reached and the instance cannot be logged in to, you can view and kill unnecessary sessions through the emergency channel.
   -  Emergency channel is available to only RDS MySQL and GaussDB(for MySQL) DB databases currently, but not to self-built databases on ECSs and instances in the creating, frozen, or abnormal state.
   -  Use this function in urgent conditions. All your kill operations will be recorded in logs.
   -  If your instance can be logged in to on the DAS console, log in to the instance and perform desired operations through **Real-Time Sessions**.
   -  Sessions of sensitive users, like rdsadmin, rdsbackup, rdsmetric, and rdsRepl cannot be killed.

-  History Logs

   On the **History Logs** tab page, you can view all your sessions killed through the emergency channel.

Prerequisites
-------------

The DB engine must be MySQL. The MySQL 5.6 version must be 5.6.43.3 or later, and MySQL 5.7 version must be 5.7.25.3 or later.

Procedure
---------

#. Log in to the DAS console using your username and password.
#. On the **Overview** page, click **Go to Intelligent O&M**.
#. Locate your desired instance and click **Details** to go to the Intelligent O&M overview page.
#. On the **Emergency Channel** tab page, select the sessions you want to kill. By default, the sessions are sorted in descending order by session duration.
#. Click **Kill**. In the displayed dialog box, click **Yes**.
#. On the **History Logs** tab page, view your sessions killed through the emergency channel.
