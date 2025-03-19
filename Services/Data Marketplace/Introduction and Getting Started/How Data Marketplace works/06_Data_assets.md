# Data assets

A representation of data in an organization. Data assets may contain relevant data elements and are contained in one or more data collections.

Data assets are the building blocks with which stakeholders create their data collections. Besides using Data Governance and Catalog assets, stakeholders can also use data assets native to Data Marketplace to enrich their data collections.

## Summary tab

On the Summary tab, you can view the properties of a data asset.

### Native data asset

**Prerequisites**

To view the properties of a native data asset, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see Predefined roles (参照先のパスはaa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data assets.

**Data Asset Summary panel**

The following table describes the fields in the Data Asset Summary panel:

| Field | Description |
|-------|-------------|
| Reference ID | Reference identifier of the data asset. |
| Name | Name of the data asset. |
| Description | Description of the data asset as defined. |
| Data Source | Source system from which the data is supplied to Data Marketplace. |
| Descriptive Source | Source application from which the description of the data asset is taken. |
| Source Path | Location of the data asset in the source system where the data asset is stored. |
| Source Path Description | Description of the location in the source system where the data asset is stored. |
| Technical Data Asset | Name of the data asset as it appears in the source system where the data asset is stored. |
| Type | Type of the data asset. In this field, you can also view the following tags that are appended by Data Marketplace to the data asset: - Native Data Asset. The data asset was created in Data Marketplace. - Governed Data Asset. The data asset was imported from Data Governance and Catalog into Data Marketplace. |
| Asset Link | Link to the associated asset in Data Governance and Catalog. |
| Status | Status of the data asset. A data asset can have one of the following statuses: - Enabled. The data asset is available. - Disabled. The data asset is not available. |

**Add to Data Collection section**

In the Add to Data Collection section, add the data asset to an existing data collection or use the data asset details to create a new data collection for the data asset. For more information, see Data Assets (参照先のパスはcc-setup-data-marketplace/Data_Assets.html) in the Set Up Data Marketplace help.

**Associated Data Collections section**

In the Associated Data Collections section, you can view all the data collections that contain the data asset. For more information, see Data Collections tab (参照先パスはaa-introduction-and-getting-started/Data_collections.html#data-collections-tab).

**Metrics section**

In the Metrics section, you can view the data quality metrics for the data asset. For more information, see Data Quality tab (参照先パスはaa-introduction-and-getting-started/Data_collections.html#data-quality-tab).

Typically, a Data Marketplace Administrator is responsible for creating and managing Data Marketplace data assets. For more information about creating or modifying a data asset, see Data Assets (参照先パスはcc-setup-data-marketplace/Data_Assets.html) in the Set Up Data Marketplace help.

### Governed data asset

**Prerequisites**

To view the properties of a Data Governance and Catalog asset, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see Predefined roles (参照先パスはaa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data assets.
  ▪ Read permission is enabled in Metadata Command Center for Data Governance and Catalog business assets and technical assets.

If you have assets in Data Governance and Catalog that are well governed and which can be used for business decision making, you can quickly load them into Data Marketplace.

If you want to modify an asset that was imported from Data Governance and Catalog, open the asset in Data Governance and Catalog. For more information about how you can modify a Data Governance and Catalog asset, see the Data Governance and Catalog help.

**Data Asset Summary panel**

The following table describes the fields in the Data Asset Summary panel:

| Field | Description |
|-------|-------------|
| Reference ID | Reference identifier of the data asset. |
| Name | Name of the data asset as defined in Data Governance and Catalog. |
| Description | Description of the data asset as defined in Data Governance and Catalog. |
| Data Source | Source system from which the data is supplied to Data Governance and Catalog. |
| Descriptive Source | Source application from which the description of the data asset is taken. |
| Source Path | Location of the data asset in the source system where the data asset is stored. |
| Source Path Description | Description of the location in the source system where the data asset is stored. |
| Technical Data Asset | Name of the data asset as it appears in the source system where the data asset is stored. |
| Type | Type of the data asset. In this field, you can also view the following tags that are appended by Data Marketplace to the data asset: - Native Data Asset. The data asset was created in Data Marketplace. - Governed Data Asset. The data asset was imported from Data Governance and Catalog into Data Marketplace. |
| Asset Link | Link to the associated asset in Data Governance and Catalog. |
| Status | Status of the data asset. A data asset can have one of the following statuses: - Enabled. The data asset is available. - Disabled. The data asset is not available. |

In the Additional Information section of the Data Asset Summary panel, you can view additional details about an asset that are specified in Data Governance and Catalog. The fields that appear in the Additional Information section are configured for the asset in Metadata Command Center.

When an asset is imported from Data Governance and Catalog into Data Marketplace, the system also retrieves its rating. A rating in Data Governance and Catalog represents a user's assessment of an asset. Data Governance and Catalog users rate assets between one to five stars. The value that you see is the average of the ratings provided by all the Data Governance and Catalog users. You can refer to the rating of a Data Governance and Catalog asset to gauge its reliability.

For more information about Data Governance and Catalog assets, see the Working With Assets help in Data Governance and Catalog.

**Add to Data Collection section**

In the Add to Data Collection section, add the data asset to an existing data collection or use the data asset details to create a new data collection for the data asset. For more information, see Data Assets (参照先パスはcc-setup-data-marketplace/Data_Assets.html) in the Set Up Data Marketplace help.

**Associated Data Collections section**

In the Associated Data Collections section, you can view all the data collections that contain the data asset. For more information, see Data Collections tab (参照先パスはaa-introduction-and-getting-started/Data_collections.html#data-collections-tab).

**Metrics section**

In the Metrics section, you can view the data quality metrics for the data asset. For more information, see Data Quality tab (参照先パスはaa-introduction-and-getting-started/Data_collections.html#data-quality-tab).

## Data Elements tab

On the Data Elements tab, you can view all the data elements that are part of a data asset.

**Prerequisites**

To view the data elements of a data asset, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see Predefined roles (参照先パスはaa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data assets and data elements.
  ▪ Read permission is enabled in Metadata Command Center for Data Governance and Catalog business assets, data classifications and technical assets, including the Profiling attribute group for technical assets.

On the Data Elements grid, you can view the data elements that a data asset contains. When an asset is imported from Data Governance and Catalog, Data Marketplace imports the data elements that constitute the asset. This also includes the manual data elements created in Data Governance and Catalog. For more information about Data Governance and Catalog assets, see the Asset Details help in Data Governance and Catalog.

To find a specific data element, enter the name of data element in the search bar and click Search. When you search for a data element, ensure that the following conditions are fulfilled:

• The search term that you enter must not exceed 1000 characters.
• If you want to use a reserved word to search for a data element, enter the reserved word in quotes. For more information about reserved words, see Reserved words (参照先パスはaa-introduction-and-getting-started/Data_collections.html#ww3_12_18_11_7_1).
• If your search query contains a special character, ensure that you enter your search query in quotes.

The following table describes the fields in the Data Elements grid:

| Field | Description |
|-------|-------------|
| Reference ID | Reference identifier of the data element. |
| Name | Name of the data element. For a data element that was imported from Data Governance and Catalog, the Name field displays the technical name of the data element specified in Data Governance and Catalog. |
| Description | Description of the data element. For a data element that was imported from Data Governance and Catalog, the Description field displays the business description of the data element. If no business description is specified for the data element in Data Governance and Catalog, the Description field displays the technical description of the data element. |
| Business Name | The business name of a data element as defined in Data Governance and Catalog. You can hover your cursor over the business name of an element to view its business description. An element's business name and business description are defined in Data Governance and Catalog. In Data Governance and Catalog, technical assets might have user-friendly business names assigned to them. Users can assign the business names manually, or the system can automatically assign the names. For more information, see the Enrich technical assets with governance context topic in the Asset Management help for Data Governance and Catalog. |
| Type | Type of the data element. |
| URI | URL path of the source system where the data element is stored. |
| Technical Name | Name of the data element as it appears in the source system where the data element is stored. |
| Technical Type | Type of the data element as defined in the source system where the data element is stored. |
| Status | Status of the data element. A data element can have one of the following statuses: - Enabled. The data element is available. - Disabled. The data element is not available. |
| Data Quality | Data quality score of the data element as calculated in a data quality system. |

For more information about how to add a data asset and add data element to a data asset, see Data Assets (参照先パスはcc-setup-data-marketplace/Data_Assets.html) in the Set Up Data Marketplace help.

## Data Quality tab

In the Data Quality tab of a data asset page, you can view the data quality score for each data element that constitutes the data asset.

**Prerequisites**

To view the data quality details of a data asset, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see Predefined roles (参照先パスはaa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data assets.
  ▪ Read permission is enabled in Metadata Command Center for Data Governance and Catalog business assets, data classifications and technical assets, including the Profiling attribute group for technical assets.

You can use these data quality metrics to determine the reliability of your data. Data Marketplace uses distinct colors to visualize the metrics. These colors allow you to identify helpful data using the target and threshold values defined in Data Marketplace or in Data Governance and Catalog.

Your Data Marketplace Administrator uses REST APIs to manage the scores of each asset. For Data Governance and Catalog assets, the scores are measured in a data quality system and are imported from Data Governance and Catalog into Data Marketplace.

For more information about data quality rules, see the Set Up Data Marketplace help.

## Data Collections tab

On the Data Collections tab, you can view all the data collections that contain the data asset.

**Prerequisites**

To view the data collections associated with a data asset, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see Predefined roles (参照先パスはaa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data assets and data collections.

The following table describes the fields that you can view in the Associated Data Collections grid:

| Property | Description |
|----------|-------------|
| Reference ID | Reference identifier of the data collection that contains the data asset. |
| Name | Name of the data collection. |
| Description | Description of the data collection |
| Status | Status of the data collection. A data collection can have one of the following statuses: - Published. The data collection is discoverable to Data Users. - Unpublished. The data collection isn't discoverable to Data Users. |
