:original_name: das_20_0036.html

.. _das_20_0036:

GaussDB(for MySQL)
==================

#. Error message: **Access denied for user 'user_name'@'100.xxx.xx.xx' (using password: YES).**

   a. Error cause: The username or password of the GaussDB(for MySQL) DB instance is incorrect.

      Solution: Check whether the username and password are correct. If you are not sure, log in to the GaussDB(for MySQL) console to view the username and reset the password.

      .. important::

         Changing the password may affect services.

      If the username and password are correct, log in to the database using a client or CLI tool and run **select \* from mysql.user where user = 'user_name'** to view the account. Make sure that the DAS CIDR block is within the CIDR block of the user. **user_name @ %** and **user_name @100.%** are two different users whose passwords and permissions are independent. Make sure to enter the password of **user user_name @100.%**.

   b. Error cause: The IP address of the DAS server is not in the whitelist of the login user.

      Solution: Log in to the database using the client or CLI tool, and create a user that can be used to access the database through DAS.

      .. code-block::

         create user 'user_name'@'100.%' identified by 'password';
         grant all privileges on *.* to 'user_name'@'100.%';

      .. note::

         #. The IP address of the DAS server is in the 100.xxx.xx.xx network segment. Add the IP address to the whitelist of the login user.
         #. Grant permissions to user **user_name@100.%** based on service requirements.

#. Error message: **Communications link failure The last packet sent successfully to the server was 0 milliseconds ago. The driver has not received any packets from the server.**

   Error cause: The network between the DAS server and the GaussDB(for MySQL) DB instance is disconnected.

   Solution: Contact technical support.
