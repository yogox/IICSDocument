# Use cases

The following use cases illustrate how you can use metadata access control to effectively manage access to the assets in your organization:

- [Use case: Control access to unpublished glossary changes](../ad-asset-management/Use_cases.html#ww3_9_23_6_1)
- [Use Case: Cross-unit glossary collaboration](../ad-asset-management/Use_cases.html#ww3_9_23_9_1)

## Use case: Control access to unpublished glossary changes

*HypoStores* is a popular online shopping retail company that offers a wide range of products, from clothing to electronics. HypoStores uses Data Governance and Catalog to manage its data assets effectively.

### Problem statement

The *HypoStores* business is growing, and the website team needs to keep the business glossary updated with product categories, pricing models, and promotional terms. The glossary stewards collaborate with stakeholders to update and finalize the glossary definitions. In the meantime, they want to make sure that only the glossary stewards have access to the unpublished changes. Otherwise, confidential information might be leaked.

### Solution

*HypoStores* can use attribute groups in access policies to explicitly grant glossary stewards in their organization access to assets that contain unpublished or draft changes. Users other than glossary stewards

With access control in Data Governance and Catalog, the organization administrator can perform a few simple steps:

1. In Administrator, define a user role called *Glossary Steward* and assign this role to users who manage glossary assets in the organization.
2. In Metadata Command Center, create and publish a user role-based access policy for the *Glossary Steward* role. The access policy can contain the following rules:
   - Grant data stewards permissions to create, read, update, and manage access on business asset types. This grants data stewards permissions to all lifecycle statuses of business assets.
   - Grant read permission on the Unpublished Changes attribute group for all business asset types.

After the access policy is published in Metadata Command Center, users with the *Glossary Steward* role can access the unpublished changes or the draft version of the business assets in Data Governance and Catalog.

## Use Case: Cross-unit glossary collaboration

*Acme Inc.* is a finance company that provides loans, credit and other financial services. *Acme Inc.* uses Data Governance and Catalog for compliance, data quality, and collaboration.

### Problem Statement

The company has three separate business units that want to work together on a common enterprise glossary. While they need to collaborate on the common glossary, each unit has its own assets that must stay private and separate from the others for security, legal, and operational reasons.

### Solution

*Acme Inc.* can use asset groups to segregate assets based on the business units that use them, ensuring that only the employees of a particular business unit can interact with the business unit's assets.

With metadata access control in Data Governance and Catalog, *Acme Inc.* can segregate assets using asset groups while ensuring collaboration among employees in a few simple steps:

1. In Metadata Command Center, create an asset group called *Acme Inc*.
2. Under the *Acme Inc* asset group, create three child asset groups that correspond to the business units. For example, create: *Acme France*, *Acme UK*, and *Acme India*.
3. Assign each child asset group to the corresponding assets from each business unit and assign the parent asset group to common glossary assets that all users can collaborate on.
4. Use these asset groups in access policies to grant different levels of user access for each asset group. Each asset group can have the following rules:
   - Grant read permission to data stewards to view all technical and business assets that belong to the asset group.
   - Grant read permission to business users to view all business assets that belong to the asset group.
   - Grant read permissions to all users to view glossary assets that are assigned to the *Acme Inc* asset group.

After the access policies are published and the assets are assigned to asset groups, only users that are part of each asset group will have permission to interact with the assets in those groups. All users can collaborate on the glossary assets that belong to the parent asset group.
