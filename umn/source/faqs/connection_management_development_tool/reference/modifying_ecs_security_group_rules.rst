:original_name: das_20_0028.html

.. _das_20_0028:

Modifying ECS Security Group Rules
==================================

#. On the ECS details page, click the **Security Groups** tab and view security group rules. To enable DAS to access the self-built DB instances on ECSs, you need to add an inbound rule with the port set to 3306 (example) and source to 100.0.0.0/8.


   .. figure:: /_static/images/en-us_image_0000001387792145.png
      :alt: **Figure 1** Security group rules


      **Figure 1** Security group rules

#. Click **Manage Rule** on the left. On the **Inbound Rules** tab page, click **Add Inbound Rule**.


   .. figure:: /_static/images/en-us_image_0000001388031793.png
      :alt: **Figure 2** Adding an inbound rule


      **Figure 2** Adding an inbound rule

   .. note::

      Recommended configuration: Select **TCP** for **Protocol & Port**, enter the port number of the self-built database, and set the source to 100.0.0.0/8 or 0.0.0.0/0.

#. On the **Outbound Rules** tab page, click **Add Outbound Rule**.


   .. figure:: /_static/images/en-us_image_0000001337591748.png
      :alt: **Figure 3** Adding an outbound rule


      **Figure 3** Adding an outbound rule

   .. note::

      Recommended configuration: Select **TCP** for **Protocol & Port**, enter the port number of the self-built database, and set the source to 100.0.0.0/8 or 0.0.0.0/0.
