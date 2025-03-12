Use the following rules and guidelines for permissions:

* When you configure permissions on an object, verify that the user or group to which you grant permissions is assigned a role with the appropriate privileges for the object type.
* For example, if you grant a user with the Service Consumer role Update privilege on a particular folder, the user cannot update the folder because the Service Consumer role does not have update privileges for folders. 
* To edit an asset, the user must have read permission on all assets used within the asset. For example, when you assign a user Read and Update permissions on a synchronization task, verify that the user also has Read permission on the connections, mapplets, schedules, and saved queries that are used in the task.
* To run a subscription or a publication that executes a mapping task, the user must have the Update privilege for the project and folder that contains the mapping task.

* When a user edits a task, assets without Read permission are not displayed. To avoid unexpected results, the user should cancel all changes and avoid editing the task until the user is granted the appropriate Read permissions.
* When configuring a taskflow, a user needs Execute permission on all tasks to be added to the taskflow.
* To edit a taskflow, a user needs Execute permission on all tasks in the taskflow. Without Execute permission on all tasks, the user cannot save changes to the taskflow.
* To run a taskflow, a user needs Read and Execute permissions on taskflows.
* To monitor jobs or to stop a running job, a user needs Execute permission on the mapping, task, or taskflow.
* If you assign custom permissions to a Data Integration task and invoke the Data Integration task through an Application Integration process or a guide, you must complete either of the following tasks:
  - Give the Application Integration anonymous user permission to run the associated Data Integration asset.
  - Add the Application Integration anonymous user to a user group that has permission to run the associated Data Integration asset.
