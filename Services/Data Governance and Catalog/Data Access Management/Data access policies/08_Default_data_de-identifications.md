# Default data de-identifications

Data Access Management applies a default data de-identification technique if there are no data de-identification policies or the existing policies don't apply in a particular context or for particular classes of data.

If the field has a data element classification, Data Access Management applies the Redact with null data de-identification technique.If the field does not have a data element classification, Data Access Management applies the Retain data de-identification technique.

The default data de-identification technique also applies when a data protection cannot be applied to a specific field.

The following diagram shows the data de-identification policy execution order:

![The diagram shows the order in which Data Access Management executes data de-identification policies. It includes a flow that shows Step 1 leading to Policy 1, which leads to Step 2. Step 2 leads to Policy 2, which leads to Policy 3. Policy 3 is followed by an ellipsis, which leads to Policy N. Policy N is Step 3, which leads to Step 4, "Default data protections." Step 1 is "Start from the policy at the top of the list." Step 2 is "Continue down the list..." Step 3 is "...until the last policy in the list is executed." Step 4 is "If no policies execute, apply the default data protections."](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-511D96E1-3C34-4D8C-BF23-AEE6546E7A3B-low.png)
