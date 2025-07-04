:original_name: das_20_0003.html

.. _das_20_0003:

Viewing Traces
==============

Scenarios
---------

After CTS is enabled, the tracker starts recording operations on cloud resources. The last 7 days of operation records are stored on the CTS console.

This section describes how to query the last 7 days of operation records on the CTS console.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner. Choose **Management & Governance** > **Cloud Trace Service**.

#. Choose **Trace List** in the navigation pane on the left.

#. Specify filter criteria to search for the required traces. The following filters are available:

   -  **Trace Source**, **Resource Type**, and **Search By**: Select a filter from the drop-down list.

      When you select **Resource ID** for **Search By**, you also need to select or enter a resource ID.

   -  **Operator**: Select a specific operator from the drop-down list.

   -  **Trace Status**: Available options include **All trace statuses**, **Normal**, **Warning**, and **Incident**. You can only select one of them.

   -  Time range: In the upper right corner of the page, specify a time range for querying traces.

#. Click **Query**.

#. Locate the required trace and click |image2| on the left of the trace to view its details.

#. Click **View Trace** in the **Operation** column. In the displayed dialog box, the trace structure details are displayed.

#. Click **Export** in the upper right corner of the trace list, and CTS exports traces collected in the past 7 days to a CSV file.

   For details about key fields in the trace structure, see sections "Trace Structure" and "Trace Examples" in the *Cloud Trace Service User Guide*.

.. |image1| image:: /_static/images/en-us_image_0000002302923710.png
.. |image2| image:: /_static/images/en-us_image_0000001694652861.png
