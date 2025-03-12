# Role asset and feature privileges

Every role is associated with a set of asset or feature privileges. These privileges allow users to perform specific functions while working with assets and service features. Assign asset and feature privileges when you create a custom role.

Asset privileges provide CRUD, Run, and Set Permission privileges for different types of assets. For example, if you assign the Create privilege for mappings to a role, users with the role can create, view, and update mappings.

The following table describes the asset privileges:

| Privilege | Description |
|-----------|-------------|
| Create | Create assets of the selected type. For Secure Agents, this privilege allows users to download and install the Secure Agent. Automatically grants the Read and Update privileges. |
| Read | Open assets of the selected type. For tasks, this privilege also allows users to use a connection or schedule in the task. |
| Update | Edit assets of the selected type. Automatically grants the Read privilege. |
| Delete | Delete assets of the selected type. |
| Run | Run assets of the selected type. For the Data Integration service, users can run mappings, tasks, or taskflows. Users can also monitor, stop, and restart instances of the mapping, task, or taskflow. For the Cloud Integration Hub service, users can run publications or subscriptions. |
| Set permission | Configure permissions for assets of the selected type. For example, if you grant this privilege for projects, users with the role can select a project and enable other users and groups to read, update, delete, or change permissions for the selected project. To configure this privilege, your organization must have the appropriate license. |

Feature privileges control the ability to use certain features of a service. For example, the Data Quality "Data Preview - Dictionaries" privilege allows users to view the contents of a dictionary.

Assign asset and feature privileges on the role details page when you create a custom role. For more information about the role details page, see Role details.

You can't change the asset and feature privileges associated with a system-defined role.

## Administrator asset and feature privileges

Use the Administrator asset and feature privileges to allow users access to specific functionality while working with Administrator. You can enable asset and feature privileges when you create a custom role.

### Administrator asset privileges

The following table describes the Administrator asset privileges:

| Asset privilege | Description |
|----------------|-------------|
| Connection | Allows users to create, read, update, delete, or set permissions on connections. |
| Elastic Configuration | Allows users to create, read, update, delete, or run advanced configurations. |
| Folder | Allows users to create, read, update, delete, or set permissions on project folders. |
| Group | Allows users to create, read, update, or delete user groups. |
| OAuth Client | Allows users to create, read, update, or delete OAuth 2.0 clients. For more information about creating and managing OAuth 2.0 clients, see the help for API Center. |
| Organization | Allows users to read and update organization information. |
| Privilege | Allows users to view the asset and feature privileges associated with each role. |
| Project | Allows users to create, read, update, delete, or set permissions on projects. |
| Role | Allows users to view users' roles and the User Roles page in Administrator. |
| Schedule | Allows users to create, read, update, delete, or set permissions on project schedules. |
| Scheduler Blackout | Allows users to create, read, update, or delete schedule blackout periods. |
| Scheduler Job | Allows users to run assets on a schedule, view schedule information for assets, update the schedule for an asset, or delete a schedule from an asset. |
| Secure Agent | Allows users to create, read, update, delete, or set permissions on Secure Agents. |
| Secure Agent Group | Allows users to create, read, update, delete, or set permissions on Secure Agent groups. |
| User | Allows users to create, read, update, and delete user accounts. |

### Administrator feature privileges

The following table describes the Administrator feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| AdditionalOrg creation privilege | Allows users to create additional production and sandbox organizations when the AdditionalOrg view privilege is also granted. |
| AdditionalOrg view privilege | Allows users to view additional production and sandbox organizations from the production organization. This privilege is required to create additional production and sandbox organizations. |
| Asset - check in/out | Allows users to check in and check out assets from the source control repository. |
| Asset - export | Allows users to export assets from the organization. |
| Asset - import | Allows users to import assets into the organization. |
| Asset - pull version | Allows users to pull assets from the source control repository. |
| Asset - Source Control Logs | Allows users to view the source control logs. |
| Audit Log - view | Allows users to view the audit log. |
| Bundle - create | Allows users to create bundles when the "Bundle - view" privilege is also granted. |
| Bundle - delete | Allows users to delete bundles when the "Bundle - view" privilege is also granted. |
| Bundle - install | Allows users to install bundles so that they are available to your organization when the "Bundle - view" privilege is also granted. |
| Bundle - publish | Allows users to publish bundles when the "Bundle - view" privilege is also granted. |
| Bundle - update | Allows users to update bundles when the "Bundle - view" privilege is also granted. |
| Bundle - view | Allows users to view bundles. This privilege is required to create, delete, install, publish, and update bundles. |
| Configure Custom Repository Source Control | Allows users to configure a project-specific repository URL and branch name for project-level source control repositories when the Configure Source Control privilege is also granted. |
| Configure Source Control | Allows users to configure source control to enable version management for projects, folders, and assets. |
| Connectors - view | Allows users to view the connectors available to their organization and to view the Add-On Connectors page in Administrator. |
| Force Undo Checkout | Allows users to undo the checkout of an object that has been checked out by another user. |
| KMS View managed Key | Allows users to view the Customer Managed Keys area on the Security tab of the Settings page. |
| Manage Billing | Allows users of Data Integration-PayGo to manage their payment information. For more information about Data Integration-Free and PayGo, see "Introducing Informatica Cloud Data Integration-Free and PayGo." |
| Manage key rotation settings | Allows customers to manage key rotation for their organization through the platform REST API version 3 key resource. For more information about the v3 key resource, see REST API Reference. |
| ratecard.view | Allows users to view the current rate card for their organization on the Metering page. |
| SMS Manage Connection | Allows users to enable and disable the use of a secrets manager for the organization and to configure and update the secrets manager settings. |
| SMS View Connection | Allows users to view the Secret Vault area on the Security tab of the Settings page. |
| Suborg - create | Allows users to create sub-organizations when the "Suborgs - view" privilege is also granted. |
| Suborg - delete | Allows users to delete sub-organizations when the "Suborgs - view" privilege is also granted. |
| Suborg - update | Allows users to edit sub-organization settings when the "Suborgs - view" privilege is also granted. |
| Suborgs - link | Allows users to link sub-organizations when the "Suborgs - view" privilege is also granted. |
| Suborgs - manage licenses | Allows users to manage licenses for the organization's sub-organizations when the "Suborgs - view" privilege is also granted. |
| Suborgs - unlink | Allows users to unlink sub-organizations from the parent organization when the "Suborgs - view" privilege is also granted. |
| Suborgs - view | Allows users to view sub-organizations and switch into sub-organizations from the parent organization. This privilege is required to create, delete, update, link, manage the licenses of, and unlink sub-organizations. |
| Upgrade SDI | Allows users to upgrade Data Integration-Free organizations to PayGo organizations. For more information about Data Integration-Free and PayGo, see "Introducing Informatica Cloud Data Integration-Free and PayGo." |

## Application Integration feature privileges

Assign Application Integration feature privileges when you create custom roles for Application Integration and Application Integration Console.

**Important:** You must assign the Folder and Project asset privileges to the user's role. To do this, select the Data Integration service, and then select the CRUD privileges for the folder and project assets.

The following table describes the Application Integration feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| Administration | Gives users complete design-time and run-time administrative access to the Application Integration and Application Integration Console. Allows users to perform the following tasks:<br>- View, create, update, and delete all Application Integration assets.<br>- Manage and invoke services.<br>- Stop running processes.<br>- View instances and logs for deployed process.<br>- Deploy Process Developer BPR files to the Application Integration Console.<br>- Manage deployed catalogs.<br>- View WSDL files deployed across multiple systems.<br>- View Process Server metrics.<br>- Activate and deactivate process APIs.<br>- View, start, and stop event sources in listener-based connections.<br>**Note:** This privilege doesn't give users organization administration privileges. For example, a user with the only the Application Integration Administration privilege can't create sub-organizations. |
| Console Administration | Gives users near-complete access to the Application Integration Console. Allows users to perform the following tasks:<br>- View instances for deployed process.<br>- Stop running processes.<br>- View deployed Process Developer BPRs and catalogs.<br>- View WSDL files deployed across multiple systems.<br>- View Process Server metrics.<br>- Activate and deactivate process APIs.<br>- View, start, and stop event sources in listener-based connections.<br>This privilege doesn't allow users to deploy BPR files. |
| Data Viewer | Gives users access to detailed logs in the Application Integration Console. For example, you might assign this privilege to a someone who needs to see all logs across the organization. You would not normally assign this role to a developer.<br>**Note:** The process logging level must be set to verbose to get detailed logs. |
| Development | Gives users the ability to debug processes. Allows users to perform the following tasks:<br>- View, create, update, and delete all Application Integration assets.<br>- Invoke services.<br>- View the Detailed Process Instance page on the Application Integration Console.<br>- Manage processes instances.<br>- Activate and deactivate process APIs.<br>- View, start, and stop event sources in listener-based connections. |
| Monitoring | Gives users the ability to view all parts of the Application Integration Console except for detailed logs. Allows users to perform the following tasks:<br>- Activate and deactivate process APIs.<br>- View, start, and stop event sources in listener-based connections. |
| Publish Application Integration Assets | Gives users the ability to publish Application Integration processes, guides, connections, and service connectors. |
| View Application Integration Console | Gives users access to the Application Integration Console. You must assign this privilege to any role that has privileges that include working on the Application Integration Console. For example, assign this privilege with the Development privilege. |
| View Application Integration Designer | Gives users access to Application Integration. You must assign this privilege to any role that has privileges that include working on the Application Integration Console. For example, assign this privilege with the Publish Application Integration Assets privilege. |

## Data Governance and Catalog feature privileges

Use the Data Governance and Catalog feature privileges to allow users access to specific functionality while working with Data Governance and Catalog. You can enable feature privileges when you create a custom role.

The following table describes the Data Governance and Catalog feature privileges:

| Feature | Description |
|---------|-------------|
| Access Data Governance and Catalog application | Enable this feature to grant access to Data Governance and Catalog. If disabled, you cannot access Data Governance and Catalog to perform any governance tasks. |
| Curate Automatic Glossary Associations | *This privilege is not in use.* |
| Curate Data Classifications | *This privilege is not in use.* |
| Execute Data Access Management | Allows users the ability to execute a mapping that includes an Access Policy transformation in Data Integration.<br>**Note:** This privilege is for a future release. |
| Export | Allows users the ability to export assets from Data Governance and Catalog. |
| Force Delete | Allows users the following privileges:<br>- Delete assets with incoming relationships<br>- Delete assets with all the child assets in the hierarchy through bulk import |
| Import | Allows users the ability to download predefined templates and import business assets into Data Governance and Catalog. If you enable this privilege, you must additionally grant users the following asset privileges to import assets:<br>- Business assets. Create and update privilege<br>- Technical assets. Update privilege |
| Manage Tickets | Allows users the following privileges:<br>- Resolve or cancel tickets without being a stakeholder of the asset.<br>- Receive notifications for manual tickets without being a stakeholder of the asset. |
| Participate in Change Approvals | Allows users the following privileges:<br>- Participate in workflow approvals in Data Governance and Catalog.<br>The role for which you grant this privilege appears in the Role in Metadata Command Center when a user creates or modifies a workflow task.<br>- Add stakeholders to assets in Data Governance and Catalog.<br>- Configure workflows in Metadata Command Center. |
| Preview Data | Allows user to view the latest preview of failed rows for data quality rule occurrences in Data Governance and Catalog. |
| Stakeholdership | *This privilege is not in use.* |
| Super Admin | *This privilege is not in use.* |
| View Business Assets | *This privilege is not in use.* |
| View Data Access Audit | Allows users the ability to view Data Access Management audit logs in Data Governance and Catalog.<br>**Note:** This privilege is for a future release. |
| View Data Access Management | Allows users the ability to view Data Access Management in Data Governance and Catalog. To perform Data Access Management tasks, the administrator must create and assign access policies to this user role in Metadata Command Center. For more details, see Administration in the Metadata Command Center help. |
| View Data Classifications | *This privilege is not in use.* |
| View Profiled Stats | *This privilege is not in use.* |
| View Sensitive Data | *This privilege is not in use.* |
| View Technical Assets | *This privilege is not in use.* |
| View Unpublished Content | *This privilege is not in use.* |

## Data Ingestion and Replication minimum asset and feature privileges

Assign Data Ingestion and Replication Database asset and feature privileges when you create custom roles for Data Ingestion and Replication Database.

To create, view, or edit database ingestion and replication tasks, assign a user role that includes the minimum required privileges. You can use a system-defined role such as Admin or Designer that includes these privileges, or you can define a custom role that includes them.

### Minimum asset privileges

The following table describes the minimum required asset privileges:

| Service | Asset type | Asset privileges |
|---------|------------|------------------|
| Data Ingestion and Replication | Database Ingestion Task | Create, Read, Update |
| Administrator | Connection | Read |
| Administrator | Secure Agent Group | Read |

### Minimum feature privileges

The following table describes the minimum required feature privileges:

| Service | Feature privileges |
|---------|-------------------|
| Administrator | Connectors - view |

## Data Integration asset and feature privileges

Use the Data Integration asset and feature privileges to allow users access to specific functionality while working with Data Integration. You can enable asset and feature privileges when you create a custom role.

### Data Integration asset privileges

The following table describes the Data Integration asset privileges:

| Asset privilege | Description |
|----------------|-------------|
| API Collection | Allows users to create, read, update, delete, run, and set permissions on API collections. |
| Azure Data Sync Task | This privilege is not used. |
| Business Service Definition | Allows users to create, read, update, delete, and set permissions on business services. |
| Data Loader Task | Allows users to create, read, update, delete, run, and set permissions on data loader tasks. |
| Data Masking Task | Allows users to create, read, update, delete, run, and set permissions on data masking tasks. |
| Data Transfer Task | Allows users to create, read, update, delete, run, and set permissions on data transfer tasks. |
| Dynamic Mapping Task | Allows users to create, read, update, delete, run, and set permissions on dynamic mapping tasks. |
| File Listener | Allows users to create, read, update, delete, run, and set permissions on file listeners. |
| Fixed-Width File Format | Allows users to create, read, update, delete, run, and set permissions on fixed-width file formats. |
| Hierarchical Schema | Allows users to create, read, update, delete, run, and set permissions on hierarchical schemas. |
| Industry Data Services | Allows users to create, read, update, delete, run, and set permissions on industry data service customizers. |
| Intelligent Structure Task | Allows users to create, read, update, delete, run, and set permissions on intelligent structure models. |
| Linear Taskflow | Allows users to create, read, update, delete, run, and set permissions on linear taskflows. |
| Mapping | Allows users to create, read, update, delete, run, and set permissions on mappings. To run a mapping, users must have Run permission on both mappings and mapping tasks. |
| Mapping Task | Allows users to create, read, update, delete, run, and set permissions on mapping tasks. To run a mapping task, users must have Run permission on both mappings and mapping tasks. |
| Mapplet | Allows users to create, read, update, delete, run, and set permissions on mapplets. |
| PowerCenter task | Allows users to create, read, update, delete, run, and set permissions on PowerCenter tasks. |
| Replication Task | Allows users to create, read, update, delete, run, and set permissions on replication tasks. |
| Saved Query | Allows users to create, read, update, delete, run, and set permissions on saved queries. |
| Sequence Generator | Allows users to create, read, update, delete, and set permissions on shared sequences. |
| Swagger | Allows users to create, read, update, and delete Swagger files. |
| Synchronization Task | Allows users to create, read, update, delete, run, and set permissions on synchronization tasks. |
| Taskflow | Allows users to create, read, update, delete, run, and set permissions on taskflows. |
| User-Defined Function | Allows users to create, read, update, delete, run, and set permissions on user-defined functions. |

### Data Integration feature privileges

The following table describes the Data Integration feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| Access CDI error logs | Allows users to preview error rows files from the All Jobs, Running Jobs, and My Jobs pages, and from the job details. |
| Data - preview | Allows users to preview data in mappings and when they run SQL ELT optimization data preview jobs. |
| EDC for IICS Discovery | Allows users to use data catalog discovery to find objects from Enterprise Data Catalog and use them in mappings and some types of tasks.<br>**Note:** Before users can perform data catalog discovery, you must configure the Enterprise Data Catalog integration properties on the Organization page. |

## Data Marketplace feature privileges

View the features privileges in Informatica Intelligent Cloud Services Administrator that are available to a user role for the Data Marketplace service.

The following table describes the Data Marketplace feature privileges:

| Feature | Description |
|---------|-------------|
| Access Data Marketplace application | Display Data Marketplace in the Informatica Intelligent Cloud Services My Services page. |
| Approve data collection order | Approve a Data User's request to gain access to a Data Marketplace. |
| Bulk import data categories | Create multiple new categories at once in Data Marketplace. |
| Bulk import data collections | Create multiple new data collections at once in Data Marketplace. |
| Curate consumer access | Curate consumer accesses in Data Marketplace. |
| Curate data categories | Curate categories in Data Marketplace. |
| Curate data collections | Curate data collections in Data Marketplace. |
| Curate delivery targets | Curate the delivery targets of a data collection. |
| Curate delivery templates | Curate the delivery templates in Data Marketplace. |
| Fulfill data collection order | Grant data collection access to a Data User that ordered the data collection. |
| Manage application options | Configure the various settings of Data Marketplace. |
| Order data collection | Request access to a data collection. |
| View data categories | View categories in Data Marketplace. |
| View data collections | View data collections in Data Marketplace. |

## Data Profiling feature privileges

Use the Data Profiling feature privileges to allow users access to specific functionality while working with Data Profiling assets. You can enable asset and feature privileges when you create a custom role.

The following table describes the Data Profiling feature privileges:

| Privilege | Description |
|-----------|-------------|
| Data Profiling | Create, read, update, delete, run, and set permissions for a data profiling task. |
| Data Profiling - Compare Columns | Compare columns in a profile run. |
| Data Profiling - Compare Data Profiling Runs | Compare multiple profile runs. |
| Data Profiling - Data Profiling Results - View* | - View the profiling results for a data profiling task for any user including the user who created the data profiling task.<br>- View the valid and invalid rows in the Data Governance and Catalog scorecard using the Preview of Successful Rows and Preview of Unsuccessful Rows. |
| Data Profiling - Drill down* | View and select the drill-down option when you create a data profiling task. |
| Data Profiling - Export Data Profiling Results | Export the profiling results to a Microsoft Excel file. |
| Data Profiling - Manage Rules | Add or delete rules for a data profiling task. |
| Data Profiling - Query - Create | Create a query. |
| Data Profiling - Query - Submit | Run a query and view query results. |
| Data Integration - Data Preview | View source object data in the **Data Preview** area. |
| Data Profiling<br>Sensitive Data - view | Hide sensitive information for a particular user role. When the Sensitive Data - view privilege is configured, you cannot view the minimum value, maximum value, and most frequent values information in the compare column tab. |
| Data Profiling<br>Disable Data Value Storage | Does not store minimum, maximum, and most frequent values in the profiling warehouse. When you configure the Disable Data Value Storage feature, the sensitive information is not stored in the profile results and the source system. The values are not stored even if you have permissions to view the sensitive data, or if you configure a profiling task with the Maximum Number of Value Frequency Pairs option. By default, this feature is disabled. When the feature is disabled, the values are stored as expected. |
| * To perform drill down, and to view the Preview of Successful Rows and Preview of Unsuccessful Rows in a Data Governance and Catalog scorecard, you need the following privileges:<br>- Data Profiling - Query - Create<br>- Data Profiling - Query - Submit<br>- Data Profiling - Data Profiling Results - View<br>- Data Profiling Sensitive Data - view |

The following table describes how the Disable Data Value Storage and Sensitive Data- view features function when you configure for different user roles:

| Features | Custom role | Administrator or Designer | Result |
|----------|-------------|---------------------------|--------|
| Disable Data Value Storage | Inactive | Active | Sensitive information is not stored. |
| Disable Data Value Storage | Active | Inactive | Sensitive information is not stored. |
| Sensitive Data- view | Inactive | Active | Sensitive information is displayed. |
| Sensitive Data- view | Active | Inactive | Sensitive information is displayed. |

**Note:** When you activate the Disable Data Value Storage feature, Data Profiling or the source system does not store the sensitive information.

## Data Quality feature privileges

Use Data Quality feature privileges to grant users access to the preview functionality in data quality assets. You can enable feature privileges when you create a custom role.

The Data Quality feature privileges are enabled by default for the Admin and Designer roles.

The following table describes the Data Quality feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| Data Preview - Dictionaries | Allows users to view the contents of a dictionary in the following cases:<br>- The user opens the dictionary from the Explore page.<br>- The user selects the dictionary in a Data Quality asset. |
| Data Preview - Test Panel | Allows users to view data in the Test panel in a Data Quality asset.<br>**Note:** To run a test in a Data Quality asset, your role must also have the Run privilege for mappings in Data Integration. |
| Exceptions Data - Delete | Enables users to delete the exception data associated with an exception management job from the exception data store. Find the exception management job on the My Jobs page in Data Quality, Data Profiling, or Data Integration. |
| Exceptions Data - View | Enables users to download the exception records that an exception management job identifies. Find the exception management job on the My Jobs page in Data Quality, Data Profiling, or Data Integration. |

**Note:** The Data Preview - Dictionaries feature privilege and the Read privilege for dictionary assets work independently of each other. The Read privilege allows you to open the dictionary from the Explore page. The Data Preview - Dictionaries privilege allows you to view the dictionary data.

If you open a dictionary without the Data Preview - Dictionaries privilege, Data Quality displays a message to notify you that you do not have sufficient permissions to view the data.

## Domain Management Service asset and feature privileges

Use the Domain Management Service asset and feature privileges to allow users access to specific functionality while working with CDI-PC. You can enable asset and feature privileges when you create a custom role.

**Important:** You must assign Read access on the Secure Agent and Secure Agent Group assets to the user's role. To do this, select the Administrator service and assign Read privilege for the assets.

### Domain Registration asset privileges

The following table describes the Domain Registration asset privileges:

| Asset privilege | Description |
|----------------|-------------|
| Read | Allows users to view registered domains and domain details. |
| Create | Allows users to perform the following tasks:<br>- View registered domains and domain details.<br>- Register a domain.<br>- Deregister a domain.<br>- Retry registration.<br>- Edit domain details.<br>- Reconcile a domain.<br>Create includes the Read and Update privileges. |
| Update | Allows users to perform the following tasks:<br>- View registered domains and domain details.<br>- Deregister a domain.<br>- Retry registration.<br>- Edit domain details.<br>- Reconcile a domain.<br>Update includes the Read privilege. |
| Delete | Allows users to perform the following tasks:<br>- View registered domains and domain details.<br>- Delete a deregistered domain.<br>Delete includes the Read privilege. |

### Domain Registration feature privileges

The following table describes the Domain Registration feature privileges:

| Domain Registration feature privilege | Description |
|--------------------------------------|-------------|
| Domain Update | Allows users to update a domain. |

## Human Task asset and feature privileges

Use the Human Task asset and feature privileges to allow users access to specific functionality while working with human task assets. You can enable asset and feature privileges when you create a custom role.

### Human Task asset privileges

The following table describes the Human Task asset privileges:

| Asset privilege | Description |
|----------------|-------------|
| Human Task Assets | Allows users to perform the following actions:<br>- Create, read, update, or delete human task assets.<br>- Run processes that contain Human Task steps, which generate human tasks.<br>- Assign permissions to other user roles so that they can access human task assets. |

### Human Task feature privileges

The following table describes the Human Task feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| Development | Allows users to create and edit human task assets and use Human Task steps in Application Integration processes. |
| View Human Task Application | Allows users to view and access the Human Task service. |
| View Tasks | Allows users to access the Human Task Inbox in the Human Task service. |

## Metadata Command Center feature privileges

Use Metadata Command Center feature privileges to allow users access to specific functionality while working with Metadata Command Center. You can enable feature privileges when you create a custom role.

The following table describes the Metadata Command Center feature privileges:

| Feature | Description |
|---------|-------------|
| Access Metadata Command Center application | Grants access to Metadata Command Center. If disabled, users can't access Metadata Command Center. |
| Manage Custom Attributes | Allows users to manage asset relationships, predefined attributes, and custom attributes for asset types that appear in Data Governance and Catalog. |
| View Custom Attributes | Allows users to view attributes for asset types in Data Governance and Catalog. |
| Manage Data Classifications | Allows users to create and manage data classification inclusion rules. |
| View Data Classifications | Allows users to view data classifications in Data Governance and Catalog after you enable the capability and run the catalog source job in Metadata Command Center. |
| Manage Reference Data | Allows users to import and publish lookup tables that you can use in data classification. |
| View Reference Data | Allows users to view reference data in Data Governance and Catalog. |
| Monitor Jobs | Allows users to monitor jobs. |
| Manage Lineage Settings | Allows users to perform the following tasks:<br>- Assign or unassign connections to one or more catalog sources.<br>- Link catalog sources to generate lineage. |
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

## Model Serve asset and feature privileges

Use the Model Serve asset and feature privileges to allow users access to specific functionality while working with Model Serve. You can enable asset and feature privileges when you create a custom role.

### Model Serve asset privileges

The following table describes the Model Serve asset privileges:

| Asset privilege | Description |
|----------------|-------------|
| Machine Learning Model | Allows users to create, read, update, delete, run, and set permissions on machine learning models. |
| Model Deployment | Allows users to create, read, update, delete, run, and set permissions on model deployments. To run a model deployment, users must have Run permission on both machine learning models and model deployments. |

### Model Serve feature privileges

The following table describes the Model Serve feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| Predictions | Allows users to access the URL endpoint that generates predictions from a machine learning model. |

## Monitor feature privileges

Use the Monitor feature privileges to allow users access to specific functionality while working with Monitor. You can enable feature privileges when you create a custom role.

The following table describes the Monitor feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| Job Results - view | Allows users to view job results on the All Jobs, Running Jobs, and My Jobs pages. |
| Logs - View and Download | Allows users to view and download job log files. |

## Operational Insights feature privilges

Use the Operational Insights feature privileges to allow users access to specific functionality while working with Operational Insights. You can enable feature privileges when you create a custom role.

The following table describes the Operational Insights feature privileges:

| Feature | Description |
|---------|-------------|
| Anomaly alert settings - modify | Allows users to create and modify CLAIRE alerts for PowerCenter projects. |
| Data Integration Job Alerts | Allows users to view the Data Integration Alerts page and to create and modify alerts for Data Integration jobs. |
| Domain infrastructure - modify | Allows users to register, edit, and unregister domains and view the Infrastructure Alerts page. |
| Domain infrastructure alert settings - modify | Allows users to modify domain alerts on the Infrastructure Alerts page. |
| Domain job analytics - view | Allows users to view the Domains page for PowerCenter, Data Engineering, and Data Quality. |
| Domain projects - modify | Allows users to create and edit PowerCenter projects. Also allows users to view projects for Data Engineering Integration and Data Quality. |
| Infrastructure - modify | Allows users to edit the domain map. |
| Infrastructure - view | Provides users with access to Operational Insights and allows users to view the Home page. Also allows users to view the Secure Agents and Groups tab on the All Infrastructure page. Allows users to view the Infrastructure and PowerCenter alerts pages. |
| Job alert settings - modify | Allows users to create and modify alerts for PowerCenter jobs. |
| Mass Ingestion Job Alerts | Allows users to view, create, and modify alerts for Data Ingestion and Replication jobs. |
| Operational Insights - view | Allows users to view the following panels and pages:<br>- Rows Loaded panel on the Home page.<br>- Domains tab on the All Infrastructure page.<br>- PowerCenter, Data Engineering Integration, and Data Quality pages.<br>- Recommendations on the PowerCenter page.<br>- Alert Settings on the PowerCenter Alerts page.<br>- Alerts Received page.<br>Also allows users to view their assigned projects and view CLAIRE alerts for their projects. |
| Secure Agent runtime alert settings - modify | Allows users to edit Secure Agent alerts on the Infrastructure Alerts page. |

## Workbench Service asset and feature privileges

Use the Workbench Service asset and feature privileges to allow users access to specific functionality while working with Cloud Data Integration for PowerCenter (CDI-PC). You can enable asset and feature privileges when you create a custom role.

### Workbench Service asset privileges

The following table describes the Workbench Service asset privileges:

| Asset privilege | Description |
|----------------|-------------|
| Assessment Repoint Configuration | Allows users to create, read, update, delete, run, and set permissions on asset repoint configuration tasks. |
| Assessment Task | Allows users to create, read, update, delete, run, and set permissions on PowerCenter repository assessment tasks. |
| Bulk Update Task | Allows users to create, read, update, delete, and set permissions on bulk asset metadata update tasks. |
| Connection Map Configuration | Allows users to create, read, update, delete, run, and set permissions on connection map configuration tasks. |
| Conversion Property Configuration | Allows users to create, read, update, delete, run, and set permissions on conversion property configuration tasks. |
| Conversion Task | Allows users to create, read, update, delete, run, and set permissions on asset conversion tasks. |
| Parameter File Conversion Task | Allows users to create, read, update, delete, run, and set permissions on parameter file conversion tasks. |

### Workbench Service feature privileges

The following table describes the Workbench Service feature privileges:

| Feature privilege | Description |
|------------------|-------------|
| Download Artifacts | Allows users to download the files generated from an assessment, conversion, or a bulk update job. |
| Repository Assessment | Allows users to assess a repository.<br>**Note:** To run an assessment job, ensure that the Admin role is assigned to the user. |
| View Assessment Results | Allows users to access the assessment results. |
| View Configurations | Allows users to view the configurations. |
| View Jobs | Allows users to view the details of assessment, conversion, parameter file conversion, and bulk update jobs. |
| View Tasks | Allows users to view the details of the assessment, conversion, parameter file conversion, and bulk update tasks. |
