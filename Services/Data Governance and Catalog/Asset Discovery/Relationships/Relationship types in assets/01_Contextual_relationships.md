You can create the following types of relationships that provide contexts to assets.

**Relationships that indicate business dependency**
 If your governance activities require business assets to be related to each other, you can create relationships between the assets.
 For example, if you want users in your organization who read the "Medical Reimbursement" policy document to understand the cost reimbursement process related to it, you can create a relationship that indicates that the "Medical Reimbursement" policy asset 'Is Related to' the "Costs Reimbursement" process asset.

**Relationships that add semantic context to technical assets**
 Add user-friendly contexts to your technical assets so that they can be easily identified in Data Governance and Catalog.
 For example, if you have three tables called CustName, cust_name and Customers, you can create a relationship between these tables and the "Customer Name" glossary asset.

**Relationships that add governance context to technical assets**
 When you create a relationship between a data set and a technical asset, the data set becomes a metadata layer that enables you to perform governance activities on the technical asset.
 For example, you can relate the "Customer Name" data set with the CustName, cust_name and customers tables. Now you can perform governance activities on the tables such as assigning stakeholders, requiring approvals for modifications, or viewing the lineage of the table data.

For more information about the types of contextual relationships that you can create among assets, see Types of direct relationships.

**Related Topics**

Relationship types in assets
