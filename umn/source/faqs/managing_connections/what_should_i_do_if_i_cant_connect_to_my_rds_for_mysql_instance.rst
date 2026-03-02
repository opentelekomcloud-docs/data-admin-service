:original_name: das_10_0014.html

.. _das_10_0014:

What Should I Do If I Can't Connect to My RDS for MySQL Instance?
=================================================================

#. Error message: **Access denied for user 'user_name'@'100.xxx.xx.xx' (using password: YES)**

   a. Error cause: The username or password of the RDS instance is incorrect.

      Solution: Check whether the username and password are correct. If you are not sure, log in to the RDS console to reset the password.

      .. important::

         Changing the password may affect services.

      If the username and password are correct, log in to the database using a client or CLI and run **select \* from mysql.user where user = 'user_name'** to view the account. If **100.**\ *xxx*\ **.**\ *xxx*\ **.**\ *xxx* is assigned to a user, only the user can connect to the database through DAS. **user_name @%** and **user_name @100.%** are different users with independent passwords and permissions. Enter the password of **user_name @100.%**.

   b. Error cause: The IP address of the DAS server is not in the whitelist of the login user.

      Solution: Log in to the database using the client or CLI, and create a user that can be used to access the database through DAS.

      .. code-block::

         create user 'user_name'@'100.%' identified by 'password';
         grant select on *.* to 'user_name'@'100.%';

      .. note::

         -  Ensure that the IP address of the DAS server is in a CIDR block starting with 100. Add the IP address to the whitelist of the login user.
         -  Grant permissions to user **user_name@100.%** based on service requirements.

   c. Error cause: The SSL function is not enabled on the server.

      Solution: Run the following statement to check whether the user is an SSL user. If yes, enable SSL on the RDS instance details page. The user is an SSL user if the **ssl_type** field has a value.

      .. code-block::

         select user, host, ssl_type from mysql.user where user = 'user_name';

#. Error message: **Trying to connect with ssl, but ssl not enabled in the server**

   Error cause: The SSL function is not enabled on the server.

   Solution: Run the following statement to check whether the user is an SSL user. If yes, enable SSL on the RDS instance details page. The user is an SSL user if the **ssl_type** field has a value.

   .. code-block::

      select user, host, ssl_type from mysql.user where user = 'user_name';

#. Error message: **Client does not support authentication protocol requested by server.** plugin type was = 'sha256_password'.

   a. Error cause: DAS does not allow you to connect to the database whose password is encrypted with SHA-256.

      Solution: Execute the following SQL statements to change the password encryption method to mysql_native_password.

      .. code-block::

         alter user 'user_name'@'%' identified with mysql_native_password by 'password';

   b. Error cause: For MySQL 8.0, the IP address of the DAS server is not in the whitelist of the user.

      Solution: Log in to the database using the client or CLI, and create a user that can be used to access the database through DAS.

#. Error message: **Communications link failure The last packet sent successfully to the server was 0 milliseconds ago.** The driver has not received any packets from the server.

   Error cause: The network between the DAS server and the target instance is disconnected.

   Solution: Contact technical support.

#. Error message: **Instance connect timeout, please login again**

   Error cause: The connection to the DAS server timed out.

   Solution: Contact technical support.

#. Error information: **RSA public key is not available client side (option serverRsaPublicKeyFile not set).**

   Error cause: The identity authentication mode of the database user has high requirements on password security. The password transmitted over the network during user authentication must be encrypted.

   -  The SSL certificate's key pair is used during TLS handshake. After that, a symmetric key is generated and is used to encrypt the password and data.
   -  For a non-SSL encrypted connection, the client uses the RSA public key of the MySQL server to encrypt the user password, and the server uses the RSA private key to decrypt and verify the password. This protects the password against snooping during network transmission.

   Solution: Enable SSL for the instance or change the identity authentication mode of the database user.
