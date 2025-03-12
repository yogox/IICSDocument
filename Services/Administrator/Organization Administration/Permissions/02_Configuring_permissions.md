You can configure permissions on an object if you are assigned a role with the Set Permission privilege for the object type. For example, to configure permissions on a folder, you must be assigned a role that has the Set Permission privilege for folders.

1. Navigate to the object for which you want to configure permissions.

For example:

- To configure permissions on a Secure Agent or Secure Agent group, in Administrator, select Runtime Environments.
- To configure permissions on a connection, in Administrator, select Connections.
- To configure permissions on a mapping, in Data Integration, open the project and folder that contain the mapping.

2. In the row that contains the object, either click Actions and select Permissions, or click the Change Permission icon.

The Permissions dialog box lists the users and groups that have permissions on the object.

If the Permissions dialog box lists no users or groups, then no permissions are configured for the object. Any user with appropriate privileges for the object type can access the object.

The following image shows the Permissions dialog box for a mapping:

![The Permissions dialog box lists the users and groups that have permissions on the object. Users and groups not listed have no permissions on the object. However, if the dialog box lists no users or groups, then there are no permission restrictions on the object.](https://onlinehelp.informatica.com/IICS/prod/admin/en/cc-iics-orgadmin/images/GUID-70E72987-F2E5-46BC-818D-7340B6903253-low.png)

3. To configure user permissions on the object:

   a. Select Users.
   
   b. If the user does not appear in the Users list, click Add, and select a user.
   
   c. Enable or disable the appropriate permissions on the user.

**Note:** When you grant any user permissions on the object, Informatica Intelligent Cloud Services also adds you as a user with permissions on the object. This prevents you from losing access to the object when you configure permissions.

4. To configure user group permissions on the object:

   a. Select Groups.
   
   b. If the group does not appear in the Groups list, click Add, and select a group.
   
   c. Enable or disable the appropriate permissions on the group.

**Note:** When you grant any group permissions on the object, Informatica Intelligent Cloud Services also adds you as a user with permissions on the object. This prevents you from losing access to the object when you configure permissions.

5. To remove all permissions restrictions for the object, remove all users and groups from the Permissions dialog box.

When you remove all users and groups, any user with appropriate privileges for the object type can access the object.

6. Click Save.
