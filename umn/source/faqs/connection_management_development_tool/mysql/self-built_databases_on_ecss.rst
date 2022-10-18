:original_name: das_20_0101.html

.. _das_20_0101:

Self-Built Databases on ECSs
============================

#. Error message: **Access denied for user 'user_name'@'100.xxx.xx.xx' (using password: YES)**

   a. Error cause: The username or password of the self-built database on the ECS is incorrect.

      Solution: Ensure that the username and password are correct. If the username and password are correct, log in to the database using a client or the CLI tool and run **select \* from mysql.user where user = 'user_name'** to view the account. Make sure that the DAS CIDR block is within the CIDR block of the user. **user_name @ %** and **user_name @100.%** are two different users whose passwords and permissions are independent. Enter the password of **user user_name @100.%**.

   b. Error cause: The IP address of the DAS server is not in the whitelist of the login user.

      Solution: Log in to the database using the client or CLI tool, and create a user account that can be used to access the database through DAS.

      .. code-block::

         create user 'user_name'@'100.%' identified by 'password';
         grant all privileges on *.* to 'user_name'@'100.%';

      .. note::

         -  The IP address of the DAS server is in the 100.xxx.xx.xx network segment. Add the IP address to the whitelist of the login user.
         -  Grant permissions to user **user_name@100.%** based on service requirements.

   c. Error cause: The SSL function is not enabled on the server.

      Solution: Run the following statement to check whether the user is an SSL user. If yes, enable SSL on the RDS DB instance details page. The user is an SSL user if the **ssl_type** field has a value.

      .. code-block::

         select user, host, ssl_type from mysql.user where user = 'user_name';

#. Error message: **Host 'xxx.xxx.xx.xx' is not allowed to connect to this MySQL server**

   Error cause: The database username you entered does not support remote login. For example, if you enter username **root**, but only username **root@localhost** is configured in the **mysql.user** table, the specified user can only log in locally.

   Solution: Use a client or CLI tool to log in to the self-built database and create a user account that supports remote login.

   .. code-block::

      create user 'user_name'@'100.%' identified by 'password';
      grant all privileges on *.* to 'user_name'@'100.%';

   .. note::

      -  The IP address of the DAS server is in the 100.xxx.xx.xx network segment. Add the IP address to the whitelist of the login user.
      -  Grant permissions to user **user_name@100.%** based on service requirements.

#. Error message: **Communications link failure The last packet sent successfully to the server was 0 milliseconds ago. The driver has not received any packets from the server.**

   a. Error cause: The security group rules do not allow inbound traffic on the port.

      Solution: Modify the security group rules by referring to :ref:`Modifying ECS Security Group Rules <das_20_0028>`.

   b. Error cause: The firewall policy does not allow inbound traffic on the port.

      Solution: Modify the firewall policy by referring to :ref:`Modifying Firewall Rules <das_20_0029>`.

   c. Error cause: The remote login times out because the DNS resolution takes a long period of time.

      Solution: Perform the following steps:

#. Search for the configuration file of the self-built database in directory **/etc/my.cn**, enter the following content in **[mysqld]**, save and exit.

   .. code-block::

      skip-name-resolve

   |image1|

   .. note::

      The default location of the configuration file is **/etc/my.cnf**. If you store the file in the specified path, modify the directory accordingly.

#. Run **systemctl restart mysqld** to restart the database and log in again.

.. |image1| image:: /_static/images/en-us_image_0000001337431632.png
