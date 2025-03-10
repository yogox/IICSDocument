# Manage access to assets

As your organization's data rapidly evolves, a robust and centralized mechanism to control access to assets becomes crucial to effectively manage the assets in your organization. Metadata access control is the practice of managing the level of user access to assets in your organization through a set of rules called access policies.

With metadata access control, you can view and perform actions on specific assets or groups of assets only if your organization administrator has explicitly granted access and permissions to you through access policies. This ensures that with appropriate permissions the right users have access to the right assets.

The following concepts apply as you implement metadata access control in your organization:

• Roles, users, and user groups. See Roles, users, and user groups.
• Access policies. See Access policies.
• Asset groups. See Asset groups.

### How it works

The organization administrator can implement access control in your organization through a combination of privileges in Administrator and access policies in Metadata Command Center. Let us look at the tasks that the administrator performs to enforce metadata access control.

In Administrator,

1. Create users, user roles, and user groups.
2. Assign users and user groups to user roles.
3. Grant minimum asset and feature privileges to user roles.

In Metadata Command Center,

1. Extend the Administrator user role definitions and create access policies to determine the level of access that users have on assets. Optionally, use asset groups or attribute groups in access policies to control access to a group of assets or to certain attributes of assets.
2. Publish the access policies to enforce metadata access control.

In Data Governance and Catalog,

1. Users interact with assets based on the permissions and level of access defined in access policies.
2. If using asset groups, assign asset groups to assets to enforce access control over the assets.
3. Assign a user as the stakeholder of the asset to grant asset permissions that are unique to the stakeholder.

© Copyright Informatica LLC 2021, 2025
