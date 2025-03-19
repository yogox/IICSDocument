# Consumer accesses

A consumer access is a record that indicates a Data User's access to a data collection, along with other details such as the date of delivery, details of the stakeholder that delivered the data, and the delivery option that was used for the delivery.

## View consumer access details

On a consumer access page, you can view details of your access to a data collection and the details of the order used to deliver the collection to you.

The following image shows a consumer access page:

![Image depicting a consumer access page.](../bb-working-with-data-collections/images/GUID-6F224737-20EF-43FE-BB24-DADCBA1DC3E9-low.png)

**Prerequisites**

To view a consumer access, verify one of the following prerequisites:

- The consumer access record is created for your access to the data collection and your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see the Predefined roles topic in the Introduction and Getting Started help.
- Your user profile is assigned one of the following user roles:
  - Technical Administrator
  - Data Marketplace Administrator
- You are either an inherited or specifically assigned stakeholder with one of the following stakeholder roles on the data collection that is associated with the consumer access:
  - Data Owner
  - Technical Owner
  - Category Owner
- You are assigned as a stakeholder on the data collection that is associated with the consumer access and your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Read permission is enabled in Metadata Command Center for consumer accesses, data collections, delivery formats, delivery methods, delivery targets, orders, terms of use and usage contexts.

**Delivery section**

The following table describes the fields that you can view in the Delivery section:

| Field | Description |
|-------|-------------|
| Target | Name of the delivery target used to deliver the data collection. |
| Description | Description of the delivery target used to deliver the data collection. |
| Type | The delivery type. This field can have the following values: <br>- Manual. Stakeholders of the data collection must approve and fulfill the order manually. <br>- Automatic. The order approval and fulfillment is automated. |
| Managed Access | A delivery setting that determines whether or not a unique location was created at the time of order fulfillment. <br>- If Managed Access is enabled, the data is made available in a location that is unique to this consumer access. <br>- If Managed Access is disabled, the same data is made available in a data location that is common to all Data Users. |
| Format | Format in which the data was delivered. |
| Method | Medium that was used to deliver the data to you. |
| System | Name of the system where the data was delivered. |
| Location | Location where the data is delivered. <br>If Managed Access is enabled for the target that is used for the delivery, the data is delivered to a location that is unique to the consumer access that you are viewing. For more information about how you can access the data that was delivered using Data Access Management, see the Data Access Management help.<br>**Note:** By default, the location details are visible if the system can verify one of the following prerequisites: <br>- You are the user that was granted access to the data collection that is associated with the consumer access. <br>- You are a stakeholder of the data collection for which the consumer access was created. <br>- Your user profile is assigned the Data Marketplace Administrator role or has the Configure and Manage Data Marketplace privilege enabled for it in Administrator. |

**Timeline section**

In the Timeline section, you can view a summary of the actions and comments that users have made on the consumer access, along with the timestamp of each action or comment.

**Data collection section**

In the data collection section, you can view the details of the delivered data collection. To view more details of the data collection that was delivered, hover your cursor over the data collection details section.

**Orders section**

The following table describes the fields that you can view for the order that was used to deliver the data collection:

| Field | Description |
|-------|-------------|
| Usage Context | The context within which the data is used as specified by the Data User at the time of order. |
| Business Justification | A brief description about how the Data User plans to use the data. |
| Approved By | Name of the stakeholder that approved the order. |
| Fulfilled By | Name of the stakeholder that fulfilled the order. |

**Terms of Use section**

In the Terms of Use section, you can view the terms of use that apply to the data collection.

**Stakeholders section**

In the Stakeholders section, you can view the names of the stakeholders that responsible for the ordered data collection.

## View consumer accesses

On the History page, you can view all the consumer accesses in Data Marketplace.

To view consumer accesses on the History page, verify the following prerequisites:

- Your user profile is assigned one of the following roles:
  - Data Owner
  - Technical Owner
  - Category Owner
  - Technical Administrator
  - Data Marketplace Administrator
- You are assigned as a stakeholder on a data collection and your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Approve or Reject Orders, Fulfill Or Reject Orders, Withdraw Consumer Accesses or Configure Data Marketplace privilege is enabled in Administrator.
  - Read permission is enabled in Metadata Command Center for categories, consumer accesses, data collections, delivery targets, delivery templates and usage contexts.

1. Open the History page.

![This image depicts the Consumer Access tab on the History page.](../bb-working-with-data-collections/images/GUID-7EE8A684-5A2B-424D-AE02-07564CF89F7E-low.png)

2. On the History > Consumer Access tab, you can view the list of consumer accesses.

The following table describes the fields that you can view in the Consumer Access Details grid:

| Column | Description |
|--------|-------------|
| Access | Reference identifier for the consumer access. |
| Consumer | Name of the Data User that ordered the data collection. |
| Data Collection | Name of the ordered data collection. |
| Delivery Target | Name of the delivery target used to deliver the data collection. |
| Delivery Template | Name of the delivery template that was used to create the delivery target. |
| Business Justification | A brief description about how the Data User plans to use the data. |
| Category | Name of the category of the data collection. |
| Access Granted | Date when the Data User received access to the data collection. |
| Usage Context | The reason for the requirement of access to the data provided by the Data User at the time of order. |
| Status | Status of the consumer access. A consumer access can have one of the following statuses: <br>- **Available**. The Data User has access to the data collection. <br>- **Pending Withdraw**. A request is submitted to withdraw the Data User's access to the data collection. <br>- **Withdrawn**. The Data User's access to the data collection is withdrawn. |
| Assigned To | The delegate of the fulfilled order. This field can have one of the following values: <br>- Me. The fulfilled order is assigned to you. <br>- My Group. The fulfilled order is assigned to your group. <br>- All. The fulfilled order is assigned to a user or group whose information is accessible to you. |

To filter the consumer accesses that are displayed in the Consumer Access Details grid, click Filter and select the filter that you want to use. After you configure the filter, click Filter again to curate the grid based on how you configured the filter.

For example, if you want to view only the consumer accesses that are available, click Filter and select the Status filter. In the Status filter, select the Available status and click Filter again to apply it. After you apply the filter, the Consumer Access Details grid displays only the consumer accesses that are available.

3. To view the details of a consumer access, click the access ID in the Access column.

4. To view the details of a data collection, click the data collection name in the Data Collection column.

5. To view the details of a category, click the category name in the Category column.

## Requesting withdrawal of consumer accesses

As a stakeholder if you determine that a Data User no longer requires access to the data, or as a Data User if you think that you don't require access to the data, you can submit a request to revoke the consumer access from the data collection.

To perform this task, verify one of the following prerequisites:

- The consumer access record is created for your access to the data collection.
- Your user profile is assigned one of the following user roles:
  - Technical Administrator
  - Data Marketplace Administrator
- You are either an inherited or specifically assigned stakeholder with one of the following stakeholder roles on the data collection that is associated with the consumer access:
  - Data Owner
  - Technical Owner
  - Category Owner
- You are assigned as a stakeholder on the data collection that is associated with the consumer access and your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Approve or Reject Orders, Fulfill Or Reject Orders, Withdraw Consumer Accesses or Configure Data Marketplace privilege is enabled in Administrator.
  - Read and Update permissions are enabled in Metadata Command Center for consumer accesses and data collections.
  - Read permission is enabled in Metadata Command Center for categories, delivery targets, delivery templates and usage contexts.

1. On your My Data page, open the consumer accesses for a data collection to which you are granted access or to a data collection for which you are assigned as a stakeholder.

For more information about the My Data page, see the My Data page topic in the Introduction and Getting Started help.

2. In the Timeline section of the consumer access page, click Request Withdrawal.

Optionally, you can enter your comments on why the access must be revoked. To tag a user to your comment, add @ to populate the list of users. You can use either the name of the user or the user's email address to search for them.

**Note:** Ensure that the user you tagged is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see the Predefined roles topic in the Introduction and Getting Started help.

Alternatively, ensure that their user profile is assigned a role for which the following privileges and permissions are enabled:

- Access Data Marketplace privilege is enabled in Administrator.
- Read permission is enabled in Metadata Command Center for consumer accesses.

Without these privileges and permissions, they won't be able to access your comment despite receiving the notification for it.

After you submit an access withdrawal request, the status of the consumer access changes from Available to Pending Withdraw. For more information about how a consumer access is withdrawn, see Withdrawing consumer accesses (参照先は#withdrawing-consumer-accesses).

## Withdrawing consumer accesses

On the Tasks page, you can respond to a request to withdraw a Data User's access to a data collection.

To perform this task, verify the following prerequisites:

- Your user profile is assigned one of the following user roles:
  - Technical Administrator
  - Data Marketplace Administrator
- You are assigned as a stakeholder with the Technical Owner stakeholder role on the data collection to which the access is to be revoked.
- You are assigned as a stakeholder on the data collection that is associated with the consumer access and your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace and Withdraw Consumer Accesses privileges are enabled in Administrator.
  - Read and Update permissions are enabled in Metadata Command Center for consumer accesses and data collections.
  - Read permission is enabled in Metadata Command Center for categories and usage contexts.

1. Open the Tasks page.

![Image depicting the Withdraw tab on the Tasks page.](../bb-working-with-data-collections/images/GUID-286B50EE-3CB1-41D2-B642-C78F6AC11D44-low.png)

2. On the Tasks > Withdraw tab, you can view all the pending consumer access withdrawal requests.

The following table describes the fields that you can view in the Withdrawal Requests grid:

| Field | Description |
|-------|-------------|
| Access | Reference identifier of the consumer access. |
| Requested By | Name of the user that requested the access withdrawal. |
| Consumer | Name of the Data User that has access to the data. |
| Requested | Date on which the access withdrawal request was submitted. |
| Category | Name of the category of the data collection. |
| Data Collection | Name of the data collection for which the consumer access is to be withdrawn. |
| Usage Context | The context within which the data is used as specified by the Data User at the time of order. |
| Business Justification | Reason for the access withdrawal. |
| Assigned To | The delegate of the withdrawal request. This field can have one of the following values: <br>- Me. The withdrawal request is assigned to you. <br>- My Group. The withdrawal request is assigned to your group. <br>- All. The withdrawal request is assigned to a user or group whose information is accessible to you. |

To filter the consumer accesses that are displayed in the Withdrawal Requests grid, click Filter and select the filter that you want to use. After you configure the filter, click Filter again to curate the grid based on how you configured the filter.

For example, if you want to view only the consumer accesses that are requested to be withdrawn this month, click Filter and select the Requested filter. In the Requested filter, select This month and click Filter again to apply it. After you apply the filter, the Withdrawal Requests grid displays only the consumer accesses that are requested to be withdrawn this month.

3. To withdraw a Data User's access to a collection, click the Action menu, and select Withdraw Access.

In the Withdraw Access dialog box, click Withdraw Access. Optionally, you can enter your comments to explain the reason behind the action taken. To tag a user to your comment, add @ to populate the list of users. You can use either the name of the user or the user's email address to search for them.

**Note:** Ensure that the user you tagged is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see the Predefined roles topic in the Introduction and Getting Started help.

Alternatively, ensure that their user profile is assigned a role for which the following privileges and permissions are enabled:

- Access Data Marketplace privilege is enabled in Administrator.
- Read permission is enabled in Metadata Command Center for consumer accesses.

Without the aforementioned privileges and permissions, they won't be able to access your comment despite receiving the notification for it.

4. To cancel a withdrawal request, click the Action menu, and select Cancel Withdrawal.

In the Cancel Withdrawal dialog box, click Cancel Withdrawal. Optionally, you can enter your comments to explain the reason behind the action taken.

5. Alternatively, you can respond to a withdrawal request from the consumer access page. To do this, open a consumer access. In the Timeline section of the consumer access page, click Withdraw Access.

Optionally, you can use the Add Comment field to explain the reason behind the action taken.

The status of the consumer access changes from Pending Withdraw to Withdrawn.
