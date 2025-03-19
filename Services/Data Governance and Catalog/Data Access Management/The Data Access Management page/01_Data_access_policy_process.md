To protect data and control access to your data, you perform steps on the Data Access Management page to create data access policies, rules, and data protections.

The data access control workflow includes the following steps:

1. Determine which type of data access policy best fits your use case.

2. On the Data Access Management page, create a data access policy.

   You can create the following types of data access policies:
   - Data access control policies
   - Data filter policies
   - Data de-identification policies

3. If you determine that you will be creating data de-identification policies, do the following:
   a. Create precedence tiers so you can select them when you are creating the policies.
   b. Create data protections so you can select them when you are creating data de-identification rules.

4. Create one or more rules to add to the data access policy.

   The rule type matches the data access policy type. Rule types include the following:
   - Data access control rules
     
     To create a data access control rule, you do the following:
     1. Select which data access policy this rule will be associated with.
     2. Give the rule a title and description.
     3. Select the attributes that define the condition for this rule to activate. 
     4. Define filters based on data asset types that grant read, write, or delete permissions.
   
   - Data filter rules
     
     To create a data filter rule, you do the following:
     1. Select which policy this rule will be associated with.
     2. Give the rule a title and description.
     3. Select the attributes that define the conditions for this rule to activate.
     4. Define filters based on data classifications that will drop records from the result set.
        
        For example, if you select a data classification called "Last Name," select the *is any of* operator, and enter a string of "Smith," Data Access Management will drop any record with "Smith" in the "Last Name" column. If instead, you selected the *is not any of* operator, Data Access Management will keep any record that has the value "Smith" in the "Last Name" column and drop all other records.
   
   - Data de-identification rules
     
     To create a data de-identification rule, you do the following:
     1. Select which policy this rule will be associated with.
     2. Give the rule a title and description.
     3. Select the attributes that define the conditions for this rule to activate.
     4. Determine which data classifications to protect and which data protections to use to protect them.
        
        You only assign one data protection to each data class. You can reuse the same data protection on multiple data classes.

5. Publish the data access policy and enable it.

The data access policy is now active.
