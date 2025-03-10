# Key concepts

To understand how your administrators can manage access to assets using metadata acccess control, you need a basic understanding of the following key concepts.

## Roles, users, and user groups

To use Data Governance and Catalog, the organization administrator must create the users, user groups, and user roles in Administrator for your organization.

A user is an individual Informatica Intelligent Cloud Services account that can perform tasks and access assets based on the roles that are assigned to the user. You can assign roles directly to the user or to a group that the user is a member of. Administrators can create user accounts for the organization in Administrator.

A user group is a group of users who can perform tasks and access assets based on the roles that you assign to the group. Administrators can create user groups for the organization in Administrator.

A role is a set of privileges that you can assign to users and user groups. When the organization administrator creates roles and sets the correct permissions and privileges, the roles define the boundaries within which the users can act. Data Governance and Catalog provides three predefined user roles that you can assign to users and user groups in Administrator. See Predefined user roles.To create custom roles, you can create a new role or clone an existing custom role in the Administrator.

With metadata access control, there are two types of roles that administrators can use to grant different types of access to users.

### User roles

A user role defines the permissions and privileges for different types of assets and features. Administrators can create and assign user roles for the organization in Administrator. You can assign a user role to the users or user groups in your organization.

The user roles that the organization administrator creates for your organization appear on the Users tab on the Access Control page in Metadata Command Center. You can use the user roles in access policies to grant users access and permissions for different types of assets.

For more information about creating user roles and assigning them to users and user groups, see User Administration in Administrator.

### Stakeholder roles

A stakeholder role is a defined organizational responsibility that you declare on assets. Stakeholder roles allow you to control how authorized users interact with the assets for which they are responsible.

A stakeholder role reflects a user's responsibilities as a stakeholder of an asset and allows them to perform governance activities with only the permissions and privileges necessary to perform their tasks. In Metadata Command Center, you can create stakeholder roles from user roles and use them in access policies to grant users granular access to assets. If a stakeholder is assigned to an asset, the level of access and permissions for users who are not stakeholders of the asset are determined by the stakeholder role policies configured with the non-stakeholder option.

View user roles, stakeholder roles, and stakeholders on the Users tab on the Access Control page in Metadata Command Center.

For information about using user roles, user groups, and stakeholder roles in access policies, see the Administration help in Metadata Command Center.

## Access policies

Access policies are sets of rules that the administrator creates in Metadata Command Center to define permissions and control the level of access to the assets in the organization.

Access policies are an extension of the asset and feature privileges that are granted to your user role through Administrator. Along with the asset and feature privileges that are assigned to the user roles in Administrator, your organization administrator must create and assign access policies in Metadata Command Center that determine whether users can read, create, update, delete or manage access for the assets. Administrators can use predefined policies or define custom policies specific to their organization in Metadata Command Center. Predefined policies are associated with predefined user roles defined in Administrator. See Predefined user roles.

Administrators can grant access to assets, asset groups, or individual attributes of an asset using the following types of access policies:

* User role policy. Defines the access level of users who are assigned a user role in Administrator.
* Stakeholder role policy. Defines the access level of users who are assigned a stakeholder role in Metadata Command Center. A stakeholder role policy grant asset permissions that are unique to the stakeholder of the asset.
* User group policy. Defines the access level of users who are assigned a user group in Administrator. You can also use this access policy to control the access level to all users in the organization.

For information about managing access policies, see the Administration help in Metadata Command Center.

## Asset groups

You can use asset groups to control access to a set of assets. By grouping assets, you can use user group policies to grant or restrict access to multiple assets at a time.

For the access policies associated with asset groups to take effect, assign the asset groups to specific assets in Data Governance and Catalog or associate asset groups with assets when you run a catalog source job in Metadata Command Center. After you publish a user group policy that includes asset groups, you can use the access policy to control the access level on assets that are associated with the asset group.

When you create an asset group, you can create a hierarchy of up to four levels by selecting a parent asset group.

The following image shows the Asset Groups tab on the Customize page with a list of hierarchical asset groups in Metadata Command Center:
![The image shows the Asset Groups tab with a list of asset groups.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ad-asset-management/images/GUID-66D9020A-73FF-45E2-BDB8-E34B966002A0-low.png)
