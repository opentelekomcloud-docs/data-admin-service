:original_name: das_20_0100.html

.. _das_20_0100:

RDS DB Instances
================

#. Error message: **Access denied for user 'user_name'@'100.xxx.xx.xx' (using password: YES)**

   a. Error cause: The username or password of the RDS DB instance is incorrect.

      Solution: Check whether the username and password are correct. If you are not sure, log in to the RDS console to reset the password.

      .. important::

         Changing the password may affect services.

      If the username and password are correct, log in to the database using a client or CLI tool and run **select \* from mysql.user where user = 'user_name'** to view the account. Make sure that the DAS CIDR block is within the CIDR block of the user. **user_name @ %** and **user_name @100.%** are two different users whose passwords and permissions are independent. Enter the password of **user user_name @100.%**.

   b. Error cause: The IP address of the DAS server is not in the whitelist of the login user.

      Solution: Log in to the database using the client or CLI tool, and create a user account that can be used to access the database through DAS.

      .. code-block::

         create user 'user_name'@'100.%' identified by 'password';
         grant selete on *.* to 'user_name'@'100.%';

      .. note::

         -  The IP address of the DAS server is in the 100.xxx.xx.xx network segment. Add the IP address to the whitelist of the login user.
         -  Grant permissions to user **user_name@100.%** based on service requirements.

   c. Error cause: The SSL function is not enabled on the server.

      Solution: Run the following statement to check whether the user is an SSL user. If yes, enable SSL on the RDS DB instance details page. The user is an SSL user if the **ssl_type** field has a value.

      .. code-block::

         select user, host, ssl_type from mysql.user where user = 'user_name';

2. Error message: **Communications link failure The last packet sent successfully to the server was 0 milliseconds ago. The driver has not received any packets from the server**

Error cause: The network between the DAS server and the RDS DB instance is disconnected.

Solution: Contact technical support.
