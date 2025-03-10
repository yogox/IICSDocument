# Feature privileges in Administrator

An organization administrator can assign privileges for some features of Data Governance and Catalog and Metadata Command Center to user roles in Administrator. To perform cataloging and governance tasks, the administrator must create and assign access policies to users in Metadata Command Center.

To assign feature privileges to user roles in Administrator, open a role, select the service, and select one or more features on the Features tab for a service. For more information about assigning feature privileges to user roles, see User Administration in the Administrator help.

For information about creating access policies and assigning them to user roles, user groups, or stakeholder roles, see Administration in the Metadata Command Center help.

### Feature privileges for Metadata Command Center

The following table explains the feature privileges that are available for the Metadata Command Center service in Administrator:    

| Feature | Description |
| --- | --- |
| Access Metadata Command Center application | Grants access to Metadata Command Center. If disabled, users can't access Metadata Command Center. |
| Manage Custom Attributes | Allows users to manage asset relationships, predefined attributes, and custom attributes for asset types that appear in Data Governance and Catalog. |
| View Custom Attributes | Allows users to view attributes for asset types in Data Governance and Catalog. |
| Manage Data Classifications | Allows users to create and manage data classification inclusion rules. |
| View Data Classifications | Allows users to view data classifications in Data Governance and Catalog after you enable the capability and run the catalog source job in Metadata Command Center. |
| Manage Reference Data | Allows users to import and publish lookup tables that you can use in data classification. |
| View Reference Data | Allows users to view reference data in Data Governance and Catalog. |
| Monitor Jobs | Allows users to monitor jobs. |
| Manage Lineage Settings | Allows users to perform the following tasks:
- Assign or unassign connections to one or more catalog sources.
- Link catalog sources to generate lineage. |
| View Lineage Settings | Allow users to view data lineage from the Lineage tab. |
| Manage Access Control | Allows users to create and manage stakeholder roles and access policies. Also allows users to share saved searches, dashboards, and set default dashboards for other users. |
| View Access Control | Allows users to view access policies. |
| Manage Asset Groups | Allows users to create, update, or delete asset groups. |
| View Asset Groups | Allows users to view asset groups. |
| Manage Workflow Settings | Allows users to create or modify workflows. |
| View Workflow Settings | Allows users to view workflows. |
| Manage System Settings | Allows users to modify system settings. |
| View System Settings | Allow user to view the Reference IDs tab. |
| Manage Asset page customization | Allows users to create, update and delete the layout of pages and preview panes of assets. Also allows users to assign default layouts to other users based on their roles, user groups, or to all users in the organization. |
| View Asset page customization | Allows users to view the layout of pages. |
| Manage IDMC Metadata Settings | Allows users to synchronize metadata from Data Integration tasks and Application Integration objects with the catalog. |
| View IDMC Metadata Settings | Allow users to view IDMC metadata. |
| Manage Upgrade | Allows users to initiate upgrades to the latest version of Data Governance and Catalog. |
| Super Admin | Allows users access to unique administrator capabilities beyond the Governance Administrator role. |

### Feature privileges for Data Governance and Catalog

The following table explains the feature privileges that are available for the Data Governance and Catalog service in Administrator:   

| Feature | Description |
| --- | --- |
| Access Data Governance and Catalog application | Enable this feature to grant access to Data Governance and Catalog. If disabled, you cannot access Data Governance and Catalog to perform any governance tasks. |
| Curate Automatic Glossary Associations | *This privilege is not in use.* |
| Curate Data Classifications | *This privilege is not in use.* |
| Execute Data Access Management | Allows users the ability to execute a mapping that includes an Access Policy transformation in Data Integration.

**Note:** This privilege is for a future release. |
| Export | Allows users the ability to export assets from Data Governance and Catalog. |
| Force Delete | Allows users the following privileges:
- Delete assets with incoming relationships
- Delete assets with all the child assets in the hierarchy through bulk import |
| Import | Allows users the ability to download predefined templates and import business assets into Data Governance and Catalog. If you enable this privilege, you must additionally grant users the following asset privileges to import assets:
- Business assets. Create and update privilege
- Technical assets. Update privilege |
| Manage Tickets | Allows users the following privileges:
- Resolve or cancel tickets without being a stakeholder of the asset.
- Receive notifications for manual tickets without being a stakeholder of the asset. |
| Participate in Change Approvals | Allows users the following privileges:
- Participate in workflow approvals in Data Governance and Catalog.
The role for which you grant this privilege appears in the Role in Metadata Command Center when a user creates or modifies a workflow task.
- Add stakeholders to assets in Data Governance and Catalog.
- Configure workflows in Metadata Command Center. |
| Preview Data | Allows user to view the latest preview of failed rows for data quality rule occurrences in Data Governance and Catalog. |
| Stakeholdership | *This privilege is not in use.* |
| Super Admin | *This privilege is not in use.* |
| View Business Assets | *This privilege is not in use.* |
| View Data Access Audit | Allows users the ability to view Data Access Management audit logs in Data Governance and Catalog.

**Note:** This privilege is for a future release. |
| View Data Access Management | Allows users the ability to view Data Access Management in Data Governance and Catalog.
To perform Data Access Management tasks, the administrator must create and assign access policies to this user role in Metadata Command Center. For more details, see Administration in the Metadata Command Center help. |
| View Data Classifications | *This privilege is not in use.* |
| View Profiled Stats | *This privilege is not in use.* |
| View Sensitive Data | *This privilege is not in use.* |
| View Technical Assets | *This privilege is not in use.* |
| View Unpublished Content | *This privilege is not in use.* |
