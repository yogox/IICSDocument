# System-defined roles

Informatica Intelligent Cloud Services provides system-defined roles that you can assign to users or user groups. You can't change or delete the system-defined roles.

The system-defined roles that you can assign to users and groups vary based on your organization's licenses. For example, if your organization has no access to Application Integration, you can't assign the Application Integration Business Manager or Application Integration Data Viewer role to any user or group in your organization.

There are two types of system-defined roles:

**Cross-service roles**
Cross-service roles define access privileges across multiple services. For example, users with the Deployer role can access some features in API Center, API Manager, Application Integration, Application Integration Console, Data Quality, and Data Ingestion and Replication.

**Service-specific roles**
Service-specific roles define access privileges for one service or for a group of closely related services. For example, users with the Governance User role can access Data Governance and Catalog but have no access to other services unless you assign additional roles.

**Note:** Don't assign the system-defined role "Dataloader admin" to any users. This role is used with Informatica Data Loader only.

## Cross-service roles

Cross-service roles are system-defined roles that define access privileges across multiple services.

The following table describes the cross-service roles:

| Cross-service role | Provides access to... | Description |
| ------------------ | --------------------- | ----------- |
| Admin | All services | Role for organization administrators. Provides full access to all licensed services with the following exceptions:<br>- Doesn't provide privileges to enable or disable the use of customer managed encryption keys for the organization. To provide these privileges, assign the user both the Admin and Key Admin roles.<br>- Doesn't provide full access to all MDM services. For example, doesn't allow the user to access the workflow inbox or create hierarchies in MDM business services. To provide full access to MDM services, assign the user an appropriate MDM service-specific role.<br>**Tip:** Best practice is to assign the Admin role to one or two trusted users and assign the users to an administrative user group that has full permissions on all asset types. These users can act as alternative organization administrators and can help troubleshoot access control and other organization security issues. |
| Data Integration Data Previewer | - Data Integration<br>- Data Profiling<br>- Data Quality<br>- Data Validation | Supplemental role that allows designers to preview data while creating mappings, tasks, profiles, and test cases. Allows users to perform the following tasks:<br>- Preview data in a mapping or task in Data Integration.<br>- Preview data on a data quality transformation in a mapping in Data Integration.<br>- View source object data for profiles and profile results in Data Profiling.<br>- Preview data while creating test cases in Data Validation.<br>**Note:** This is a supplemental role. Assign this role with another role, such as the Designer role, to ensure that users can access Data Integration, Data Profiling, and Data Validation. |
| Data Integration Task Executor | - Data Integration<br>- Data Access Management | Role for running tasks and taskflows and executing data access policies. Allows users to perform the following tasks:<br>- View assets and asset details in Data Integration.<br>- Run tasks and taskflows and test-run mappings in Data Integration.<br>- View user's own data integration jobs and job details in Data Integration.<br>- Start and stop user's own jobs in Data Integration.<br>- Download session logs in Data Integration.<br>- Execute data access policies in Data Integration.<br>- Access Data Access Management.<br>- View data access policies in Data Access Management. |
| Deployer | - API Center<br>- Application Integration<br>- Application Integration Console<br>- Data Quality<br>- Data Ingestion and Replication<br>- Data Validation | Role for users that deploy assets and processes. Allows users to perform the following tasks:<br>- View and deploy assets, assign policies, manage organization settings, and add OAuth 2.0 clients in API Center when assigned with the Service Consumer role.<br>- View asset details in Application Integration.<br>- Deploy assets, view settings, and upload and deploy Process Developer-generated orchestration artifacts (BPRs) in Application Integration Console.<br>- View asset details except dictionary data in Data Quality.<br>- View application ingestion, database ingestion, and streaming ingestion tasks in Data Ingestion and Replication.<br>- View test cases, test suites, and reports in Data Validation.<br>- Run test cases and test suites in Data Validation. |
| Designer | - Administrator<br>- API Center<br>- Application Integration<br>- Application Integration Console<br>- B2B Gateway<br>- Data Integration<br>- Data Profiling<br>- Data Quality<br>- Integration Hub<br>- Data Ingestion and Replication<br>- Model Serve<br>- Monitor<br>- Data Validation | Role for users that create assets, tasks, and processes. Allows users to perform the following tasks:<br>- Create assets, tasks, and processes.<br>- Configure connections, schedules, and runtime environments.<br>- Monitor jobs and advanced clusters, except in Mass Ingestion.<br>- View, create, and edit test cases and test suites in Data Validation.<br>Provides full access to Application Integration, B2B Gateway, Data Integration, Data Profiling, Data Quality, and Monitor.<br>Provides full access to API Center when the Service Consumer role is also assigned.<br>Provides partial access to Administrator, API Center, Application Integration Console, Integration Hub, Data Ingestion and Replication, Model Serve, and Data Validation. |
| Monitor | - Administrator<br>- API Center<br>- Application Integration<br>- Application Integration Console<br>- B2B Gateway<br>- Data Integration<br>- Data Profiling<br>- Data Quality<br>- Integration Hub<br>- Data Ingestion and Replication<br>- Model Serve<br>- Monitor | Role for users that monitor jobs. Allows users to perform the following tasks:<br>- Monitor API Center assets, Data Integration jobs, Data Quality assets, Integration Hub assets, Data Ingestion and Replication jobs, Model Serve assets, and Application Integration process instances.<br>- View schedules and upgrade settings for Secure Agent services in Administrator.<br>- Start and stop file servers, configure proxy servers, and view file server settings in Administrator.<br>- View asset details in Application Integration, B2B Gateway, Data Integration, Data Profiling, Integration Hub, and Model Serve.<br>- View settings in Application Integration Console.<br>- View asset details except dictionary data in Data Quality.<br>- View API invocation logs in API Center.<br>- View application ingestion, database ingestion, and streaming ingestion jobs and job details in Data Ingestion and Replication.<br>- View data integration and job details in Monitor. |
| Operator | - Application Integration<br>- Application Integration Console<br>- Data Profiling<br>- Data Quality<br>- Model Serve<br>- Operational Insights | Role for users that manage processes. Allows users to perform the following tasks:<br>- View asset details in Application Integration, Data Profiling, and Model Serve.<br>- Manage process instances and modify some operational server parameters in Application Integration.<br>- View and edit Process Server settings and some Cloud Server settings in Application Integration Console.<br>- View asset details except dictionary data in Data Quality.<br>- View cloud and domain infrastructure and Secure Agent alert settings in Operational Insights. |
| Service Consumer | - Administrator<br>- API Portal<br>- Application Integration<br>- Data Integration<br>- Data Quality | Role for users that run tasks and processes. Allows users to perform the following tasks:<br>- View schedules, Swagger files, and upgrade settings for Secure Agent services, start and stop file servers, configure proxy servers, and view other file server settings in Administrator.<br>- Open API Portal.<br>- Invoke processes in Application Integration.<br>- View tasks, run tasks, test-run mappings, run taskflows, and download workflow XML in Data Integration.<br>- View asset details except dictionary data in Data Quality.<br>Provides full access to API Portal. |

## Administrator roles

To provide access to the Administrator service, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Administrator:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Administrator except for privileges to enable or disable the use of customer managed encryption keys for the organization. To allow this ability, assign the user both the Admin and Key Admin roles. |
| Designer* | Allows users to perform the following tasks in Administrator:<br>- Configure connections, runtime environments, schedules, Swagger files, and advanced configurations.<br>- Install add-on connectors and install and uninstall add-on bundles.<br>- View upgrade settings for Secure Agent services.<br>- Start and stop file servers, configure proxy servers, and view other file server settings. |
| Key Admin | Allows users to enable and disable the use of customer managed encryption keys for their organization on the Security tab of the Settings page. Assign this role to a user who also has the Admin role. If the user doesn't have both roles, they can't see the Security tab.<br>For more information about customer managed encryption keys, see Organization Administration. |
| Monitor* | Allows users to perform the following tasks in Administrator:<br>- View schedules and upgrade settings for Secure Agent services.<br>- Start and stop file servers, configure proxy servers, and view other file server settings. |
| Service Consumer* | Allows users to perform the following tasks in Administrator:<br>- View schedules, Swagger files, and upgrade settings for Secure Agent services.<br>- Start and stop file servers, configure proxy servers, and view other file server settings. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## API Center roles

To provide access to API Center, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to API Center:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to API Center. |
| API Policy Manager | Allows users to define policies. Allows users to access the following pages in API Center:<br>- Explore (read-only)<br>- Policies |
| Deployer* | When assigned with the Service Consumer role, allows users to view and deploy assets, assign policies, manage organization settings, and add OAuth 2.0 clients in API Center. Allows users to access the following pages:<br>- Explore (read-only)<br>- API Console<br>- Configuration<br>**Note:** To provide these privileges, you must assign both the Deployer and Service Consumer roles. |
| Designer* | When assigned with the Service Consumer role, provides full access to all asset privileges and allows users to assign policies in API Center. Allows users to access the following pages:<br>- New Asset<br>- Explore<br>**Note:** To provide these privileges, you must assign both the Designer and Service Consumer roles. |
| Monitor* | Allows users to monitor API Center assets. Allows users to access the following pages:<br>- Explore (read-only)<br>- API Monitor |
| Service Consumer* | Allows users to access API Center when the Designer or Deployer role is also assigned. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

For more information about API Center roles, see the API Center help.

## API Manager roles

To provide access to API Manager, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to API Manager:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to API Manager. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

To provide different levels of access to API Manager, create custom roles. For more information, see the API Manager help.

## API Portal roles

To provide access to API Portal, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to API Portal:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to API Portal. |
| Service Consumer* | Allows users to open API Portal. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Application Integration and Application Integration Console roles

To provide access to Application Integration and Application Integration Console, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Application Integration and Application Integration Console:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Application Integration and Application Integration Console. Has the execution privileges. |
| Application Integration Business Manager | Role for monitoring business activity. Users with this role can view information about assets and process instances, but they can't change them.<br>Allows users to perform the following tasks:<br>- View folder and asset lists and asset details in Application Integration.<br>- Access the Processes, APIs, and Connections pages in Application Integration Console. |
| Application Integration Data Viewer | Supplemental role that allows users to view detailed logs in Application Integration Console. Assign this role along with at least one other role. For example, if you want a user with the Designer role to view detailed Process Server logs, assign the user the Application Integration Data Viewer and the Designer roles, and set the Process Server logging level to verbose.<br>**Note:** Users can view detailed logs for an artifact when the logging level is set to verbose. |
| Deployer* | Allows users to perform the following tasks in Application Integration and Application Integration Console:<br>- View asset details in Application Integration.<br>- Deploy assets and view settings on the Processes, Logs, Server Configuration, Deployed Assets, and Resources pages in Application Integration Console.<br>- Upload and deploy Process Developer-generated orchestration artifacts (BPRs) in Application Integration Console.<br>Assign this role in a production environment where deployment access is typically restricted. |
| Designer* | Provides full access to Application Integration.<br>Allows users to view and edit all settings except server configuration properties in Application Integration Console. |
| Monitor* | Allows users to perform the following tasks in Application Integration and Application Integration Console:<br>- View asset details in Application Integration.<br>- View settings in Application Integration Console. |
| Operator* | Allows users to perform the following tasks in Application Integration and Application Integration Console:<br>- View asset details in Application Integration.<br>- View and edit Process Server settings and some Cloud Server settings in Application Integration Console. For example, a user with the Operator role can create an alert service but can't view tenant details. |
| Service Consumer* | Allows users to execute Application Integration processes through APIs. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## B2B Gateway roles

To provide access to B2B Gateway, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to B2B Gateway:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to B2B Gateway. |
| Designer* | Provides full access to B2B Gateway. |
| Monitor* | Allows users to view asset details. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## B2B Partners Portal roles

If your organization uses B2B Gateway, you might want to enable access to B2B Partners Portal for your external trading partners. To give your trading partners access to B2B Partners Portal, create a custom role and assign it to partner users.

**Note:** There is no system-defined role for B2B Partners Portal external trading partners. Therefore, you'll need to create a custom role for them.

When you create a custom role for partner users, name the role so that you know it is for B2B Partners Portal users. For example, you might name the role "B2B Partners Portal User."

Optionally, you can give the role a description. Clearly describe the role so that you know it is for users from partner companies. For example, you might describe the role as "Role for users from partner companies to access the B2B Partners Portal service."

When you create a custom role for B2B Partners Portal users, enable the Partners Portal feature privilege for the B2B Partners Portal service. For more information about creating custom roles, see Creating a custom role.

Assign the custom role to users from your partner companies. You only need to create one role for B2B Partners Portal users. Assign the same role to all external B2B Partners Portal users.

## Business 360 Console roles

To provide access to Business 360 Console, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Business 360 Console:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Business 360 Console. Allows users to perform solution upgrades.<br>**Note:** To provide full access to Business 360 Console, assign users the Admin, Designer, and MDM Designer user roles. To allow users to perform only the configuration tasks in Business 360 Console, you can assign users the Admin role or both the Designer and MDM Designer roles. |
| Business 360 Process Executor | Required role for users with custom user roles to perform tasks in Business 360 Console and business applications. Allows users to update business entities in Business 360 Console.<br>Allows users to perform the following tasks in business applications:<br>- Save records and custom reports.<br>- View, create, update, and delete hierarchies.<br>- Import records, related records, and hierarchy data.<br>- Access the Workflow Inbox page. |
| Designer* | Allows users to perform tasks in Business 360 Console that require integration with other services such as Data Integration and Data Quality.<br>Allows users to perform the following tasks in Business 360 Console:<br>- Create MDM SaaS assets except reference data assets.<br>- Define a data model and source systems.<br>- Define and monitor jobs, such as ingress and egress.<br>- Configure data quality, match and merge, survivorship, business events, and global settings.<br>Doesn't allow users to define reference data assets. |
| Job Executor | Allows users to run ingress and egress jobs in Business 360 Console.<br>**Note:** This role is not required to run jobs that business applications run when users perform tasks, such as file import. |
| MDM Designer | Allows users to perform the following tasks in Business 360 Console:<br>- Create MDM SaaS assets.<br>- Define a data model and source systems.<br>- Define and monitor jobs, such as ingress and egress.<br>- Configure data quality, match and merge, survivorship, business events, and global settings.<br>- Export and import assets when the user also has the Designer role. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

For more information about Business 360 Console roles, see the Business 360 Console help.

## CLAIRE GPT roles

To provide access to CLAIRE GPT, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined user role that provides access to CLAIRE GPT:

| Role | Description |
| ---- | ----------- |
| CLAIRE GPT User | Provides full access to all the capabilities of CLAIRE GPT. |

For more information about CLAIRE GPT user roles, see the CLAIRE GPT help.

## Cloud Data Integration for PowerCenter (CDI-PC) roles

To provide access to the CDI-PC service, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to CDI-PC:

| Role | Description |
| ---- | ----------- |
| Domain Management | Provides full access to CDI-PC. |

## Customer 360 SaaS roles

To provide access to MDM - Customer 360 SaaS, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to MDM - Customer 360 SaaS:

| Role | Description |
| ---- | ----------- |
| Customer 360 Analyst | Role for creating records. Allows users to create, edit, and delete records in MDM - Customer 360 SaaS.<br>When a Customer 360 Analyst creates or edits a record, the changes trigger a review process that requires approval from a Customer 360 Manager. |
| Customer 360 Data Steward | Role for creating records and hierarchies. Allows users to perform any task in Customer 360 SaaS, including the following tasks:<br>- Create, edit, and delete records without approval.<br>- Run jobs.<br>- Review and approve customer records. |
| Customer 360 Manager | Role for managing records. Allows users to perform the following tasks:<br>- Review and approve or reject customer records.<br>- Create, edit, and delete records without approval. |
| MDM Business User | Allows users to view records in Customer 360 SaaS but not create or edit them. |

For more information about Customer 360 SaaS roles, see the MDM - Customer 360 SaaS help.

## Data Governance and Catalog roles

To provide access to Data Governance and Catalog, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Data Governance and Catalog:

| Role | Description |
| ---- | ----------- |
| Admin | Role for exporting assets in Data Governance and Catalog. |
| Data Access Owner | Role for viewing the Data Access Management page. |
| Governance Administrator* | Role for administering and managing assets in Data Governance and Catalog and Metadata Command Center. Allows users to perform the following tasks in Data Governance and Catalog:<br>- Export and import assets.<br>- Participate in change approvals.<br>- View the Data Access Management page.<br>- View the latest preview of failed rows for data quality rule occurrences. |
| Governance Owner* | Role for managing assets in Data Governance and Catalog. Allows users to perform the following tasks in Data Governance and Catalog:<br>- Export and import assets.<br>- Participate in change approvals.<br>- View the latest preview of failed rows for data quality rule occurrences. |
| Governance User* | Role for exporting assets in Data Governance and Catalog. Allows users to export assets in Data Governance and Catalog. Also allows users to view the Data Access Management page. |
| *Also provides access to Data Access Management, Data Marketplace and Metadata Command Center. For more information, see Data Marketplace roles and Metadata Command Center roles.<br>To perform cataloging and governance tasks, the administrator must create and assign access policies to these user roles in Metadata Command Center. For more details, see Administration in the Metadata Command Center help. |

For more information about Data Governance and Catalog roles, see the Data Governance and Catalog help.

## Data Ingestion and Replication roles

To provide access to Data Ingestion and Replication, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Data Ingestion and Replication:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Data Ingestion and Replication. |
| Deployer* | Allows users to view application ingestion, database ingestion, and streaming ingestion tasks. |
| Designer* | Allows users to create, view, edit, delete, run, and set permissions on application ingestion, database ingestion, and streaming ingestion tasks. |
| Monitor* | Allows users to view application ingestion, database ingestion, and streaming ingestion jobs and job details. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Data Integration roles

To provide access to Data Integration, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Data Integration:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Data Integration. |
| Data Integration Data Previewer* | Supplemental role that allows users to perform the following tasks in Data Integration:<br>- Preview data when they select a source, target, or lookup object for use in a mapping or task.<br>- Preview data when on a data quality transformation that they select in a mapping.<br>Assign this role with another role, such as the Designer role, to ensure that users can access Data Integration. |
| Data Integration Task Executor* | Role for running tasks and taskflows. Allows users to perform the following tasks in Data Integration:<br>- View assets and asset details.<br>- Run tasks and taskflows and test-run mappings.<br>- View user's own data integration jobs and job details.<br>- Start and stop user's own jobs.<br>- Download session logs. |
| Designer* | Provides full access to Data Integration. |
| Monitor* | Allows users to view asset details in Data Integration. |
| Service Consumer* | Allows users to view tasks, run tasks, test-run mappings, run taskflows, and download workflow XML in Data Integration. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Data Marketplace roles

To provide access to Data Marketplace, assign users the appropriate roles. You can assign a system-defined role to Data Marketplace users. 

The following table describes the system-defined roles that provide access to Data Marketplace:

| Role | Description |
| ---- | ----------- |
| Data Marketplace Administrator | Role for performing administrative tasks. Provides full access to access to Data Marketplace. |
| Data Marketplace Category Owner | Role for users that have the rights to a category. Allows users to perform the following tasks:<br>- Create and bulk create data collections within the user's category.<br>- Add and remove data assets inside data collections within the user's category.<br>- Approve and reject data orders for data collections.<br>- Approve and reject data collection requests on categories that the user is responsible for.<br>- Add and edit delivery targets inside data to collections within the user's category.<br>- Link and remove variants to data collections within the user's category.<br>- Delete data collections within the user's category.<br>- Rate data collections that the user has access to against the context the user has access with.<br>- Search for published data collections.<br>- Compare collections.<br>- Add and bulk add data assets to data collections.<br>- Create an order and raise data collection requests.<br>- Create, bulk create, modify, and delete categories.<br>- Add and remove terms of use inside data collections within the user's category.<br>- Participate in public discussion channels.<br>- Comment on private channels that the user has access to. |
| Data Marketplace Data Collection Owner | Role for users that have rights to a data collection. Allows users to perform the following tasks:<br>- Create, bulk create, modify, and delete data collections.<br>- View data collections that the user owns.<br>- Add and bulk add terms of use and data assets to data collections that the user owns.<br>- Remove terms of use and data assets from data collections that the user owns.<br>- Search for published data collections.<br>- Compare collections.<br>- Add and edit delivery targets inside the data collections that the user owns.<br>- Rate data collections that the user has access to against the context the user has access with.<br>- Create an order for collections and raise data collection requests against collections or categories.<br>- Complete and reject data collection requests raised on data collections that the user owns.<br>- Approve and reject data collection access requests.<br>- Link variants.<br>- Participate in public discussion channels.<br>- Comment on private channels that the user has access to. |
| Data Marketplace Data Collection Technical Owner | Role for users that have technical rights to a data collection. Allows users to perform the following tasks:<br>- View orders for data collections.<br>- Add and edit delivery targets to data collections.<br>- Request withdrawal and withdraw access to data collections.<br>- Add and remove data assets and terms of use inside data collections.<br>- Rate data collections that the user has access to against the context the user has access with.<br>- Search for published data collections.<br>- Compare collections.<br>- Create an order on collections and raise data collection requests against collections and categories.<br>- Bulk create "terms of use - data collection" relationships and "delivery target - data collection" relationships.<br>- Deliver data that is ordered by a data user.<br>- Participate in public discussion channels.<br>- Comment on private channels that the user has access to. |
| Data Marketplace Delivery Owner | Role for managing the delivery option for delivering data collections. Allows users to perform the following tasks:<br>- Search and compare data collections.<br>- Rate data collections that user has access to.<br>- Create delivery options and delivery targets.<br>- Bulk create delivery formats, delivery methods, delivery templates, and "delivery target - data collection" relationships.<br>- Request withdrawal of consumer access, withdraw consumer access, and fulfill data orders for data collections that have a delivery option that the user is responsible for.<br>- Participate in public and private discussion channels that the user has access to. |
| Data Marketplace Technical Administrator | Role for performing technical administrative tasks. Allows users to perform the following tasks:<br>- View data orders for and add delivery targets to data collections.<br>- Deliver requested data collections to data users.<br>- Search and compare data collections.<br>- Rate data collections that the user has access to.<br>- Add data assets, delivery targets, and terms of use to data collections.<br>- Bulk create data elements, data assets, and consumer accesses.<br>- Delete data elements and data assets.<br>- Modify object labels.<br>- Configure data delivery formats and methods.<br>- Configure default delivery targets to deliver data.<br>- Import assets from Data Governance and Catalog.<br>- Configure the general "terms of use" message and create new terms of use.<br>- Create cost centers.<br>- Request withdrawal and withdraw consumer accesses.<br>- Bulk create cost centers, delivery formats, delivery methods, delivery templates, "terms of use - data collection" relationships, and "delivery target - data collection" relationships.<br>- Configure star owners.<br>- Participate in public and private discussion channels that the user has access to.<br>- Customize the Data Marketplace user interface. |
| Data Marketplace User | Role for using data collections. Allows users to perform the following tasks:<br>- Order, and compare data collections.<br>- Search for published data collections.<br>- View requested and delivered data collections.<br>- View data collection details.<br>- Rate data collections that the user has access to.<br>- Create and cancel data collection requests on collections and categories.<br>- Participate in public and private discussion channels. |
| Governance Administrator | Role for using data collections. Allows users to perform the following tasks:<br>- Order, and compare data collections.<br>- Search for published data collections.<br>- View requested and delivered data collections.<br>- View data collection details.<br>- Rate data collections that the user has access to.<br>- Create and cancel data collection requests on collections and categories.<br>- Participate in public and private discussion channels. |
| Governance User | Role for using data collections. Allows users to perform the following tasks:<br>- Order, and compare data collections.<br>- Search for published data collections.<br>- View requested and delivered data collections.<br>- View data collection details.<br>- Rate data collections that the user has access to.<br>- Create and cancel data collection requests on collections and categories.<br>- Participate in public and private discussion channels. |

For more information about Data Marketplace roles, see the Data Marketplace help.

## Data Profiling roles

To provide access to Data Profiling, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Data Profiling:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Data Profiling. |
| Data Integration Data Previewer* | Supplemental role that allows users to preview source object data when they create a profile or view profile results.<br>Assign this role with another role, such as the Designer role, to ensure that users can access Data Profiling. |
| Designer* | Provides full access to Data Profiling. |
| Monitor* | Allows users to view asset details in Data Profiling. |
| Operator* | Allows users to view asset details in Data Profiling. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Data Quality roles

To provide access to Data Quality, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Data Quality:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Data Quality. |
| Deployer* | Allows users to view asset details except dictionary data in Data Quality. |
| Designer* | Provides full access to Data Quality. |
| Monitor* | Allows users to view asset details except dictionary data in Data Quality. |
| Operator* | Allows users to view asset details except dictionary data in Data Quality. |
| Service Consumer* | Allows users to view asset details except dictionary data in Data Quality. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Integration Hub roles

To provide access to Cloud Integration Hub, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Cloud Integration Hub:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Cloud Integration Hub. |
| Designer* | Allows users to create, view, edit, delete and run
| Monitor* | Allows users to view asset details in Cloud Integration Hub. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

For more information about Cloud Integration Hub roles, see the Cloud Integration Hub help.

## Metadata Command Center roles

To provide access to Metadata Command Center, assign users the appropriate roles. You can assign a system-defined role or custom roles for users.

The following table describes the system-defined roles that provide access to Metadata Command Center:

| Role | Description |
| ---- | ----------- |
| Admin* | Role for performing upgrades. In addition, this role can perform all tasks that a Governance Administrator can perform in Metadata Command Center. |
| Governance Administrator** | Role for administering assets and operations in Data Governance and Catalog and Metadata Command Center. Allows users to perform the following tasks in Metadata Command Center:<br>- Run and set permissions on catalog source configurations.<br>- Manage metadata access control, asset groups, asset page customization, custom attributes, data classifications, IDMC metadata settings, lineage settings, reference data, system settings, and workflow settings.<br>- Monitor jobs.<br>- View access control, asset groups, asset page customization, custom attributes, data classifications, IDMC metadata settings, lineage settings, reference data, system settings, and workflow settings. |
| * Provides access to multiple services. For more information, see Cross-service roles.<br>** Also provides access to Data Access Management, Data Governance and Catalog, and Data Marketplace. For more information, see Data Governance and Catalog roles.<br>To perform cataloging and governance tasks, the administrator must create and assign access policies to these user roles in Metadata Command Center. For more details, see Administration in the Metadata Command Center help. |

For more information about Metadata Command Center roles, see the Metadata Command Center help.

## Model Serve roles

To provide access to Model Serve, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Model Serve:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Model Serve. |
| Designer* | Allows users to perform the following tasks in Model Serve:<br>- Create, view, edit, and delete machine learning models.<br>- Create, view, edit, delete, and run model deployments.<br>- Generate predictions from a deployed machine learning model. |
| Model Serve Admin | Role for Model Serve administration. Allows users to perform the following tasks:<br>- Assign permissions for other Model Serve users.<br>- Register and deploy machine learning models.<br>- Generate predictions from a deployed machine learning model. |
| Model Serve Predictions User | Role for generating predictions. Allows users to perform the following tasks:<br>- Generate predictions from a deployed machine learning model.<br>- View, but not change, model deployment assets. |
| Model Serve System Role | Role for the Model Serve system user. Assigns necessary permissions so that the system user can perform tasks such as provisioning resources for model deployments.<br>Do not assign this role to users.<br>For more information about the Model Serve system user, see Model Serve system user. |
| Monitor* | Allows users to view asset details in Model Serve. |
| Operator* | Allows users to view asset details in Model Serve. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Monitor roles

To provide access to Monitor, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Monitor:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Monitor. |
| Designer* | Provides full access to Monitor. |
| Monitor* | Allows users to view data integration jobs and job details in Monitor.<br>Doesn't allow users to view export or import jobs. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Operational Insights roles

To provide access to Operational Insights, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to Operational Insights:

| Role | Description |
| ---- | ----------- |
| Admin* | Provides full access to Operational Insights. |
| Operator* | Allows users to perform the following tasks in Operational Insights:<br>- View cloud and domain infrastructure.<br>- View Secure Agent alert settings. |
| * Provides access to multiple services. For more information, see Cross-service roles. |

## Product 360 SaaS roles

To provide access to MDM - Product 360 SaaS, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to MDM - Product 360 SaaS:

| Role | Description |
| ---- | ----------- |
| Product 360 Manager | Role for managing records. Allows users to perform the following tasks:<br>- Review and approve records.<br>- Create, edit, and delete records without approval. |
| Product 360 Read-Only | Role for viewing records. Allows users to view records in Product 360 SaaS but not edit them. |

For more information about Product 360 SaaS roles, see the MDM - Product 360 SaaS help.

## Reference 360 roles

To provide access to MDM - Reference 360, assign users the appropriate roles. You can assign a system-defined role to Reference 360 users. 

The following table describes the system-defined roles that provide access to MDM - Reference 360:

| Role | Description |
| ---- | ----------- |
| Reference 360 Administrator | Administrative role for Reference 360. Allows users to configure the Reference 360 environment. |
| Reference 360 Business Analyst | Role for analyzing assets. Allows users to view and analyze assets, but not propose changes to them. |
| Reference 360 Business Steward | Role for the subject matter experts for reference data. Allows users to perform the following tasks:<br>- Create and manage code values in code lists and value mappings in crosswalks.<br>- Approve changes proposed by other users.<br>- Send their own changes for approval or directly publish their changes without approval. |
| Reference 360 Planner | Role for creating and managing hierarchies. Allows users to perform the following tasks:<br>- Create hierarchy assets, define hierarchy models, and import hierarchy relationships.<br>- Delete hierarchies that are no longer needed.<br>- Assign the Planner stakeholder role to other users for a hierarchy. |
| Reference 360 Primary Owner | Role for creating and defining reference data structures. Allows users to perform the following tasks:<br>- Create and define reference data structures, such as reference data sets and code lists.<br>- Delete code lists.<br>- Propose changes to code values in code lists. The changes must be approved by Business Stewards.<br>- Assign users access to code lists and reference data sets using Stakeholder roles. |
| Reference 360 Stakeholder | Role for proposing changes to code values. Allows users to propose changes, but the proposed changes must be approved by Business Stewards. |
| Reference 360 User | Restricted access role. By default, users with this role can't access any assets. To allow users to access a specific asset, such as a code list or crosswalk, assign this role along with the stakeholder role for the asset. |

For more information about Reference 360 roles, see the MDM - Reference 360 help.

## Supplier 360 SaaS roles

To provide access to MDM - Supplier 360 SaaS, assign users the appropriate roles. You can assign a system-defined role or create custom roles for users.

The following table describes the system-defined roles that provide access to MDM - Supplier 360 SaaS:

| Role | Description |
| ---- | ----------- |
| Supplier 360 Analyst | Role for analyzing records. Allows users to create, read, edit, and delete records in Supplier 360 SaaS. When a Supplier 360 Analyst creates or edits a record, the changes trigger a review process that requires approval from a Supplier 360 manager. |
| Supplier 360 Commodity Manager | Role for managing commodity evaluation tasks. Has the originator and approver privileges. Allows users to perform the following tasks:<br>- Claim and disclaim commodity evaluation tasks.<br>- Act on the commodity evaluation tasks in the approval workflow.<br>- Create, read, edit, and delete records. |
| Supplier 360 Contract Manager | Role for managing contract evaluation tasks. Has the originator and approver privileges. Allows users to perform the following tasks:<br>- Claim and disclaim contract evaluation tasks.<br>- Act on the contract evaluation tasks in the approval workflow.<br>- Create, read, edit, and delete records. |
| Supplier 360 Credit Manager | Role for managing credit evaluation tasks. Has the originator and approver privileges. Allows users to perform the following tasks:<br>- Claim and disclaim credit evaluation tasks.<br>- Act on the credit evaluation tasks in the approval workflow.<br>- Create, read, edit, and delete records. |
| Supplier 360 Data Steward | Role for managing records. Allows users to perform the following tasks:<br>- Create, read, edit, and delete records with or without approval.<br>- Run jobs.<br>- Review and approve records.<br>- Match, merge, and unmerge records. |
| Supplier 360 Read Only | Role for viewing records in Supplier 360 SaaS. Allows users to view records but not create or edit them. |
| Supplier 360 Risk Manager | Role for managing risk evaluation tasks. Has the originator and approver privileges. Allows users to perform the following tasks:<br>- Claim and disclaim risk evaluation tasks.<br>- Act on the risk evaluation tasks in the approval workflow.<br>- Create, read, edit, and delete records. |
| Supplier 360 Task Admin | Role for administering evaluation tasks. Has the originator and approver privileges. Allows users to view all unclaimed evaluation tasks. |
