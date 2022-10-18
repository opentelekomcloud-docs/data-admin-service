:original_name: das_04_0027.html

.. _das_04_0027:

Creating an Event
=================

Scenarios
---------

This section describes how to create an event to periodically respond to specific operations.

When **event_scheduler** for RDS DB instances is set to **ON** and the event function is enabled, you can perform operations on events.

When **event_scheduler** is set to **OFF**, but the event function is enabled, you can only create events and the events do not take effect.

Procedure
---------

#. On the top menu bar, choose **Database Management**. On the displayed **Objects** page, select **Events**, and click **Create Event**.
#. Specify an event name (mandatory) and event definition statements (mandatory), set the execution time, status, and comment, and click **Create**.

   -  **Event Definition Statements**

      Indicates the SQL statements to be executed when a scheduled event is triggered.

   -  **Dropped upon expiration**

      -  Indicates that the events to be executed at a fixed point in time will be deleted after they are executed.
      -  Indicates that the events to be periodically executed will be deleted at the specified end time.

#. In the displayed dialog box, click **Execute**. If no error is reported, the event takes effect.
