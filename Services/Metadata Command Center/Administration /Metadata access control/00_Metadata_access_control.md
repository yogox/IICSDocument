# Manage access policies

You can create, modify, clone, disable, or delete access policies.

When you disable or delete an access policy, the rules defined in the access policy do not apply. You cannot delete predefined access policies, but you can disable or clone them.

You can manage access policies on the Access Policies tab on the Access Control page.

To search for access policies, you can use filters. To show or hide the Category and Updated By columns on the Access Policies tab, right-click any column header and select the column.

### Required privileges

To view access policies, you need the View Access Control privilege. Also, to create, view, update, and delete access policies, you need the Manage Access Control privilege.

## Creating and publishing an access policy

To create an access policy, specify the name and description and associate the access policy with a stakeholder role, user group, or user role. Define one or more rules for the access policy that determine the level of access to assets, and then publish the access policy.

1. Go to Access Control and click Access Policies.
2. Click Add, and then select the type of access policy that you want to create.

   The New Access Policy page opens on the Overview tab. The properties that appear depend on the type of access policy you select.

3. Enter the general information applicable to your access policy type.

User role policy

| Property | Description |
|----------|-------------|
| Name | A name to identify the access policy. |
| Description | Optional. A description of the access policy. |
| User Role | Select the user role that you want the access policy to apply to. |
| Override other policy types | Optional. From Advanced Settings, choose to override other access policy types if multiple access policies are enabled. |

Stakeholder role policy

| Property | Description |
|----------|-------------|
| Name | A name to identify the access policy. |
| Description | Optional. A description of the access policy. |
| Selected Role | Specify if you want the stakeholder role policy to apply to users with specific stakeholder roles or to users who are non-stakeholders. Choose from the following options: - Stakeholder. Select Stakeholder to specify a stakeholder role. - Non-Stakeholder. Select Non-Stakeholder to specify if you want the access policy to apply to both non-stakeholders and users with stakeholder roles. |
| Stakeholder Role | Required if you choose Stakeholder as the selected role. Select the stakeholder role that you want the access policy to apply to. |
| Override other policy types | Optional. From Advanced Settings, choose to override other access policy types if multiple access policies are enabled. |

User group policy

| Property | Description |
|----------|-------------|
| Name | A name to identify the access policy. |
| Description | Optional. A description of the access policy. |
| Selected Group | Specify if you want the user group policy to apply to a specific user group or to all users. Choose from the following options: - Single User Group. Select Single User Group to specify a user group - All Users. Select All Users if you want the access policy to apply to all users. |
| User Group | Required if you choose Single User Group. Select the user group that you want the access policy to apply to. |

4. Click Next.
5. Add one or more rules to define the access policy.

   You can create rules based on asset types or attribute groups.

   - Create a rule based on asset types. For information about how to create rules based on asset types, see Creating rules based on asset types.
   - Create a rule based on attribute groups. For information about how to create rules based on attribute groups, see Creating rules based on attribute groups.

6. Click Save.
7. To publish the policy, click Publish to start the publishing job.

   To discard the policy, click Discard.

### Creating rules based on asset types

You can create rules to define an access policy based on asset types.

1. On the Rules tab, click Add.

   The Condition page appears.

2. Click Add.
3. Select Asset Type.
4. For user role and stakeholder role policies, perform the following steps:
   a. Click Add New to select one or more asset types from the hierarchy and click OK. Optionally, add one or more predicates to the condition.
   b. Click Add Permission to grant permissions to users governed by the access policy.

   **Note:** The list of available permissions is based on the asset type and the predicate that you selected.

5. For a user group policy, perform the following steps:
   a. To apply the condition to specific asset groups, choose Is Any Of and click Add New.
   b. In the Select Asset Groups window, select one or more asset groups from the hierarchy and click OK.
   c. To add a condition that applies to assets that are not associated with asset groups, choose Is Null.
   d. Click Add Permission to grant permissions to users governed by the access policy.

6. Click Save.
7. To create another rule, click Add or to edit an existing rule, click Edit.

### Creating rules based on attribute groups

You can create rules to define an access policy based on attribute groups.

1. On the Rules tab, click Add.

   The Condition page appears.

2. Click Add.
3. Select Attribute Groups.
4. For user role and stakeholder role policies, perform the following steps:
   a. Click Add New and choose an attribute group.
   b. Add the condition based on your requirement.
      - To add a condition that applies to any asset type, choose Is Any.
      - To add a condition that applies to specific asset types, choose Is Any Of and click Add New. In the Select Asset Groups window, select one or more asset groups from the hierarchy and click OK.
   c. Optional. Add one or more predicates to the condition.
   d. Select the permissions to grant users governed by the access policy.

5. For a user group policy, perform the following steps:
   a. Click Add New and choose an attribute group.
   b. Add the condition based on your requirement.
      - To add a condition that applies to specific asset groups, choose Is Any Of, click Add New. In the Select Asset Group window, select the asset groups from the hierarchy and click OK.
      - To add a condition that applies to assets that are not associated with asset groups, choose Is Null.
   c. Select the permissions to grant users governed by the access policy.

6. Click Save.
7. To create another rule, click Add or to edit an existing rule, click Edit.

## Editing an access policy

You can edit an access policy that you created and change the name, description, and other properties.

1. On the Access Control page, click Access Policies.
2. Select the access policy that you want to modify.
3. From the Actions menu, click Edit.
4. Modify the required properties and click Save.

   A draft access policy is created.

5. To publish the updated access policy, click Publish.
6. To enable the access policy, click Enable.

## Disabling a metadata access policy

Disabling an access policy removes it from all users that are associated with it.

1. On the Access Control page, click Access Policies.
2. Select the access policy that you want to disable.
3. From the Actions menu, click Disable.

   A confirmation box appears.

4. Click Disable.

   You can enable the access policy to associate it with users again. To enable an access policy that you disabled, click Enable.

## Cloning an access policy

Clone an access policy to create an access policy that is similar to the existing access policy. You cannot edit a predefined access policy, but you can clone the access policy and update it.

1. On the Access Control page, click Access Policies.
2. Select the access policy that you want to clone.
3. From the Actions menu, click Clone.
4. Modify the name and description and click Create.

   **Note:** You cannot change the policy type for a user group policy.

5. Click Create.
6. Update the policy as needed and click Save.
