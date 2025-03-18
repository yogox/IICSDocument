# Data assets

A representation of data in an organization. Data assets may contain relevant data elements and are contained in one or more data collections.

The following image shows the details page of a data asset:

![Image depicting the details page of a data asset.](../cc-setup-data-marketplace/images/GUID-33F9B2CB-E9DA-4427-ADF1-8E9896DB138E-low.png)

Data assets are the building blocks with which stakeholders can create data collections. On top of using Data Governance and Catalog assets, stakeholders can also use data assets native to Data Marketplace to enrich their data collections. As a Data Marketplace Administrator, you are responsible for creating Data Marketplace data assets. For more information about how you can create data assets, see [Creating data assets](#ww3_9_12_8_1 "Data assets").

## Creating data assets

You can add new data assets native to Data Marketplace.

To perform this task, verify the following prerequisites:

- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace and View Set up Page privileges are enabled in Administrator.
  - Create and Read permissions are enabled in Metadata Command Center for data assets.

1. Open the Setup page.
2. In the Data Assets grid on the Setup > Data Assets tab, click New.

![Image depicting the New Data Asset dialog box.](../cc-setup-data-marketplace/images/GUID-4F8B67CE-EB77-40C7-84A0-13C849F11EAC-low.png)

3. In the New Data Asset dialog box, configure the data asset properties.

The following table describes the properties of a data asset that you can configure in the New Data Asset dialog box:

| Property | Description |
| --- | --- |
| Reference ID | Enter a reference identifier for the data asset. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see [Manage reference IDs of objects](../cc-setup-data-marketplace/Use_Metadata_Command_Center_to_enrich_and_manage_objects.html#ww3_6_11_10_1 "Use Metadata Command Center to enrich and manage objects"). |
| Name | Enter a name for the data asset. |
| Description | Enter a description for the data asset. |
| Data Source | Specify the source system from which the data is supplied to Data Marketplace. |
| Descriptive Source | Specify the source application from which the description of the data asset is taken. |
| Source Path | Enter the location of the data asset in the source system where the data asset is stored. |
| Source Path Description | Enter a description for the location in the source system where the data asset is stored. |
| Technical Data Asset | Enter the name of the data asset as it appears in the source system where the data asset is stored. |
| Type | Enter a type for data asset. |
| URI | Enter a uniform resource identifier for the new data asset. |
| Status | Select a status for the data asset. The status determines whether the data asset is available to be added to data collections. - To make the data asset available, set the status to Active. - To make the data asset unavailable, set the status to Inactive. |

4. Click Save.

You can add data elements to the data asset that you created. For more information about how you can add a data element to a data asset, see [Adding data elements to a data asset](#ww3_9_12_8_8_1 "Data assets").

You can also modify the data elements that you have created. For more information about how you can modify a data element, see [Modifying data elements](#ww3_9_12_14_8_1 "Data assets").

### Adding data elements to a data asset

A data element is the smallest unit of data that is present in Data Marketplace. A grouping of one or more related data elements forms a data asset. You add a new data element to a data asset that already exists in Data Marketplace.

Before you can add a data element to a data asset, verify the following prerequisites:

Verify the privileges and permissions
: Verify one of the following:
- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Create and Read permissions are enabled in Metadata Command Center for data elements.
  - Read and Update permissions are enabled in Metadata Command Center for data assets.

Verify the data element
: Ensure that the data asset to which you want to add the data element is native to Data Marketplace.

1. Open the Setup page.
2. In the Data Assets grid on the Setup > Data Assets tab, click the data asset to which you want to add a data element.

**Note:** You can also navigate to the data asset page from the details page of a data collection that contains the asset.

3. On the Data Elements tab on the data asset page, click New.

![Image depicting the New Data Element dialog box.](../cc-setup-data-marketplace/images/GUID-3B9807D3-2882-49EE-ADB6-3BB357C371D4-low.png)

4. In the New Data Element dialog box, configure the data element properties.

The following table describes the properties of a data element that you can configure in the New Data Element dialog box:

| Property | Description |
| --- | --- |
| Reference ID | Enter a reference identifier for the data element. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see [Manage reference IDs of objects](../cc-setup-data-marketplace/Use_Metadata_Command_Center_to_enrich_and_manage_objects.html#ww3_6_11_10_1 "Use Metadata Command Center to enrich and manage objects"). |
| Name | Enter a name for the data element. |
| Description | Enter a description for the data element |
| URI | Enter a uniform resource identifier for the data element in the source system where the data element is stored. |
| Technical Name | Enter the name of the data element as it appears in the source system where the data element is stored. |
| Technical Type | Enter the type of the data element as defined in the source system where the data element is stored. |
| Type | Enter a type for data element. |
| Status | Select a status for the data element. To make the data element available, set the status to Enabled. To make the data element unavailable, set the status to Disabled. |

5. Click Save.

**Note:** If you add a data element to a data asset or remove a data element from a data asset, and the data asset belongs to a data collection, your changes may take some time to reflect on the Search page.

You can also modify the data elements that you have created. For more information about how you can modify a data element, see [Modifying data elements](#ww3_9_12_14_8_1 "Data assets").

## Searching for data assets

Use the search bar to look up data assets that are native to Data Marketplace.

The following image shows the Data Assets tab on the Setup page:

![Image depicting the Data Assets tab on the Setup page.](../cc-setup-data-marketplace/images/GUID-46E1A7C5-CEE0-4A48-B640-D03D2B716E1D-low.png)

To search for a data asset on the Setup > Data Assets tab, enter the name of data asset in the search bar, and click Search.

To search for a data asset, enter a search query for the data that you want to find in the search box, and click Search.

**Note:** When you search for data assets, consider the following:

- The search term that you enter must not exceed 1000 characters.
- If you want to use a reserved word to search for a data asset, enter the reserved word in quotes. For more information about reserved words, see [Reserved words](#ww3_9_12_11_8_1 "Data assets").
- If your search query contains a special character, ensure that you enter your search query in quotes.

You can use the Status field to filter the search results based on the status of the data assets. To clear the search box, click Clear Search.

### Reserved words

Reserved words are words that are reserved for specific functions in Data Marketplace.

The reserved words include the following words:

- ALL
- ARE
- TYPE
- AND
- ANY
- AS
- CONTAINING
- DAY
- DAYS
- EQUALS
- GREATER
- HOUR
- HOURS
- HAS
- IN
- INBOUND
- IS
- LAST
- LESS
- BETWEEN
- MATCHING
- NOT
- NULL
- OR
- OUTBOUND
- RELATED
- TRAVERSE
- REPEAT
- UNTIL
- HOPS
- UNBOUNDED
- RELATIONSHIPS
- ROLE
- THAN
- THROUGH
- TO
- WHERE
- WHICH
- WITH
- WITHIN
- WITHOUT
- HAVING
- STAKEHOLDER

**Note:** If you want to use a reserved word to search for a data asset or a data element, enter the reserved word in quotes.

## Modifying data assets

You can view and modify the properties of the data assets that are available in Data Marketplace.

Before you can modify a data asset, verify the following prerequisites:

Verify the privileges and permissions
: Verify one of the following:
- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Read and Update permissions are enabled in Metadata Command Center for data assets.
  - Read permission is enabled in Metadata Command Center for data collections.

Verify the data asset
: Ensure that the data asset that you want to modify is native to Data Marketplace. To modify a data asset that was imported from Data Governance and Catalog, open the asset in Data Governance and Catalog. For more information about how you can modify a Data Governance and Catalog asset, see the Data Governance and Catalog help.

1. Open the Setup page.
2. On the Setup > Data Assets tab, click the Action menu icon next to the data asset that you want to modify.
3. In the Action menu, click Edit.
4. In the Edit Data Asset dialog box, configure the data asset properties.

The following table describes the properties of a data asset that you can configure in the Edit Data Asset dialog box:

| Property | Description |
| --- | --- |
| Associated Data Collections | The data collections to which the data asset is added. **Note:** If a data collection associated with the data asset is added to an asset group for which you aren't assigned the required permissions. The Associated Data Collections field won't display the data collection. For more information about asset groups, see [Implement access controls on metadata](../cc-setup-data-marketplace/Use_Metadata_Command_Center_to_enrich_and_manage_objects.html#ww3_6_11_7_1 "Use Metadata Command Center to enrich and manage objects"). |
| Reference ID | Enter a reference identifier for the data asset. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see [Manage reference IDs of objects](../cc-setup-data-marketplace/Use_Metadata_Command_Center_to_enrich_and_manage_objects.html#ww3_6_11_10_1 "Use Metadata Command Center to enrich and manage objects"). |
| Name | Enter a name for the data asset. |
| Description | Enter a description for the data asset. |
| Data Source | Specify the source system from which the data is supplied to Data Marketplace. |
| Descriptive Source | Specify the source application from which the description of the data asset is taken. |
| Source Path | Enter the location of the data asset in the source system where the data asset is stored. |
| Source Path Description | Enter a description for the location in the source system where the data asset is stored. |
| Technical Data Asset | Enter the name of the data asset as it appears in the source system where the data asset is stored. |
| Type | Enter a type for data asset. |
| Asset Link | Enter a link to the Data Governance and Catalog associated asset. |
| Status | Select a status for the data asset. The status determines whether the data asset is available to be added to data collections. - To make the data asset available, set the status to Active. - To make the data asset unavailable, set the status to Inactive. **Note:** If you try to disable a data asset that is associated with one or more data collections, a confirmation dialog box appears. This dialog box lists all data collections that will be affected if you disable the data asset. To disable the data asset, click Continue. If a data asset is not associated with a data collection, you will not receive a confirmation dialog box. |

5. Click Save.

### Modifying data elements

You can modify the properties of a data element in a data asset in Data Marketplace.

Before you can modify a data element, verify the following prerequisites:

Verify the privileges and permissions
: Verify one of the following:
- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Read and Update permissions are enabled in Metadata Command Center for data elements.
  - Read permission is enabled in Metadata Command Center for data assets.

Verify the data element
: Ensure that the data element that you want to modify is native to Data Marketplace.

1. Open the Setup page.
2. In the Data Assets grid on the Setup > Data Assets tab, click the data asset whose data elements you want to modify.

**Note:** You can also navigate to the data asset page from the details page of a data collection that contains the asset.

3. On the Data Elements tab on the data asset page, enter the name of data element that you seek in the search bar and click Search.

When you search for a data element, ensure that the following conditions are fulfilled:
- The search term that you enter must not exceed 1000 characters.
- If you want to use a reserved word to search for a data element, enter the reserved word in quotes. For more information about reserved words, see [Reserved words](#ww3_9_12_11_8_1 "Data assets").
- If your search query contains a special character, ensure that you enter your search query in quotes.

4. Click the Action menu icon next to the data element that you want to modify. 
5. In the Action menu, click Edit.
6. In the Edit Data Element dialog box, configure the data element properties.

The following table describes the properties of a data element that you can configure in the Edit Data Element dialog box:

| Property | Description |
| --- | --- |
| Reference ID | Enter a reference identifier for the data element. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see [Manage reference IDs of objects](../cc-setup-data-marketplace/Use_Metadata_Command_Center_to_enrich_and_manage_objects.html#ww3_6_11_10_1 "Use Metadata Command Center to enrich and manage objects"). |
| Name | Enter a name for the data element. |
| Description | Enter a description for the data element |
| Technical Name | Enter the name of the data element as it appears in the source system where the data element is stored. |
| Technical Type | Enter the type of the data element as defined in the source system where the data element is stored. |
| Type | Enter a type for data element. |
| URI | Enter the uniform resource identifier of the data element in the source system where the data element is stored. |
| Status | Select a status for the data element. To make the data element available, set the status to Enabled. To make the data element unavailable, set the status to Disabled. |

7. Click Save.

## Adding a data asset to data collections

You can add a data asset to one or more data collections.

To perform this task, verify the following prerequisites:

- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Read and Update permissions are enabled in Metadata Command Center for data collections and data assets.

1. Open the Setup page.
2. On the Setup > Data Assets tab, click the Action menu icon next to the data asset that you want to add to data collections.
3. In the Action menu, click Add to Data Collection.
4. In the Add to Data Collection dialog box, select the data collection to which you want to add the data asset.

**Note:** When you add a data asset to a data collection, consider the following:
- If a data collection is added to an asset group for which you aren't assigned the required permissions. The Add to Data Collection dialog box won't display the data collection.
- If you select a data collection that is added to an asset group that requires additional permissions, Data Users won't be able to discover the data asset and its data elements when they browse the Search > Other Items tab for relevant data. For more information about asset groups, see the Implement access controls on metadata topic in the Set Up Data Marketplace help.

5. Click Save.

**Note:** When you add or remove a data asset from a data collection, your changes may take some time to reflect on the Search page.

## Creating a data collection from a data asset

You can create a data collection from a data asset.

To perform this task, verify the following prerequisites:

- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Create, Manage Access, Read and Update permissions are enabled in Metadata Command Center for data collections.
  - Read permission is enabled in Metadata Command Center for categories and usage contexts.
  - Read and Update permissions are enabled in Metadata Command Center for data assets.

1. Open the Setup page.
2. On the Setup > Data Assets tab, click the Action menu icon next to the data asset that you want to add to a data collection.
3. In the action menu, click Create a Data Collection.
4. On the Create Data Collection page, enter the details of the collection that you want to create and click Save.

**Note:** On the Create Data Collection page, some fields are populated automatically with values from the data asset that you select. You can use the auto-populated icon (![Auto-populated icon.](../cc-setup-data-marketplace/images/GUID-47983AE6-2E21-457D-B516-ABEC2A4E8C0A-low.png)) to identify these fields. Review the content in these fields and make the necessary adjustments.

For more information about the fields in the dialog box, see the Creating data collections topic in the Working With Data Collections help.

## Deleting data assets

If you created a data asset accidentally or if a data asset is obsolete, you can delete it.

Before you can delete a data asset, verify the following prerequisites:

Verify the privileges and permissions
: Verify one of the following:
- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Delete and Read permissions are enabled in Metadata Command Center for data assets.

Verify the data asset
: Ensure that the data asset that you want to delete is native to Data Marketplace. To delete a data asset that was imported from Data Governance and Catalog, open the asset in Data Governance and Catalog. For more information about how you can delete a Data Governance and Catalog asset, see the Data Governance and Catalog help.

1. Open the Setup page.
2. On the Setup > Data Assets tab, click the Action menu icon next to the data asset that you want to delete.
3. In the action menu, click Delete.
4. In the Delete Data Asset dialog box, click Delete.

The data asset that you selected is deleted. When you delete a data asset, the asset is removed from all the data collections that use it. Moreover, all the elements that are associated with the asset are deleted.

**Note:** You can also delete an asset from a data asset page. On a data asset page, you can use the Delete button in the Data Asset Summary panel to delete the data asset.

### Deleting data elements

If you created a data element accidentally or if a data element is obsolete, you can delete it.

Before you can delete a data element, verify the following prerequisites:

Verify the privileges and permissions
: Verify one of the following:
- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Delete and Read permissions are enabled in Metadata Command Center for data elements.
  - Read and Update permissions are enabled in Metadata Command Center for data assets.

Verify the data element
: Ensure that the data element that you want to delete is native to Data Marketplace and the Status of the data asset that contains the data element is Enabled.

1. Open the data asset page. 
2. On the Data Elements grid of the data asset page, click the Action menu icon next to the data element that you want to delete.
3. In the Action menu, click Delete.
4. In the Delete Data Element dialog box, click Delete.

The data element that you selected is deleted.

**Note:** If you add a data element to a data asset or remove a data element from a data asset, and the data asset belongs to a data collection, your changes may take some time to reflect on the Search page.
