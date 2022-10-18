:original_name: das_13_0023.html

.. _das_13_0023:

Creating an Event
=================

Scenarios
---------

-  Create an event to periodically response to specific operations on databases.
-  When **event_scheduler** of an RDS DB instance is set to **ON**, and the event function is enabled, you can manage events. When **event_scheduler** is set to **OFF**, but the event function is enabled, you can only create events and the events do not take effect.

Procedure
---------

#. On the top menu bar, choose **Database Management**. On the displayed **Objects** page, select **Events**, and click **Create Event**.
#. Specify an event name (mandatory) and event definition statements (mandatory), set the execution time, status, and comment, and click **Create**.

   -  **Event Definition Statements**

      Indicates the SQL statements to be executed when a scheduled event is triggered.

   -  **Dropped upon expiration**

      Indicates that the event to be executed at a fixed time will be deleted after it is executed and the event to be executed in a scheduled cycle will be deleted at the specified time.

#. In the displayed dialog box, click **Execute**. If no error is reported, the event takes effect.
