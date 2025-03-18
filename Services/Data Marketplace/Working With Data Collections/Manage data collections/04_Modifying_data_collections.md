# Modifying data collections

You can modify the properties of a data collection for which you or your group is assigned as a stakeholder.

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
  - Read and Update permissions are enabled in Metadata Command Center for data collections.
  - Read permission is enabled in Metadata Command Center for categories and usage contexts.

1. Open a data collection. 

   For more information about how you can find a data collection, see Browsing for data collections.

2. On the Summary tab of the data collection page, click Edit to modify the Data Collection Summary section.

   The following table describes the fields that you can configure in the Data Collection Summary section:

   | Field | Description |
   |-------|-------------|
   | Reference ID | Enter a reference identifier for the data collection. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see the Manage reference IDs of objects topic in the Set Up Data Marketplace help. |
   | Name | Enter a name for the data collection. |
   | Purpose | Enter a purpose for the data collection. Enter a descriptive text so that Data Users can easily find the data collection. You can explain the nature of the data and the purpose for which it was created so that users can decide whether it meets their business requirements. You can also upload an image to this field. Data Marketplace only supports .jpg, .jpeg and .png type images. |
   | Status | Select a status for the data collection. The status determines whether the data collection is discoverable by Data Users when they search for it. - To make the data collection discoverable to Data Users, set the status to Published. - To make the data collection not discoverable to Data Users, set the status to Unpublished. Note: If you modify the status of a data collection to Unpublished after it is ordered by a Data User, the stakeholders of the collection can still fulfill the order. |
   | Category | Select a category for the data collection. A category contains related data collections that are bundled together. It is possible that the applicable category that you select is a subcategory to another category. For more information about categories, see the Categories topic in the Set Up Data Marketplace help. Note: If a category is added to an asset group for which you aren't assigned the required permissions, the Category field won't display the category. If the category that contains your data collection becomes inactive, your data collection will not be discoverable to Data Users on the Browse and Search pages. If you select a category that is added to an asset group that requires additional permissions, Data Users won't be able to discover the data collection when they browse Data Marketplace for relevant data. For more information about asset groups, see the Implement access controls on metadata topic in the Set Up Data Marketplace help. |
   | Certified Use | Select the most suitable use for the data. |

   If your Administrator configured custom attributes in Metadata Command Center for data collections in Data Marketplace, you can view additional fields in the Additional Information section. You can use these fields to specify additional information about the data collection.

3. Click Save.

## Modifying stakeholders of a data collection

You can modify the stakeholders of a data collection. Stakeholders are authorized users that are responsible for a data collection and the data within it.

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
  - Read, Manage Access and Update permissions are enabled in Metadata Command Center for data collections.
  - Read permission is enabled in Metadata Command Center for categories.

1. Open a data collection. 

   For more information about how you can find a data collection, see Browsing for data collections.

2. On the Stakeholders tab of the data collection, click Edit.

3. In the Users section on the Edit Stakeholders dialog box, select a role, and then select the users or user groups that you want to assign as stakeholders of the data collection.

   To remove a stakeholder, click the Delete icon next to the stakeholder that you want to remove from the Selected Stakeholders section.

   Note: When you modify the stakeholders of a data collection, consider the following:

   - Ensure that the users that you want to add as the stakeholders of the data collection are already assigned the relevant user role in Administrator. For example, if you want to assign a user as a Data Owner of a data collection, the user must already be assigned the Data Owner user role in Administrator. Additionally, ensure that the relevant user role is configured as a stakeholder role for data collections in Metadata Command Center. For more information, see the Use Metadata Command Center to enrich and manage objects in the Set Up Data Marketplace help.
   - The Users section displays only the users that are directly assigned the relevant user role. If a user is added to a user group that is assigned the relevant user role, the Users section won't display the user.
   - If you modify the stakeholders of a data collection, your changes may take some time to reflect on the Data Marketplace interface. While the system updates the stakeholders for the data collection, you can't modify the properties of the data collection, the data assets and data elements within it, and all the categories in the hierarchy of the data collection's category.

4. Click OK.

## Modifying delivery targets

You can modify the delivery target of a data collection for which you or your group is assigned as a stakeholder.

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
  - Read and Update permissions are enabled in Metadata Command Center for data collections and delivery targets.
  - Read permission is enabled in Metadata Command Center for delivery formats, delivery methods and delivery templates.

1. Open a data collection. 

   For more information about how you can find a data collection, see Browsing for data collections.

2. On the Delivery tab of the data collection page, click the Action menu icon and click Edit to modify a delivery target.

   Note: You cannot modify a delivery target that you have configured as the default delivery option of the data collection.

3. In the Edit Delivery Target dialog box, you can modify the properties of a delivery target.

   The following table describes the fields that you can configure in the Edit Delivery Target dialog box:

   | Field | Description |
   |-------|-------------|
   | Delivery Template | The delivery template based on which the delivery target was created. Note: You cannot modify this field. |
   | Reference ID | Enter the reference identifier of the delivery target. If you don't specify a reference identifier, Data Marketplace automatically assigns a unique value to the object. If you want to specify a reference identifier, enter a unique alphabetical, numeric or alphanumeric value. You can also use special characters when you enter a reference identifier value. Ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For more information about reference IDs, see the Manage reference IDs of objects topic in the Set Up Data Marketplace help. |
   | Delivery Target | Enter a name for the delivery target. |
   | Description | Enter a description for the delivery target. Enter a description that helps Data Users understand the utility of the delivery target. |
   | Status | Select a status for the delivery target. The status determines whether the delivery target is available for use to the Data Users that order the data collection. You can select one of the following options: - To make the delivery target available, select Active. - To make the delivery target unavailable, select Inactive. |
   | System | Enter the systems for which you want to specify the data. |
   | Location | Specify a location where the data collection is to be delivered. Enter the system URL of the location in this field. |
   | Type | The delivery type. This field can have the following values: - Manual. Stakeholders of the data collection must approve and fulfill the order manually. - Automatic. The order approval and fulfillment is automated. For more information about how you can use an automatic type delivery target, see Automated deliveries. |
   | Format | The delivery format. |
   | Method | The delivery method. |
   | Delivery Owners | Name of the users that manage the delivery template based on which you want to create the delivery target. |

4. Click Save.

## Deleting delivery targets

If you created a delivery target accidentally or if a delivery target is obsolete, you can delete it.

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
  - Delete and Read permissions are enabled in Metadata Command Center for delivery targets.
  - Read and Update permissions are enabled in Metadata Command Center for data collections.

1. Open a data collection. 

   For more information about how you can find a data collection, see Browsing for data collections.

2. In the Delivery Targets grid on the Delivery tab of a data collection page, click the Action menu icon next to the delivery target that you want to delete.

   Note: You cannot delete a delivery target that you have already configured as the default delivery option for a data collection. You cannot delete a delivery target that is associated with a consumer access or an order. For more information about how you can delete an order, see Delete orders topic in the API Reference help.

3. In the action menu, click Delete.

4. In the Delete Delivery Target dialog box, click Delete.
