# Permissions

Permissions determine the access rights that a user has for a Secure Agent, Secure Agent group, connection, schedule, or asset. Permissions add additional or custom security for an object. Permissions define which users and groups can read, update, delete, execute, and change permissions on the object.

The role assigned to your user account or to a group in which you are a member must have the Set Permission privilege for the object type. For example, to configure permissions on a Secure Agent, you must be assigned a role that has the Set Permission privilege for Secure Agents.

To configure permissions on an object, navigate to the object and set the appropriate permissions. For example, you want only users in the Development Team user group to have access to assets in the Development Data folder. Navigate to the folder, edit the permissions, and grant the Development Team user group permissions on the folder.

Permissions apply to the objects that you configure but not to copies of the object. Therefore, when you copy or export an asset, the permissions are not copied or exported with the asset. For example, you export a mapping task in which only user rjones has execute permission. When you import the mapping task, the imported mapping has no permissions assigned to it. Therefore, any user with privileges to run mapping tasks can run the imported task.

You can configure the following permissions on an object:

| Permission | Description |
| --- | --- |
| Read | Open and view the object.<br>If the object is source controlled, this permission allows the user or group to pull or check out the object from the source control repository. You must have the read permission to access the integration hub connection to perform any operations.<br>If you select a task, this permission also allows the user or group to use a connection or schedule in the task. |
| Update | Edit the object.<br>If the object is source controlled, this permission allows the user or group to check in, check out, pull, unlink, or roll back the object.<br>Requires read permission, which is automatically granted. |
| Delete | Delete the object. |
| Execute | Run the object.<br>Applies to mappings, tasks, taskflows, and Cloud Integration Hub assets. Monitor, stop, and restart instances of the mapping, task, or taskflow. |
| Change permissions | Change the permissions that are assigned to the object. |

**Note:** These permissions control permissions within Informatica Intelligent Cloud Services. They do not control operating system permissions, such as the ability to start, stop, or configure the Secure Agent on Windows or Linux.
