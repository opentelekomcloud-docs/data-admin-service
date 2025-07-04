:original_name: das_01_2110.html

.. _das_01_2110:

Enabling Multifactor Authentication for Critical Operations
===========================================================

This section describes how to enable and use multifactor authentication for critical operations.

Procedure
---------

#. Log in to the OTC console.

#. Click |image1| in the upper left corner and select a region and project.

#. Click |image2| in the upper left corner, and under **Databases**, click **Data Admin Service**.

#. In the navigation pane, choose **Development Tool**.

#. On the **Development Tool** page, enable **Multifactor Authentication for Critical Operations**.


   .. figure:: /_static/images/en-us_image_0000002346986173.png
      :alt: **Figure 1** Enabling the function

      **Figure 1** Enabling the function

   When you hover the pointer over the switch, its function description is displayed. This switch is available only for your domain account.


   .. figure:: /_static/images/en-us_image_0000002313027352.png
      :alt: **Figure 2** Modifying the switch

      **Figure 2** Modifying the switch

#. Follow the on-screen instructions to enable operation protection. Multifactor authentication for critical operations takes effect only when both **Multifactor Authentication for Critical Operations** on DAS and **Operation Protection** for critical operations on IAM are enabled.


   .. figure:: /_static/images/en-us_image_0000002346946481.png
      :alt: **Figure 3** Operation protection

      **Figure 3** Operation protection

#. After this function is enabled, you will be authenticated when logging in to a DB instance from Development Tool on DAS.


   .. figure:: /_static/images/en-us_image_0000002305313278.png
      :alt: **Figure 4** Confirm

      **Figure 4** Confirm

   If this function is not required, disable it on the **Development Tool** page of DAS.

.. |image1| image:: /_static/images/en-us_image_0000002305317006.png
.. |image2| image:: /_static/images/en-us_image_0000002305157322.png
