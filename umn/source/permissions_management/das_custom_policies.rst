:original_name: das_08_0004.html

.. _das_08_0004:

DAS Custom Policies
===================

Custom policies can be created to supplement the system-defined policies of DAS.

There are two ways to create custom policies:

-  Visual editor: Select cloud services, actions, resources, and request conditions. This does not require knowledge of policy syntax.
-  JSON: Edit JSON policies from scratch or based on an existing policy.

. This section describes example custom policies of DAS.

Examples of DAS Custom Policies
-------------------------------

Example 1: Assign only DAS permissions.

.. code-block:: text

   {
       "Version": "1.1",
       "Statement": [
           {
               "Action": [
                   "das:*:*"
               ],
               "Effect": "Allow"
           }
       ]
   }
