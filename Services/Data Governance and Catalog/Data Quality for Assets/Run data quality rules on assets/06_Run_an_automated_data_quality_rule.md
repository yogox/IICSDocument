# Run an automated data quality rule

When you define an automated data quality rule, Data Governance and Catalog runs the rules automatically according to the schedule you have specified in the Frequency field of the rule template or rule occurrence. You don't need to do anything. You can open the rule occurrence to see the individual data quality scores of the date elements on which the rules have been run.

Consider the following scenarios while you run a data quality rule automation process:

1. The Data Quality and Data Quality Rule Automation options are enabled in Metadata Command Center for a catalog source. The data quality rule occurrences are created automatically for the catalog source and you can manually run them on the data elements associated with the catalog source.
2. The Data Quality option is enabled and Data Quality Rule Automation option is disabled in Metadata Command Center for a catalog source. Automatic rule occurrences are not created. However, you can still run the existing data quality rule occurrences on the data elements associated with the catalog source. You can manually create and run the data quality rule occurrences for the catalog source.

### Automated rules for governance assets

To run automated rules on governance assets, make sure that you have done the following tasks when you define the rule:

* Select the Automation check box.
* Specify the rule schedule in the Frequency field.

When you click Create, Data Governance and Catalog runs the rule once immediately, and then runs all subsequent rules according to your specified schedule.

For more information on defining rules for governance assets, see Defining data quality rules for business assets.

### Automated rules for data elements

To run automated rules on data elements, make sure that you select a schedule in the Frequency field when you define the rule.

When you click Create, Data Governance and Catalog runs the rule once immediately, and then runs all subsequent rules according to your specified schedule.

For more information on defining rules for data elements, see Defining data quality rules for data elements.
