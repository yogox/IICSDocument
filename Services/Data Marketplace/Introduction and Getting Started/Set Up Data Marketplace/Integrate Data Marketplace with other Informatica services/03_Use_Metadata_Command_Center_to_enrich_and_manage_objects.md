# Use Metadata Command Center to enrich and manage objects

You can use Metadata Command Center to further customize Data Marketplace.

In Metadata Command Center, you can create custom attributes for Data Marketplace objects. This allows you to enter additional information about the Data Marketplace objects according to the business needs of your organization.

You can also use Metadata Command Center to modify the prefix value of the reference IDs of Data Marketplace objects. This allows you to define a Data Marketplace object notation that accurately reflects the notation that you have for your organization.

You can also leverage metadata access control in Metadata Command Center to manage the level of user access to the objects in your Data Marketplace through a set of rules called access policies.

## Implement access controls on metadata

As your organization's data rapidly evolves, a robust and centralized mechanism to control access to objects becomes crucial to effectively manage the objects in your organization. Metadata access control is the practice of managing the level of user access to objects in your organization through a set of rules called access policies.

With metadata access control, you can view and perform actions on specific objects or groups of objects only if your organization administrator has explicitly granted access and permissions to you through access policies. This ensures that with appropriate permissions the right users have access to the right objects.

Your administrator can define access policies in Metadata Command Center that allow them to:

• Specify the objects that users can interact with.
• Control the individual aspects of an object, providing different levels of access to different users.
• Define the users that can assume stakeholder responsibilities for an object.

For information about managing access policies, see the Administration help in Metadata Command Center.

### Key concepts

To understand how you can apply metadata access controls on Data Marketplace objects, you must understand the following concepts.

**Access policies**

Access policies are sets of rules that the organization administrator creates in Metadata Command Center to define permissions and control the level of access to the objects in the organization.

Access policies are an extension of the privileges that are granted to your user role through Administrator. Along with the feature privileges that are assigned to the user roles in Administrator, your organization administrator must create and assign access policies in Metadata Command Center that determine whether users can read, create, update, delete or manage access for the objects. Administrators can use predefined policies or define custom policies specific to their organization in Metadata Command Center. Predefined policies are associated with predefined user roles defined in Administrator.

**Asset groups**

Asset groups is a mechanism in metadata access control that administrators can use to control access to a set of objects. By grouping objects, you can grant or restrict access to multiple objects at a time.

You can use asset groups in access policies to control access to a group of objects among users based on parameters such as their location, business area, or function within the organization. You can assign asset groups to the categories in Data Marketplace. Access policies associated with an asset group are also applied to the subcategories and data collections of a category to which you have assigned an asset group.

**Stakeholder roles**

A stakeholder role is a defined organizational responsibility that you declare on objects such as a category or a data collection. Stakeholder roles allow you to control how authorized users interact with the objects for which they are responsible.

A stakeholder role reflects a user's responsibilities as a stakeholder of an object and allows them to perform tasks with only the necessary permissions and privileges. In Metadata Command Center, you can create stakeholder roles from user roles and use them in access policies to grant users granular access to objects.

Unlike with Informatica Intelligent Cloud Services user roles that allow users to perform actions across Data Marketplace, a user with a stakeholder role can only perform actions on the assets on which they are assigned as a stakeholder. For example, a user that is assigned with the Data Marketplace Administrator user role can perform various actions such as create, modify or delete data assets. On the other hand, a user that is assigned as a stakeholder of a category with the Category Owner stakeholder role can only manage their respective category and the subcategories and data collections within it.

For more information about metadata access control, see the Administration help in Metadata Command Center.

### Example 1

Connect2Con is a global telecom company that is a leading provider of internet and mobile communication services. Connect2Con uses Data Marketplace to provide its employees with access to timely and trusted data so that they can make faster and better-informed business decisions.

**Problem statement**

The company uses Data Marketplace, which has some data collections that contain sensitive data such as employee salary figures, bonus details, and performance records. Though Connect2Con believes in generally democratizing data for all its employees, it wants to draw boundaries around sensitive data. Only the HR leadership team should have access to sensitive employee data to make HR-related decisions.

**Solution**

Connect2Con can use asset groups in access policies to manage the visibility of sensitive HR data. They can group these data collections in a separate category that only approved users can access.

With metadata access control in Data Marketplace, Connect2Con can restrict access to sensitive data collections in a few simple steps:

1. Create a dedicated category in Data Marketplace called HR-Sensitive and add related data collections that contain sensitive employee data to this category.
2. In Administrator, define a user group called HR Leadership and assign this user group only to users who require access to sensitive HR data.
3. In Metadata Command Center, create an asset group named HR-Leaders and assign this asset group to the HR-Sensitive category in Data Marketplace.
4. In Metadata Command Center, create a user group-based access policy for the HR Leadership user group with a rule granting read permission on assets with the HR-Leaders asset group.

After the access policy is published, users in the HR Leadership user group can access the data collections in the HR-Sensitive category, ensuring confidentiality and compliance.

### Example 2

Utsukushi is a Japanese cosmetics company that specializes in luxury beauty products. Utsukushi uses Data Marketplace to provide its employees with access to timely and trusted data so that they can make faster and better-informed business decisions.

**Problem statement**

The company is looking to expand into the EMEA market. To achieve this, they are seeking to purchase a London based beauty products company. Utsukushi wishes to ensure that the data pertaining to the acquisition remain available in Data Marketplace only to the senior leadership of the company and the other stakeholders that are key participants in the acquisition.

**Solution**

Utsukushi can use asset groups in access policies to manage the visibility of sensitive data that pertains to the acquisition of the London based beauty products company. They can group these data collections in a separate category that only approved users can access.

With metadata access control in Data Marketplace, Utsukushi can restrict access to sensitive data collections in a few simple steps:

1. Create a dedicated category in Data Marketplace called Mergers and Acquisitions and add related data collections that contain sensitive data to this category.
2. In Administrator, define a user group called Mergers and Acquisitions Team and assign this user group only to users who require access to the data pertaining to the acquisition.
3. In Metadata Command Center, create an asset group named M&A Team and assign this asset group to the Mergers and Acquisitions category in Data Marketplace.
4. In Metadata Command Center, create a user group-based access policy for the Mergers and Acquisitions Team user group with a rule granting read permission on assets with the M&A Team asset group.

After the access policy is published, users in the Mergers and Acquisitions Team user group can access the data collections in the Mergers and Acquisitions category, ensuring confidentiality and compliance.

## Manage reference IDs of objects

The reference ID is a unique identifier that is assigned to a Data Marketplace object. This reference ID can be automatically assigned by Data Marketplace or you can manually enter it.

When you create an object, Data Marketplace automatically assigns a unique value to the object. When Data Marketplace generates a reference ID, it uses the following format:

<prefix>-<value>

You can also choose to specify an object's reference ID at the time of creation. If you specify a reference ID, ensure that the value that you enter doesn't use a prefix value that is configured in Metadata Command Center. For example you can specify Category01 or CT-1 as the reference ID of a category. However, if CAT- is a reference ID prefix that is configured in Metadata Command Center, you cannot use CAT-1. When you try to modify the properties of an object, you can also modify its reference ID.

For more information about how you can modify the prefix value of a reference ID in Metadata Command Center, see the Prefix values for asset reference IDs topic in the Administration help for Metadata Command Center.

## Create custom attributes for objects

Custom attributes are additional properties for Data Marketplace objects that are defined by your Administrator in Metadata Command Center.

**How can I create a custom attribute?**

In Metadata Command Center, your Administrator can create custom attributes for your Data Marketplace objects.

To create a custom attribute for a Data Marketplace object, on the New Attribute page in Metadata Command Center, set the Asset Type to data collection or order.

For more information about how you can create or manage custom attributes in Metadata Command Center, see the Asset customization topic in the Administration help for Metadata Command Center.

**Where can I view the custom attributes that I created?**

After your Administrator configures a custom attribute in Metadata Command Center for your Data Marketplace instance, you can view the property on the following pages:

- The Summary > Additional Information section of a data collection page
- The Request Details section of the Order Checkout wizard
- The Additional Information and Timeline sections of an order page

The custom attributes are also available in the applicable bulk create templates of the objects for which your Administrator configured the attributes in Metadata Command Center.

**How can I use custom attributes?**

A stakeholder of a data collection can use custom attributes to specify additional information about a data collection when the standard properties of the collection are insufficient. Additionally, Data Users that order the data collection can use the newly added property to provide more information when they place an order.

For example, in Metadata Command Center, if your Administrator creates a custom attribute called Region, a stakeholder can use the newly added Region property to specify the region for which their data collection is relevant. A Data User can use the information specified in the Region property to determine whether the data suits their business requirement.
