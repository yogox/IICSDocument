# Access policies

Access policies are sets of rules that you use to define permissions and control the level of access to organizational assets.

To implement access control, you can use predefined access policies or define custom access policies in Metadata Command Center. Predefined access policies are associated with predefined user roles defined in Administrator. For information about predefined access policies, see Introduction and Getting Started.

To define access policies, you create rules that provide specific permissions and privileges to users or user groups on asset types or attribute groups. The access policies control the level of access that users have based on the assigned user role, stakeholder role, or the user group.

The following table describes the access policies that you can create in Metadata Command Center:

| Access policy | Description |
|---------------|-------------|
| User role policy | Defines the access level of users who are assigned a user role in Administrator. |
| Stakeholder role policy | Defines the access level of users who are assigned a stakeholder role. A stakeholder role policy is only applicable for assets that have a user with a stakeholder role assigned. For information about how to create a stakeholder role, see Creating a stakeholder role. |
| User group policy | Defines the access level of users who are assigned a user group in Administrator. You can also use this access policy to control the access level to all users in the organization. |

The following image shows the Access Policies tab with a list of access policies: ![The image shows the Access Policies tab with a list of access policies.](https://onlinehelp.informatica.com/IICS/prod/MCC/en/metadata-command-center-administration/images/GUID-4EC64FC7-CFBC-405F-A8EF-8CC256DFBD31-low.png)

### How access policies work

Users inherit the intersection of the permissions granted by all the assigned access policies.

For example, if a user has the following access policies, then only the intersection of those permissions are granted to the user on the asset:

• User role policy for the Governance Owner
• Stakeholder role policy for the Governance Owner
• User group policy for the Finance user group

When you create a user role or stakeholder role policy and override other access policy types, then this access policy provides access regardless of other access policies that might apply.

### Access policies to work with catalog sources

To work with catalog sources, the administrator needs to configure asset privileges for the Catalog Source Configuration asset for the user role in Administrator. Also, the administrator needs to configure an access policy with the required permissions in Metadata Command Center.

The following table describes the privileges and permissions required to perform certain actions:

| Action | User role privilege | Access policy permission |
|--------|---------------------|--------------------------|
| Create a catalog source | create, read, update | create, read |
| View the catalog source configuration | read | read |
| Purge a catalog source | read, delete | delete |
| Copy a catalog source | create, read, update | create, read |
| Update a catalog source | read, update | update |

To run a catalog source job, you need to grant the following permissions:

• For a catalog source that does not have connection assignments, grant the read permission to the user role.
• For a catalog source that has connection assignments, grant the read and update permissions on the reference catalog source and the endpoint catalog source to the user role, stakeholder role, and non-stakeholders.
