:original_name: das_20_0035.html

.. _das_20_0035:

DDS
===

#. Error message: Command failed with error 18 (AuthenticationFailed): 'Authentication failed.' on server xxx.xxx.xx.xx:xxxx. The full response is { 'ok' : 0.0, 'errmsg' : "Authentication failed.", "code" : 18, "codeName" : "AuthenticationFailed" }

   a. Error cause: The username or password of the DDS DB instance is incorrect.

      Solution: Check whether the username or password is correct. If you are not sure, view the username or reset the password on the DDS console.

      .. important::

         Changing the password may affect services.

   b. Error cause: The entered username does not have the permission to access the database.

      Solution: Check whether the username has the permission to access the database. If you are not sure, connect to the admin database as user **rwuser**. Then check whether the entered username has the required permission.
