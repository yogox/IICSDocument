A data access policy is a set of rules that you can use to protect data and control access to your data. For example, you can write a data access policy around a regulation such as HIPAA or GDPR, or around a business objective such as provisioning data for marketing analytics.

As a Data Steward, you can create data access control policies, data filter policies, and data de-identification policies on the Data Access Management page.

The following image shows the Data Access Management page where you start to define data access policies:

![The image shows the Data Access Management page, which includes a top navigation options for Data Access Control, Data Filter, and Data De-identification. The user has selected Data De-identification. The three sub-tabs are Data De-identification, Data Protection, and Precedence Tier. A plus sign appears for creating a new data de-identification. Filter and sort options also appear.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-ACB49ED0-66EA-42D7-A395-1E9D93212CEE-low.png)

You use data access control policies to grant read, write, or delete access to a table or a view in a specified source system.

You use data filter policies to filter out records that Data Consumers should not access due to their role or location.

You use data de-identification policies to remove, alter, or otherwise protect the columns and values in each data asset that the given user can access. Each data de-identification policy contains one or more data de-identification rules, which contain data protections that define which data de-identification techniques to apply to the data.
