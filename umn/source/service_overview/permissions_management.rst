:original_name: das_01_0012.html

.. _das_01_0012:

Permissions Management
======================

If you need to assign different permissions to different employees in your enterprise to access your DAS resources, Identity and Access Management (IAM) is a good choice for fine-grained permissions management. IAM provides identity authentication, permissions management, and access control for your cloud resources.

With IAM, you can use your account to create IAM users, and assign permissions to the users to control their access to specific resources. For example, if you need software developers in your enterprise to be able to use DAS but not able to delete DAS resources or perform any high-risk operations, you can create IAM users for the developers and grant them only the permissions required for using DAS resources.

If your account does not require individual IAM users for permissions management, you can skip this section.

DAS Permissions
---------------

By default, new IAM users do not have any permissions assigned. You need to add a user to one or more groups and attach permissions policies or roles to these groups. Users then inherit permissions from the groups they belong to and can perform specified operations on cloud services.

DAS is a project-level service deployed in specific physical regions. To assign DAS permissions to a user group, specify projects in specific regions where the permissions will take effect. If you select **All projects**, the permissions will be granted to the user group in all projects. When accessing DAS, you need to switch to a region where you have been authorized to use this service.

You can grant users permissions by using roles and policies.

-  Roles: A type of coarse-grained authorization system that defines permissions related to users responsibilities. Only a limited number of service-level roles are available for authorization. When using roles to grant permissions, you may need to also assign other roles that the permissions depend on. Roles are not ideal for fine-grained authorization and secure access control.

-  Policies: A type of fine-grained authorization system that defines permissions required to perform operations on specific cloud resources under certain conditions. Policies are more flexible than roles, and they can ensure more secure access control. For example, you can grant IAM users only permissions for managing a certain type of database resource.

:ref:`Table 1 <das_01_0012__table739818105539>` lists all the system-defined roles and policies supported by DAS.

.. _das_01_0012__table739818105539:

.. table:: **Table 1** DAS system permissions

   +-------------------+------------------------------------------------------+-----------------------+--------------------------------------------------------------------------------------------+
   | Policy Name       | Description                                          | Type                  | Dependency                                                                                 |
   +===================+======================================================+=======================+============================================================================================+
   | DAS Administrator | DAS administrator, who has full permissions for DAS. | System-defined role   | This role depends on the **Tenant Guest** role.                                            |
   |                   |                                                      |                       |                                                                                            |
   |                   |                                                      |                       | The **DAS Administrator** and **Tenant Guest** roles must be assigned in the same project. |
   +-------------------+------------------------------------------------------+-----------------------+--------------------------------------------------------------------------------------------+
   | DAS FullAccess    | Full permissions for DAS                             | System-defined policy | None                                                                                       |
   +-------------------+------------------------------------------------------+-----------------------+--------------------------------------------------------------------------------------------+

.. note::

   -  DAS depends on other services to manage databases.
   -  If you authorize IAM users in fine-grained mode and want to use DAS to manage DB instances, add the DAS FullAccess system policy during authorization.
   -  On the DAS console, you can view and manage the instances configured in the corresponding services.

By default, users with fine-grained authorization have permissions to view and delete database connections on the **Development Tool** page on DAS. The instances are the same as those configured for related services.

:ref:`Table 2 <das_01_0012__table43871018105520>` describes the common operations supported by each system-defined policy or role of DAS. Select the policy or role you need based on the following tables.

.. _das_01_0012__table43871018105520:

.. table:: **Table 2** Common operations supported by each system-defined policy or role of DAS

   +--------------------------------------------+-------------------+----------------+
   | Operation                                  | DAS Administrator | DAS FullAccess |
   +============================================+===================+================+
   | Logging in to a database                   | Supported         | Supported      |
   +--------------------------------------------+-------------------+----------------+
   | Adding a database connection               | Supported         | Supported      |
   +--------------------------------------------+-------------------+----------------+
   | Modifying a database connection            | Supported         | Supported      |
   +--------------------------------------------+-------------------+----------------+
   | Deleting a DB instance connection          | Supported         | Supported      |
   +--------------------------------------------+-------------------+----------------+
   | Viewing the login list in Development Tool | Supported         | Supported      |
   +--------------------------------------------+-------------------+----------------+

.. table:: **Table 3** Common DAS operations and supported actions

   +--------------------------------------+------------------------+--------------------------------------------------------------------------------------------------+
   | Operation                            | Action                 | Remarks                                                                                          |
   +======================================+========================+==================================================================================================+
   | Logging in to a database             | das:connections:login  | Configure the permissions required to query other database instances based on the instance type. |
   |                                      |                        |                                                                                                  |
   |                                      |                        | -  rds:instance:list;                                                                            |
   |                                      |                        | -  dds:instance:list;                                                                            |
   |                                      |                        | -  gaussdb:instance:list;                                                                        |
   +--------------------------------------+------------------------+--------------------------------------------------------------------------------------------------+
   | Obtaining the login information list | das:connections:list   | Configure the permissions required to query other database instances based on the instance type. |
   |                                      |                        |                                                                                                  |
   |                                      |                        | -  rds:instance:list;                                                                            |
   |                                      |                        | -  dds:instance:list;                                                                            |
   |                                      |                        | -  gaussdb:instance:list;                                                                        |
   +--------------------------------------+------------------------+--------------------------------------------------------------------------------------------------+
   | Deleting login information           | das:connections:delete | Configure the permissions required to query other database instances based on the instance type. |
   |                                      |                        |                                                                                                  |
   |                                      |                        | -  rds:instance:list;                                                                            |
   |                                      |                        | -  dds:instance:list;                                                                            |
   |                                      |                        | -  gaussdb:instance:list;                                                                        |
   +--------------------------------------+------------------------+--------------------------------------------------------------------------------------------------+
   | Adding a database connection         | das:connections:create | Configure the permissions required to query other database instances based on the instance type. |
   |                                      |                        |                                                                                                  |
   |                                      |                        | -  rds:instance:list;                                                                            |
   |                                      |                        | -  dds:instance:list;                                                                            |
   |                                      |                        | -  gaussdb:instance:list;                                                                        |
   +--------------------------------------+------------------------+--------------------------------------------------------------------------------------------------+
   | Modifying a database connection      | das:connections:modify | Configure the permissions required to query other database instances based on the instance type. |
   |                                      |                        |                                                                                                  |
   |                                      |                        | -  rds:instance:list;                                                                            |
   |                                      |                        | -  dds:instance:list;                                                                            |
   |                                      |                        | -  gaussdb:instance:list;                                                                        |
   +--------------------------------------+------------------------+--------------------------------------------------------------------------------------------------+

.. table:: **Table 4** Other permissions DAS depends on

   +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+-----------------+
   | Policy Name          | Description                                                                                                                                                                                                          | Type                  | Dependency      |
   +======================+======================================================================================================================================================================================================================+=======================+=================+
   | Tenant Administrator | Operation permissions:                                                                                                                                                                                               | System-defined role   | None            |
   |                      |                                                                                                                                                                                                                      |                       |                 |
   |                      | -  All permissions on the account center, billing center, and resource center                                                                                                                                        |                       |                 |
   |                      | -  All permissions on cloud resources owned by the account                                                                                                                                                           |                       |                 |
   |                      |                                                                                                                                                                                                                      |                       |                 |
   |                      | OBS policies are configured in the Global project.                                                                                                                                                                   |                       |                 |
   +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+-----------------+
   | OBS OperateAccess    | Operation permissions: Users with this permission can view buckets, obtain basic bucket information, obtain bucket metadata, view objects, upload objects, download objects, delete objects, and obtain object ACLs. | System-defined policy | None            |
   |                      |                                                                                                                                                                                                                      |                       |                 |
   |                      | Configure the OBS policies globally.                                                                                                                                                                                 |                       |                 |
   +----------------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+-----------------+

DAS import and export features require the usage of OBS buckets. You need to obtain required OBS permissions before using these features.

-  Typically, it is recommended that you configure the Tenant Administrator policy that allows you to perform operations on OBS resources.
-  If you do not want employees to have the permissions for creating and deleting buckets, you can configure the OBS OperateAccess policy for the employees so that they can use the DAS features but cannot create or delete OBS buckets.
