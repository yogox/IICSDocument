# Data collections

A data collection is a grouping of one or more related data assets.

You can use relevant keywords to search for a data collection that meets your requirements. For more information about how you can search for data collections, see the Search and access data collections topic in the Working With Data Collections help.

To view the details of a data collection, click the data collection. When you open a data collection, the page contains several tabs.

The following image shows an example of a data collection page:

![Image depicting the Summary tab on a data collection page.](../aa-introduction-and-getting-started/images/GUID-71A6F2DB-D319-4DEC-B4F1-216B4575E51D-low.png)

## Summary tab

On the Summary tab, you can view the properties of a data collection.

**Prerequisites**

To view the properties of a data collection, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see [Predefined roles](../aa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for categories, data collections and usage contexts.

### Data Collection Summary section

The following table describes the fields in the Data Collection Summary section:

| Field | Description |
|-------|-------------|
| Reference ID | Reference identifier of the data collection. |
| Purpose | Purpose of the data collection as defined by a stakeholder of the data collection. As a Data User, you can refer to this description to determine if you need the data to make business decisions. |
| Category | Name of the category that contains the data collection. |
| Certified Use | The uses for which the data is best suited as specified by the stakeholders of the data collection. |

For more information about how you can modify or delete a data collection, see the Working with Data Collections help.

### Additional information section

View additional details about a data collection that are specified by a stakeholder of the data collection. The fields that appear in the Additional Information section are configured by your Administrator in Metadata Command Center. The Additional Information section displays only the fields for which the stakeholder has specified a value. The empty fields remain hidden until the stakeholder adds a value to them.

For more information about these fields, see the Create custom attributes for objects topic in the Set Up Data Marketplace help.

### Stakeholders section

View the users or user groups that are responsible for the data collection. For more information, see [Stakeholders tab](#stakeholders-tab).

### Metrics section

View the essential metrics of a data collection in the form of pie charts and bar charts. This information can help you to decide whether or not the data suits your business needs. Pie charts provide information about the usage context and delivery templates of data collection. Bar charts provide information about the number of consumer access and order timeline details.

The metrics section of a data collection page displays the following two pie charts:

What it's used for? This pie chart shows the usage contexts that the users have entered while placing orders for a data collection. This pie chart displays the breakdown of usage contexts for all active consumer accesses of the data collection.

The pie chart displays the following four segments:

• The top three usage contexts are represented in three different segments.
• The Other segment denotes the remaining usage contexts specified by users.

A legend helps you to understand what each segment represents. At the center of the pie chart, you can find the total number of usage contexts. When you hover over the pie chart, a list of all the usage contexts associated with this data collection is displayed.

Where it's used? This pie chart represents the delivery templates used for the data collection. It displays the top three delivery templates, and the Other segment indicates all the remaining delivery templates used for this data collection. Hover over this pie chart to see the breakdown of all the delivery templates.

The following image depicts the metrics section:

![Image depicting the pie charts on the Metrics section.](../aa-introduction-and-getting-started/images/GUID-B5E7A373-D8DF-45E7-9F37-256E765128F4-low.png)

The metrics section also displays three bar charts to indicate the timeline of the data collection orders, number of consumer accesses, and the average delivery time.

• The Orders bar chart indicates the order timeline and displays the number of orders at each stage of processing the data collection order. The timeline of an order has three stages: requested, approval, and fulfillment stage.
• The Consumers bar chart displays the number of active consumer accesses for the data collection.
• The Delivery bar chart denotes the average time taken for approval and fulfillment of the order.

### Data Quality Per Asset section

View the data quality score for each data asset available on the Data Assets tab.

The following image depicts an example of the Data Quality Per Asset section on a data collection page:

![Image depicting the data quality scores of all the data assets associated to the data collection.](../aa-introduction-and-getting-started/images/GUID-D8AFAD05-19EF-43CD-8C04-316FC9EFEF15-low.png)

You can use these data quality metrics to determine the reliability of your data. Data Marketplace uses distinct colors to visualize the metrics. These colors allow you to distinguish helpful data from unhelpful data according to the target and threshold values defined in Data Marketplace or in Data Governance and Catalog.

Your Data Marketplace Administrator uses REST APIs to manage the scores of each asset. For Data Governance and Catalog assets, the scores are measured in a data quality system and are imported from Data Governance and Catalog.

For more information about data quality rules, see the Viewing data quality scores topic in the Set Up Data Marketplace help.

### Similar Data section

View the data collections that a stakeholder has linked to the collection that you are viewing.

As a Data User, you can use this section to identify data collections that are similar to the collection that you are viewing. You can then use the Compare button to add the data collections to the Compare page, and you can use the compare feature to determine the data collection that meets your business requirements. If the Similar Data section contains an unpublished data collection, you cannot click it to navigate to the details page of the unpublished collection.

A stakeholder of the data collection is responsible for linking data collections that are similar to the one for which they are responsible. For more information about how you can link similar data collections, see the Linking data collections topic in the Working With Data Collections help.

## Data Assets tab

On the Data Assets tab, you can view all the data assets that are part of a data collection and also view the data elements that are part of the data assets that comprise the collection.

The Data Assets tab contains the following grids:

• Data Assets
• Data Elements

### Data Assets grid

**Prerequisites**

To view the data assets of a data collection, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see [Predefined roles](../aa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data assets and data collections.
  ▪ Read permission is enabled in Metadata Command Center for Data Governance and Catalog business assets, data classifications and technical assets, including the Profiling attribute group for technical assets.

In this grid, you can view all the data assets that are part of the data collection. If you want to view the data asset page of an asset, click the data asset that you want to open. If you want to show or hide a column in the Data Asset grid, click the Settings icon . To revert to the default view, click Reset.

The following table describes the fields in the Data Assets grid:

| Field | Description |
|-------|-------------|
| Reference ID | Reference identifier of the data asset. |
| Name | Name of the data asset. For a data asset that was imported from Data Governance and Catalog, the Name field displays the business name of the data asset. If no business name is specified for the data asset in Data Governance and Catalog, the Name field displays the technical name of the data asset. |
| Description | Description of the data asset. For a data asset that was imported from Data Governance and Catalog, the Description field displays the description of the data asset specified in Data Governance and Catalog. |
| Data Source | Source system from which the data is supplied to Data Marketplace. |
| Descriptive Source | Source application from which the description of the data asset is taken. |
| Type | Type of the data asset. A data asset can have one of the following types: Native Data Asset. The data asset was created in Data Marketplace. Governed Data Asset. The data asset was imported from Data Governance and Catalog. |
| Asset Link | Link to the associated asset in Data Governance and Catalog. |
| Source Path | Location of the data asset in the source system where the data asset is stored. |
| Source Path Description | Description of the location in the source system where the data asset is stored. |
| Technical Data Asset | Name of the data asset as it appears in the source system where the data asset is stored. |
| Status | Status of the data asset. The status indicates whether the data asset is available to be added to data collections. A data asset can have one of the following statuses: Enabled. The data asset is available. Disabled. The data asset isn't available. |
| Created | Date when the data asset was created. |
| Data Quality | Data quality score of the data asset as calculated in a data quality system. |
| Average Score | Average of the data quality score for the data asset. |
| Last updated | Latest date when the data asset was modified. |
| Rating | Rating of the associated asset in Data Governance and Catalog. |

### Data Elements grid

**Prerequisites**

To view the data elements of a data asset, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see [Predefined roles](../aa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data assets, data collections and data elements.
  ▪ Read permission is enabled in Metadata Command Center for Data Governance and Catalog business assets, data classifications and technical assets, including the Profiling attribute group for technical assets.

In the Data Elements grid, you can view the data elements that a data asset contains. To find a specific data element, enter the name of data element in the search bar and click Search. When you search for a data element, ensure that the following conditions are fulfilled:

• The search term that you enter must not exceed 1000 characters.
• If you want to use a reserved word to search for a data element, enter the reserved word in quotes. For more information about reserved words, see [Reserved words](#reserved-words).
• If your search query contains a special character, ensure that you enter your search query in quotes.

The following table describes the fields in the Data Elements grid:

| Field | Description |
|-------|-------------|
| Reference ID | Reference identifier of the data element. |
| Name | Name of the data element. For a data element that was imported from Data Governance and Catalog, the Name displays the technical name of the data element. |
| Description | Description of the data element. For a data element that was imported from Data Governance and Catalog, Data Marketplace displays the business description of the data element. If no business description is specified for the data element in Data Governance and Catalog, the Description field displays the technical description of the data element. |
| Business Name | Business name of a data element as defined in Data Governance and Catalog. You can also hover your cursor over the business name of an element to view its business description. An element's business name and business description are defined in Data Governance and Catalog. In Data Governance and Catalog, technical assets might have user-friendly business names assigned to them. Users can assign the business names manually, or the system can automatically assign the names. For more information, see the Enrich technical assets with governance context topic in the Asset Management help for Data Governance and Catalog. |
| Type | Type of the data element. |
| Technical Name | Name of the data element as it appears in the source system where the data element is stored. |
| Technical Type | Type of the data element as defined in the source system where the data element is stored. |
| URI | URL path of the source system where the data asset is stored. |
| Status | Status of the data element. A data element can have one of the following statuses: Enabled. The data element is available. Disabled. The data element isn't available. |
| Data Asset | Name of the data asset to which the data element is associated. |
| Data Quality | Data quality score of the data element as calculated in a data quality system. |

The Data Elements grid displays additional profiling information obtained from Data Governance and Catalog. You can view the following profiling information for a data element that is imported from Data Governance and Catalog:

• Nulls / Distinct / Non-Distinct
• Glossary
• Classification
• Source Data Type
• Inferred Data Type

For more information about how to add a data asset and add data element to a data asset, see the Set Up Data Marketplace help.

### Reserved words

Reserved words are words that are reserved for specific functions in Data Marketplace.

The reserved words include the following words:

• ALL
• ARE
• TYPE
• AND
• ANY
• AS
• CONTAINING
• DAY
• DAYS
• EQUALS
• GREATER
• HOUR
• HOURS
• HAS
• IN
• INBOUND
• IS
• LAST
• LESS
• BETWEEN
• MATCHING
• NOT
• NULL
• OR
• OUTBOUND
• RELATED
• TRAVERSE
• REPEAT
• UNTIL
• HOPS
• UNBOUNDED
• RELATIONSHIPS
• ROLE
• THAN
• THROUGH
• TO
• WHERE
• WHICH
• WITH
• WITHIN
• WITHOUT
• HAVING
• STAKEHOLDER

**Note:** If you want to use a reserved word to search for a data asset or a data element, enter the reserved word in quotes.

## Delivery tab

On the Delivery tab, you can select a delivery target for the data collection.

**Prerequisites**

To view the delivery options of a data collection, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see [Predefined roles](../aa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data collections, delivery formats, delivery methods, delivery targets and delivery templates.

The following table describes the fields in the Delivery Targets grid:

| Field | Description |
|-------|-------------|
| Default | Indicates whether or not the delivery target is the default delivery option of the data collection. |
| Reference ID | Reference identifier of the delivery target. |
| Target | Name of the delivery target. |
| Status | Status of the delivery target. The status indicates whether the delivery target is available for use to the Data Users that order the data collection. A delivery target can have one of the following statuses: Active. The delivery target is available. Inactive. The delivery target isn't available. |
| Type | The type of delivery. If the delivery type is Automatic, the order approval and fulfillment is automated. If the delivery type is Manual, one or more stakeholders of the data collection must approve and fulfill the order manually. |
| Format | Format in which the data is delivered. |
| Method | Method used to deliver the data. |
| System | Systems for which you want to specify the data. |
| Description | Description of the delivery target. |
| Delivery Owner | Name of the users that manage the delivery template on which the delivery target is created. |

For more information about configuring a delivery target for a data collection, see the Specifying delivery targets for data collection topic in the Working With Data Collections help.

## Terms of use tab

On the Terms of Use tab, you can view the terms of use that are guidelines for appropriate use of a data collection.

**Prerequisites**

To view the terms of use associated with the data collection, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see [Predefined roles](../aa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data collections and terms of use.

The following table describes the sections on the Terms of Use tab:

| Section | Description |
|---------|-------------|
| General Terms of Use | View the terms of use that apply to all the data collections in Data Marketplace. |
| Terms of Use Types | View the terms of use configured by your Administrator for the data in Data Marketplace. A stakeholder can specify the following types of terms of use for a data collection: Accessible, Controlled, Restricted |
| Terms of Use | View the terms of use that you must to agree to use the data collection. |

For more information about adding terms of use to a data collection, see the Adding terms of use to a data collection topic in the Working With Data Collections help.

## Stakeholders tab

On the Stakeholders tab, you can view the stakeholders of the data collection. Stakeholders are authorized users that are responsible for a data collection and the data within it.

**Prerequisites**

To view the stakeholders of a data collection, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see [Predefined roles](../aa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data collections.

The following table describes the fields in the Stakeholders grid:

| Field | Description |
|-------|-------------|
| Stakeholder Role | Name of the stakeholder role that is assigned to the user or user group. For more information about a stakeholder role, see the Use Metadata Command Center to enrich Data Marketplace objects topic in the Set Up Data Marketplace help. |
| Stakeholder Name | Name of the user or user group that is assigned as the stakeholder of the data collection. |
| Stakeholder Assignment | This field indicates whether or not a stakeholder is inherited from the category of the data collection. This field can have one of the following values: Inherited. The stakeholder is inherited from the category. Specifically Assigned. The stakeholder is assigned directly to the data collection. |

For more information about how you can modify the stakeholders of a data collection, see the Modifying stakeholders of a data collection topic in Working With Data Collections help.

## Consumers tab

On the Consumers tab, you can view the records that indicate a Data User's access to a data collection.

**Prerequisites**

To view the consumer access for the data collection, verify one of the following prerequisites:

- Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see [Predefined roles](../aa-introduction-and-getting-started/Predefined_roles.html).
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace privilege is enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for consumer accesses and data collections.

The following table describes the fields in the Consumer Access Details grid:

| Field | Description |
|-------|-------------|
| Access ID | Reference identifier of a consumer access. |
| Consumer | Name of the Data User that has access to the data collection. |
| Fulfilled | Data when the order was fulfilled. |
| Usage Context | The context within which the data is used as specified by the Data User at the time of order. |
| Status | Status of the consumer access. A consumer access can have one of the following statuses: **Available**. The Data User has access to the data collection. **Pending Withdraw**. A request is submitted to withdraw the Data User's access to the data collection. **Withdrawn** . The Data User's access to the data collection is withdrawn. |

For more information, see the Consumer accesses topic in the Working with Data Collections help.

## Approve tab

On the Approve tab, you can view the orders placed by Data Users to gain access to the data collection.

**Prerequisites**

To view this tab, verify one of the following prerequisites:

- Your user profile is assigned the Data Marketplace Administrator user role.
- You are either an inherited or specifically assigned stakeholder with one of the following stakeholder roles on the data collection:
  ▪ Data Owner
  ▪ Category Owner
- You are assigned as a stakeholder on the data collection and your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace and Approve or Reject Orders privileges are enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data collections, orders and usage contexts.

The following table describes the fields in the Orders grid:

| Field | Description |
|-------|-------------|
| Order | Reference identifier of the order. |
| Consumer | Name of the Data User that ordered the data collection. |
| Ordered | Date on which the data collection was ordered. |
| Usage Context | The context within which the data is to be used if the order is fulfilled as specified by the Data User. |
| Business Justification | The reason for the requirement of access to the data provided by the Data User at the time of order. |
| Assigned To | The delegate of the order. This field can have one of the following values: Me. The order is assigned to you. My Group. The order is assigned to your group. All. The order is assigned to a user or group whose information is accessible to you. |

To approve or reject an order, click the Action Menu icon and select Approve or Reject. For more information about order approval, see the Responding to orders topic in the Working with Data Collections help.

## Fulfill tab

On the Fulfill tab, you can view approved orders that await fulfillment.

**Prerequisites**

To view this tab, verify one of the following prerequisites:

- Your user profile is assigned one of the following user roles:
  ▪ Technical Administrator
  ▪ Data Marketplace Administrator
- You are either an inherited or specifically assigned stakeholder with one of the following stakeholder roles on the data collection:
  ▪ Technical Owner
  ▪ Category Owner
- You are assigned as a stakeholder on the data collection and your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace and Fulfill Or Reject Orders privileges are enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for data collections, orders and usage contexts.

The following table describes the fields in the Orders grid:

| Field | Description |
|-------|-------------|
| Order | Reference identifier of the order. |
| Consumer | Name of the Data User that ordered the data collection. |
| Ordered | Date on which the data collection was ordered. |
| Usage Context | The context within which the data is to be used if the order is fulfilled as specified by the Data User. |
| Business Justification | The reason for the requirement of access to the data provided by the Data User at the time of order. |
| Assigned To | The delegate of the order. This field can have one of the following values: Me. The order is assigned to you. My Group. The order is assigned to your group. All. The order is assigned to a user or group whose information is accessible to you. |

For more information about order fulfillment, see the Fulfilling orders topic in the Working with Data Collections help.

## Withdraw tab

On the Withdraw tab, you can view the requests to remove the Data Users' access to data collections.

**Prerequisites**

To view this tab, verify one of the following prerequisites:

- Your user profile is assigned one of the following user roles:
  ▪ Technical Administrator
  ▪ Data Marketplace Administrator
- You are either an inherited or specifically assigned stakeholder with the Technical Owner stakeholder role on the data collection.
- You are assigned as a stakeholder on the data collection and your user profile is assigned a role for which the following privileges and permissions are enabled:
  ▪ Access Data Marketplace and Withdraw Consumer Accesses privileges are enabled in Administrator.
  ▪ Read permission is enabled in Metadata Command Center for consumer accesses, data collections and usage contexts.

The following table describes the fields in the Withdraw Requests grid:

| Field | Description |
|-------|-------------|
| Access | Reference identifier of a consumer access. |
| Requested By | Name of the user that requested the access withdrawal. |
| Consumer | Name of the Data User that has access to the data. |
| Requested | Date on which the access withdrawal request was submitted. |
| Usage Context | The context within which the data is used as specified by the Data User at the time of order. |
| Business Justification | Reason for the access withdrawal. |
| Assigned To | The delegate of the withdrawal request. This field can have one of the following values: Me. The withdrawal request is assigned to you. My Group. The withdrawal request is assigned to your group. All. The withdrawal request is assigned to a user or group whose information is accessible to you. |

For more information about consumer access withdrawal, see the Withdrawing consumer accesses topic in the Working with Data Collections help.

## Order section

In the Order section, you can check out the data collection that you are viewing or send it to the Compare page to compare it with the other collections that interest you.

**Checkout**

On the Order section, you can use the Checkout button to submit a request to gain access to a data collection that meets your requirements. For more information about how you can order a data collection, see the Ordering data collections topic in the Working with Data Collections help.

**Compare**

On the Order section, you can use the Compare button to add the data collection to the Compare page. On the Compare page, you can compare data collections to determine the collection that best suits your needs.

For more information about how you can compare data collections, see the Comparing data collections topic in the Working with Data Collections help.

You can view the Order section on the following tabs of a data collection page:

• Summary
• Data Assets
• Delivery
• Terms of Use
