Catalog Source Configuration > Manage catalog sources > Managing configuration permissions for catalog sources

As a service administrator, you can grant configuration permissions for catalog sources to different roles in your organization, and add specific users and user groups to those roles so that they can perform operational activities on a catalog source.

To manage permissions for catalog source configuration, verify that at least one role has the catalog source configuration Set Permissions functionality enabled for Metadata Command Center in Administrator. In Administrator, create the required roles, assign users and user groups to the roles, and specify appropriate permissions to the roles.

You can select roles and add specific users or user groups to those roles to grant the following levels of permission for catalog source configuration:

* Create
* Read
* Update
* Run
* Set Permissions

Based on the permissions granted to the roles, the selected users and user groups belonging to that role can perform appropriate operations for configuring catalog sources.

1. Go to the Explore page in Metadata Command Center.
2. From the list of catalog sources, search for the catalog source for which you want to manage permissions.
3. Click the Action menu, and select Permissions.

The Catalog Source Permissions dialog box appears. The following image shows the Catalog Source Permissions dialog box:

![Image of the catalog source Permissions dialog box](https://onlinehelp.informatica.com/IICS/prod/MCC/en/metadata-command-center-catalog-source-configuration/images/GUID-9A30BA2B-7F01-44B2-9F4E-40532078D652-low.gif)

4. In the Roles panel, click Add Roles.

The Add Roles dialog box displays the list of roles that your organization administrator configured for Metadata Command Center. The following image shows the Add Roles dialog box:

![Image of the Add Roles dialog box](https://onlinehelp.informatica.com/IICS/prod/MCC/en/metadata-command-center-catalog-source-configuration/images/GUID-36902864-7C19-41F3-B3C4-DFD08F439876-low.gif)

5. Select one or more roles, and click OK to add the roles.
6. In the Add Users & User Groups panel, by default, all users and user groups that belong to the selected role are granted the role-defined permissions for the catalog source configuration. To assign permissions only to the selected users and user groups that belong to this role, choose Specific Users and User Groups.

The following image shows the Add Users & User Groups panel:

![Image of the Add Users and User Groups dialog box](https://onlinehelp.informatica.com/IICS/prod/MCC/en/metadata-command-center-catalog-source-configuration/images/GUID-97AC968D-4BC3-4130-A21A-973BA49F7EFD-low.gif)

7. Select Add Specific Users and User Groups.

The Add Users & User Groups dialog box displays the list of users and user groups that the administrator has assigned to the selected role.

8. Select one or more users or user groups to assign to the selected role, and click OK.

Only the selected users and user groups belonging to the specified role will be granted the role-defined permissions for catalog source configuration.

9. View the assigned permissions for each user and or group, and click Save.
