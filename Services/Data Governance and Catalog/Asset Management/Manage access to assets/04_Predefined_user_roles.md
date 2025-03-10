# Predefined user roles

As an organization administrator, you can assign predefined user roles to users and user groups in Administrator.  

Predefined user roles are system-defined roles that define certain privileges to the services that your organization uses. Some asset and feature privileges are enabled by default for predefined user roles. You cannot modify, rename, or delete predefined roles.  

Data Governance and Catalog provides the following predefined roles:
* [Data Access Owner role](#ww3_9_17_7_1)
* [Governance Administrator role](#ww3_9_17_10_1)
* [Governance Owner role](#ww3_9_17_13_1)
* [Governance User role](#ww3_9_17_16_1)

To extend the user role privileges provided in Administrator, you can assign the predefined access policies to user roles and stakeholder roles in Metadata Command Center. See Predefined access policies.

## Data Access Owner role

A user with the Data Access Owner role has the feature privileges assigned in Administrator to perform certain tasks in Data Governance and Catalog. In Metadata Command Center, a user with this role also automatically receives the default privileges to perform tasks on data access policies in Data Governance and Catalog.

### Data Governance and Catalog

The following table lists the feature privileges that are enabled or disabled by default in Data Governance and Catalog for the Data Access Owner role:

| Features | Status |
|----------|--------|
| Access Data Governance and Catalog Application | Enabled |
| Export | Disabled |
| Force Delete | Disabled |
| Import | Disabled |
| Manage Tickets | Disabled |
| Participate in Change Approvals | Disabled |
| Preview Data | Disabled |
| View Data Access Audit | Enabled **Note:** This privilege is for a future release. |
| View Data Access Management | Enabled |

## Governance Administrator role

A user with the Governance Administrator role has asset and feature privileges assigned in Administrator that assist in working with features and assets in Metadata Command Center, Data Governance and Catalog and Data Marketplace. The Governance Administrator role also includes features and privileges that you need to configure and run Application Integration processes and Human Tasks services using custom workflows. 

### Metadata Command Center

The following table lists all the asset privileges that are enabled or disabled by default for the Governance Administrator role in Metadata Command Center:

| Assets | Privileges enabled | Privileges disabled |
|--------|-------------------|------------------|
| Catalog Source Configurations | Create, read, update, delete, run, set permission | None |
| Custom Catalog Source Type | Create, read, update, delete | Run, set permission |
| Custom Models | Create, read, update, delete | Run, set permission |

The following table lists the feature privileges that are enabled or disabled by default for the Governance Administrator role in Metadata Command Center:

| Features | Status |
|----------|--------|
| Access Metadata Command Center Application | Enabled |
| Manage Access Control | Enabled |
| Mange Asset Groups | Enabled |
| Manage Asset Page Customization | Enabled |
| Manage Custom Attributes | Enabled |
| Manage Data Classifications | Enabled |
| Manage IDMC Metadata Settings | Enabled |
| Manage Lineage Settings | Enabled |
| Manage Reference Data | Enabled |
| Manage System Settings | Enabled |
| Manage Upgrade | Disabled |
| Manage Workflow Settings | Enabled |
| Monitor Jobs | Enabled |
| Super Admin | Disabled |
| View Access Control | Enabled |
| View Asset Groups | Enabled |
| View Asset Page Customization | Enabled |
| View Custom Attributes | Enabled |
| View Data Access Audit | Enabled **Note:** This privilege is for a future release. |
| View Data Access Management | Enabled |
| View Data Classifications | Enabled |
| View IDMC Metadata Settings | Enabled |
| View Lineage Settings | Enabled |
| View Reference Data | Enabled |
| View System Settings | Enabled |
| View Workflow Settings | Enabled |

### Data Governance and Catalog

The following table lists the feature privileges that are enabled or disabled by default for the Governance Administrator role in Data Governance and Catalog:

| Features | Status |
|----------|--------|
| Access Data Governance and Catalog Application | Enabled |
| Export | Enabled |
| Force Delete | Disabled |
| Import | Enabled |
| Manage Tickets | Disabled |
| Participate in Change Approvals | Enabled |
| Preview Data | Enabled |

### Data Marketplace

The following table lists the feature privileges that are enabled or disabled by default for the Governance Administrator role in Data Marketplace:

| Features | Status |
|----------|--------|
| Access Data Marketplace | Enabled |
| Approve or Reject Orders | Disabled |
| Cancel Your Orders And Data Collection Requests | Enabled |
| Complete or Reject Data Collection Requests | Disabled |
| Configure And Manage Data Marketplace | Disabled |
| Fulfill Or Reject Orders | Disabled |
| View Set up page | Disabled |
| Withdraw Consumer Accesses | Disabled |

### Application Integration

The following table lists the asset privileges that are enabled or disabled by default for the Governance Administrator role in Application Integration:

| Assets | Privileges enabled | Privileges disabled |
|--------|-------------------|------------------|
| Application Integration Assets | Create, read, update, delete, run, set permission | None |

The following table lists the feature privileges that are enabled or disabled by default for the Governance Administrator role in Application Integration:

| Features | Status |
|----------|--------|
| Administration | Enabled |
| Console Administration | Enabled |
| Data Viewer | Enabled |
| Development | Enabled |
| Monitoring | Enabled |
| Publish Application Integration Assets | Enabled |
| View Application Integration Console | Enabled |
| View Application Integration Designer | Enabled |

### Human Tasks

The following table lists the asset privileges that are enabled or disabled by default for the Governance Administrator role in Human Tasks:

| Assets | Privileges enabled | Privileges disabled |
|--------|-------------------|------------------|
| Human Task Assets | Create, read, update, delete, run, set permission | None |

The following table lists the feature privileges that are enabled or disabled by default for the Governance Administrator role in Human Tasks:

| Features | Status |
|----------|--------|
| Development | Enabled |
| View Human Task Application | Enabled |
| View Tasks | Enabled |

## Governance Owner role

A user with the Governance Owner role has the privileges assigned in Administrator to perform certain tasks and manage assets in Data Governance and Catalog and Data Marketplace.

### Data Governance and Catalog

The following table lists the feature privileges that are enabled or disabled by default in Data Governance and Catalog for the Governance Owner role:

| Features | Status |
|----------|--------|
| Access Data Governance and Catalog Application | Enabled |
| Execute Data Access Management | Disabled |
| Export | Enabled |
| Force Delete | Disabled |
| Import | Enabled |
| Manage Tickets | Disabled |
| Participate in Change Approvals | Enabled |
| Preview Data | Enabled |

### Data Marketplace

The following table lists the feature privileges that are enabled or disabled by default in Data Marketplace for the Governance Owner role:

| Features | Status |
|----------|--------|
| Access Data Marketplace | Enabled |
| Approve or Reject Orders | Disabled |
| Cancel Your Orders And Data Collection Requests | Enabled |
| Complete or Reject Data Collection Requests | Disabled |
| Configure And Manage Data Marketplace | Disabled |
| Fulfill Or Reject Orders | Disabled |
| View Set up page | Disabled |
| Withdraw Consumer Accesses | Disabled |

## Governance User role

A user with the Governance User role is assigned specific privileges in Administrator that assist in working with features and assets in Data Governance and Catalog and Data Marketplace.

### Data Governance and Catalog

The following table lists the feature privileges that are enabled by default for the Governance User role in Data Governance and Catalog:

| Features | Status |
|----------|--------|
| Access Data Governance and Catalog Application | Enabled |
| Execute Data Access Management | Disabled |
| Export | Enabled |
| Force Delete | Disabled |
| Import | Disabled |
| Manage Tickets | Disabled |
| Participate in Change Approvals | Disabled |
| Preview Data | Disabled |
| View Data Access Audit | Enabled **Note:** This privilege is for a future release. |
| View Data Access Management | Enabled |

### Data Marketplace

The following table lists the feature privileges that are enabled by default for the Governance User role in Data Marketplace:

| Features | Status |
|----------|--------|
| Access Data Marketplace | Enabled |
| Approve or Reject Orders | Disabled |
| Cancel Your Orders And Data Collection Requests | Enabled |
| Complete or Reject Data Collection Requests | Disabled |
| Configure And Manage Data Marketplace | Disabled |
| Fulfill Or Reject Orders | Disabled |
| View Set up page | Disabled |
| Withdraw Consumer Accesses | Disabled |
