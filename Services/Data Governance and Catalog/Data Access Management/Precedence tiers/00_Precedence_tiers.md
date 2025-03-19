Precedence tiers are ordered groupings of data de-identification policies that determine the priority and sequence of evaluating data de-identification policies and applying data protections. You assign data de-identification policies to a precedence tier.

Data Access Management evaluates the data de-identification policies within each tier from top to bottom. Data Access Management also evaluates precedence tiers based on rank from lowest integer to highest.

The following image shows the Precedence Tier tab:

![The image shows a ranked list of precedence tiers on the Precedence Tier tab.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-1AFE2EAD-1147-424F-886A-2749F048EB02-low.png)

Keep the following in mind when working with precedence tiers:

* You can't reorder data de-identification policies within a precedence tier if you don't have access to see all the policies within that precedence tier due to metadata access controls.
* You can't rank tiers if you can't see all the precedence tiers.
