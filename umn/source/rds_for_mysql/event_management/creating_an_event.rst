:original_name: das_04_0027.html

.. _das_04_0027:

Creating an Event
=================

This section describes how to create an event to periodically respond to specific operations.

If you set **event_scheduler** to **ON** and enable the event function, you can manage events.

When **event_scheduler** is set to **OFF**, but the event function is enabled, you can only create events and the events do not take effect.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane on the left, choose **Development Tool**.

#. Locate the DB instance that you want to log in to and click **Log In** in the **Operation** column.

#. On the top menu bar, choose **Database Management**.

#. Click **Change** on the right of the current database to switch to the database where you want to create a table.

#. On the **Objects** tab page, choose **Events**.

#. Click **Create Event**.

#. Enter an event name (mandatory) and event definition statements (mandatory), set the execution time, status, and comment, and click **Create**.

   -  **Event Definition Statements**

      Indicates the SQL statements to be executed when a scheduled event is triggered.

   -  **Dropped upon expiration**

      -  Indicates that the events to be executed at a fixed point in time will be deleted after they are executed.
      -  Indicates that the events to be periodically executed will be deleted at the specified end time.

#. In the displayed dialog box, click **Execute**.

   If there are no errors reported, the event takes effect.

.. |image1| image:: /_static/images/en-us_image_0000001694653209.png
.. |image2| image:: /_static/images/en-us_image_0000001694653201.png
