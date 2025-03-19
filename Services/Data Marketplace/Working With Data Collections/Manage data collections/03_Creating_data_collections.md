# Creating data collections

A data collection refers to one or more data assets that are bundled together. Data Users can place an order to gain access to the data collections that you create.

To perform this task, verify one of the following prerequisites:

- Your user profile is assigned one of the following roles:
  - Data Owner
  - Category Owner
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Create, Manage Access, Read and Update permissions are enabled in Metadata Command Center for data collections.
  - Read permission is enabled in Metadata Command Center for categories and usage contexts.

1. On the New page, click the Data Collection tile.

   The following table describes the fields that you can configure on the New Data Collection page:

   | Field | Description |
   | --- | --- |
   | Reference ID | Enter a reference identifier for the data collection. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see the Manage reference IDs of objects topic in the Set Up Data Marketplace help. |
   | Name | Enter a name for the new data collection as you want it to appear in Data Marketplace. Enter a name that represents the data that it contains. |
   | Purpose | Enter a purpose for the new data collection. Enter a descriptive text so that Data Users can easily find the data collection. You can explain the nature of the data and the purpose for which it was created so that users can decide whether it meets their business requirements. You can also upload an image to this field. Data Marketplace only supports .jpg,.jpeg and .png type images. |
   | Status | Select a status for the data collection. The status determines whether the data collection is discoverable by Data Users when they search for it. - To make the data collection discoverable to Data Users, set the status to Published. - To make the data collection not discoverable to Data Users, set the status to Unpublished. |
   | Category | Select a category for the data collection. A category contains related data collections that are bundled together. It is possible that the applicable category that you select is a subcategory to another category. For more information about categories, see the Categories topic in the Set Up Data Marketplace help. **Note:** If a category is added to an asset group for which you aren't assigned the required permissions, the Category field won't display the category. If the category that contains your data collection becomes inactive, your data collection will not be discoverable to Data Users on the Browse and Search pages. If you select a category that is added to an asset group that requires additional permissions, Data Users won't be able to discover the data collection when they browse Data Marketplace for relevant data. For more information about asset groups, see the Implement access controls on metadata topic in the Set Up Data Marketplace help. |
   | Certified Use | Select the most suitable use for the data. |

   **Note:** If your Administrator configured custom attributes in Metadata Command Center for data collections in Data Marketplace, you can view additional fields in the Additional Information section. You can use these fields to specify additional information about the data collection. For more information, see the Create custom attributes for objects topic in the Set Up Data Marketplace help.

2. In the Stakeholders section, click Add to specify the users that will be responsible for the new data collection and the data within it.

3. In the Add Stakeholders dialog box, select a role, and then select the users or user groups that you want to assign as stakeholders of the data collection.

   To remove a stakeholder, click the Delete icon next to the stakeholder that you want to remove from the Selected Stakeholders section.

   **Note:** When you configure stakeholders for a data collection, consider the following:

   - Ensure that the users that you want to add as the stakeholders of the data collection are already assigned the relevant user role in Administrator. For example, if you want to assign a user as a Data Owner of a data collection, the user must already be assigned the Data Owner user role in Administrator. Additionally, ensure that the relevant user role is configured as a stakeholder role for data collections in Metadata Command Center. For more information, see the Use Metadata Command Center to enrich and manage objects in the Set Up Data Marketplace help.
   - The Users section displays only the users that are directly assigned the relevant user role. If a user is added to a user group that is assigned the relevant user role, the Users section won't display the user.
   - If you don't assign a stakeholder to the new data collection, you can modify the data collection after its creation only if you are a Data Marketplace Administrator or are assigned the Configure and Manage Data Marketplace privilege in Metadata Command Center.

4. Click Save.

## Adding data assets to a data collection

To enrich your data collections, you can use data assets native to Data Marketplace or data assets imported from Data Governance and Catalog.

To perform this task, verify one of the following prerequisites:

- Your user profile is assigned one of the following user roles:
  - Technical Administrator
  - Data Marketplace Administrator
- You are either an inherited or specifically assigned stakeholder with one of the following stakeholder roles on the data collection:
  - Data Owner
  - Technical Owner
  - Category Owner
- You are assigned as a stakeholder on the data collection and your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Read and Update permissions are enabled in Metadata Command Center for data assets and data collections.

1. Open a data collection. 

   For more information about how you can find a data collection, see [Browsing for data collections](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Browsing_for_data_collections.html).

2. On Data Assets tab of the data collection page, click Add to add new data assets to the collection.

3. In the Add Assets grid, you can search for a Data Marketplace or a Data Governance and Catalog asset by the asset name. You can also use filters to assist you with searching for the appropriate asset.

   To view the data elements that constitute an asset, click the asset to reveal the Data Elements grid for the selected asset.

   **Note:** When you add data assets to data collections, consider the following:

   - If a Data Governance and Catalog asset is added to an asset group for which you aren't assigned the required permissions, the Add Assets grid won't display the data asset. For more information about asset groups, see the Implement access controls on metadata topic in the Set Up Data Marketplace help.
   - When the Add Assets grid is available, you can view the data elements only for the assets that you want to add to the data collection. To view the data elements that comprise a data asset that is already added to the data collection, close the Add Assets grid.
   - If you want to utilize a delivery target that is based on a Managed Access enabled template, ensure that you select only the assets that belong to the same source system. For more information about how you can assign a delivery target to a data collection, see [Specifying delivery targets for data collection](#specifying-delivery-targets-for-data-collection).

   ![Image depicting the Data Assets tab on a data collection page. The Add Assets section is encircled.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/images/GUID-60C5AAE9-85C0-441C-8E21-A392AF05503B-low.png)

4. Click Add.

   You can view the newly added data asset on the Data Assets tab of the data collection page. When you add a Data Governance and Catalog asset to a data collection, the Overview page of the asset in Data Governance and Catalog indicates that the asset is published to Data Marketplace. Additionally, you can view in Data Governance and Catalog the details of data collection to which the asset was added.

5. Click Close to close the Add Assets grid.

To remove a data asset, click the Action menu icon next to the data asset that you want to remove, and click Remove. In the Remove dialog box that appears, click Remove Data Asset.

If you want to modify the data elements that comprise the data asset, contact your administrator.

**Note:** If you add a data asset to a data collection or remove a data asset from a data collection, your changes may take some time to reflect on the Search page.

## Specifying delivery targets for data collection

A delivery target is a delivery option that you as a stakeholder of a data collection can use to deliver data to a Data User. Stakeholders use delivery templates to create new delivery targets for their data collections. To ensure that you can fulfill an order, ensure that you configure a delivery target for your data collection.

To perform this task, verify one of the following prerequisites:

- Your user profile is assigned one of the following user roles:
  - Technical Administrator
  - Data Marketplace Administrator
- You are either an inherited or specifically assigned stakeholder with one of the following stakeholder roles on the data collection:
  - Data Owner
  - Technical Owner
  - Category Owner
- You are assigned as a stakeholder on the data collection and your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Create and Read permissions are enabled in Metadata Command Center for delivery targets.
  - Read and Update permissions are enabled in Metadata Command Center for data collections.
  - Read permission is enabled in Metadata Command Center for delivery formats, delivery methods and delivery templates.

1. Open a data collection. 

   For more information about how you can find a data collection, see [Browsing for data collections](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Browsing_for_data_collections.html).

2. On the Delivery tab of the data collection page, click New.

3. In the New Delivery Target dialog box, configure the properties of the new delivery target.

   The following table describes the fields that you can configure in the New Delivery Target dialog box:

   | Field | Description |
   | --- | --- |
   | Delivery Template | Select the delivery template based on which you want to create the delivery target. For more information delivery templates, see the Delivery options topic in the Set Up Data Marketplace help. **Note:** If the Managed Access option is enabled for the delivery template that you selected, ensure that the data collection for which you are creating this target is comprised only of data assets that belong to the same source system. For more information about how you can add data assets to a data collection, see [Adding data assets to a data collection](#adding-data-assets-to-a-data-collection). |
   | Reference ID | Enter a reference identifier for the delivery target. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see the Manage reference IDs of objects topic in the Set Up Data Marketplace help. |
   | Delivery Target | Enter a name for the delivery target. |
   | Description | Enter a description for the delivery target. Enter a description that helps Data Users understand the utility of the delivery target. |
   | Status | Select a status for the delivery target. The status determines whether the delivery target is available for use to the Data Users that order the data collection. You can select one of the following options: - To make the delivery target available, select Active. - To make the delivery target unavailable, select Inactive. |
   | System | Enter the systems for which you want to specify the data. |
   | Location | Specify a location where the data collection is to be delivered. Enter the system URL of the location in this field. |
   | Type | The delivery type. This field can have the following values: - Manual. Stakeholders of the data collection must approve and fulfill the order manually. - Automatic. The order approval and fulfillment is automated. For more information about how you can use an automatic type delivery target, see [Automated deliveries](#automated-deliveries). |
   | Format | The delivery format. |
   | Method | The delivery method. |
   | Delivery Owners | Name of the users that manage the delivery template based on which you want to create the delivery target. |

4. Click Save.

You can also modify the delivery targets that you have created. For more information about how you can modify a delivery target, see [Modifying delivery targets](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Modifying_data_collections.html#ww3_9_15_10_1).

### Automated deliveries

If a data collection that you own requires no approval to be accessed, you can configure an automatic type delivery target for the data collection. This greatly simplifies the ordering experience of the Data User that orders the data collection.

The following image shows the overall process of how a data collection whose delivery is automated is delivered to a Data User that ordered it:

![Image depicting the overall process of how a data collection whose delivery is automated is delivered to a Data User that ordered it.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/images/GUID-8C82E6F2-B3B7-4C26-AEBD-F66F1FEFD75A-low.png)

**Note:** The process flow is illustrated using the predefined roles for Data Marketplace.

**Example 1. Example**

In a food and beverage company, Arthur and Gawain are the administrators of all of the websites in the organization. One of the website that Arthur manages is used solely by the employees to get updates that relate to the organization. At the end of the calendar year, Arthur must use an XLSX sheet that is present in a shared SFTP folder to update the organization's holiday calendar on the website.

Vivienne is the Human Resources manager in the organization. She has prepared an XLSX sheet that lists the holidays for the upcoming year and has uploaded the file to a shared FTP folder. The shared FTP folder is configured to be accessible to everyone in the organization. As a Data Owner, she also publishes the data to the "Holiday List" data collection within the "Human Resources" category in Data Marketplace.

Gareth works in the Human Resources department with Vivienne. He is the Technical Owner of the "Holiday List" data collection. He uses an automatic type delivery template that represents the shared SFTP folder to create the delivery target of the "Holiday List" data collection.

Arthur calls in sick and therefore Gawain must complete the task in Arthur's absence. Unlike Arthur, Gawain is unaware of the file path of the XLSX sheet. Gawain uses the keyword "holiday" to search in Data Marketplace and sees the "Holiday List" data collection that Vivienne had published. He places an order for the data collection. As soon as the order is placed, it is delivered and Gawain receives the file path to the XLSX sheet that Vivienne had published.

For more information about how you can configure a delivery target for a data collection, see [Specifying delivery targets for data collection](#specifying-delivery-targets-for-data-collection).

**Note:** The preceding example uses the predefined roles for Data Marketplace.

## Adding terms of use to a data collection

You can specify the terms of use for a data collection that exists in Data Marketplace. The terms of use that you specify are displayed on the checkout page when a Data User orders a data collection.

To perform this task, verify one of the following prerequisites:

- Your user profile is assigned one of the following user roles:
  - Technical Administrator
  - Data Marketplace Administrator
- You are either an inherited or specifically assigned stakeholder with one of the following stakeholder roles on the data collection:
  - Data Owner
  - Technical Owner
  - Category Owner
- You are assigned as a stakeholder on the data collection and your user profile is assigned a role for which the following permissions and privileges are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Read and Update permissions are enabled in Metadata Command Center for data collections.
  - Read permission is enabled in Metadata Command Center for terms of use.

1. Open a data collection. 

   For more information about how you can find a data collection, see [Browsing for data collections](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Browsing_for_data_collections.html).

2. On the Terms of Use tab of the data collection, click Add.

3. In the Add Terms of Use dialog box, select the applicable terms of use.

   ![Image depicting the Add Terms of Use dialog box.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/images/GUID-D4033906-7894-4FE7-9CD2-576191752D2C-low.png)

4. Click Add to save your changes and exit the dialog box.

   If you want to add more than one terms of use, click Add and Select Another.

   **Note:** A Data User can check out a data collection only if the Usage Guide step in the Order Checkout wizard contains the General Terms Of Use and Terms of Use.

To remove a terms of use, click the Action menu icon next to the terms of use that you want to remove, and click Remove. In the Remove dialog box that appears, click Yes.

For more information about the terms of use, see the Terms of use topic in the Set Up Data Marketplace help.
