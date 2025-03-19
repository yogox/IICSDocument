You create data access policies to control access to tables or views in cloud data platforms and to filter or de-identify data in other data assets. The steps for creating data access policies are mostly the same, regardless of which type of data access policy you create.

1. Click Data Access in the left navigation to display the Data Access Management page.

   The following image shows the Data Access Management page:

   ![The image shows the Data Access Management page, which includes a top navigation options for Data Access Control, Data Filter, and Data De-identification. The user has selected Data De-identification. The three sub-tabs are Data De-identification, Data Protection, and Precedence Tier. A plus sign appears for creating a new data de-identification. Filter and sort options also appear.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-ACB49ED0-66EA-42D7-A395-1E9D93212CEE-low.png)

2. Select a type of data access policy by clicking the corresponding tab.

   You can create the following types of data access policies:

   - Data access control policies
   - Data filter policies
   - Data de-identification policies

3. Click the plus sign to open the data access policy creation page.

   The following image shows the data access policy creation page for a data de-identification policy:

   ![The image shows the data access policy creation page with the following fields: Name, Description, Precedence Tier, Reference ID, Status, Effective Date, End Date, and Asset Groups. A Stokeholders section appears at the bottom of the page. "Create" and "X" buttons appear at the top of the page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-A0D475DA-A9C8-41C7-84E4-DFA968169C81-low.png)

4. Enter a title and description for the data access policy.

5. Data de-identification policies must be part of a precedence tier. Data access control policies and data filter policies are not organized in precedence tiers.

6. Enter a reference ID or allow Data Governance and Catalog to auto-generate one.

7. Enable the data access policy if you want it to be active immediately after you publish it.

8. Optionally enter effective and end dates.

9. Select stakeholders.

   **Note:** Informatica recommends that you add stakeholders even though it is optional.

10. Click Create.

    The overview page for the data access policy appears.

You can now add rules to this policy.

This policy will stay in Draft status until you publish it.

## Adding a condition to a data access policy

Once you create a new data access policy, you can add one or more conditions to it to further refine when the policy will be activated. This is optional. Only data filter policies and data de-identification policies have conditions. The steps for adding a condition to a data access policy are mostly the same, regardless of the type of data access policy.

1. View a data access policy.

2. Click the Conditions tab.

3. Click the plus sign.

   The Add Condition page appears. The following image shows the Add Condition page:

   ![The image shows one condition on the Add Condition page. The user has selected "User Group" as the driver, "is any of" as the operator, and "AML Team" as one value. the user is searching for a second value for "User Group." A "New Row" button appears below the condition. "Save" and "X" buttons appear at the top of the page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-C962473F-7234-4B73-915E-20C01ED007D7-low.png)

4. Click New Row.

5. Select a contextual attribute, such as "User Group" or "User Context."

6. Select an operator, such as "is any of" or "is null."

7. Add a value.

8. Add additional values as needed.

9. Click Save.

   You can add rules to this data access policy. The type of rules that you add depends on the type of data access policy.
