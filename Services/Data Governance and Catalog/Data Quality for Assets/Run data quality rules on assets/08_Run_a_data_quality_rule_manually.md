[Data Quality for Assets](Data_quality_scores.html) > [Run data quality rules on assets](Run_data_quality_rules_on_assets.html#3_9_27_1) > Run a data quality rule manually

Apart from the automated data quality rule that you might have configured, you can manually run a data quality rule on governance assets any time.

You might want to manually run a data quality rule for a business asset in the following situations:

* When you defined the rule template, you did not select the Automation check box.
* When you defined the rule template, you selected the Automation check box and specified the schedule in the Frequency field.
* You want to run the rule at a time other than the schedule you specified in the Frequency field of the rule template. For example, if you specified a weekly schedule, you want to run the rule before one week has elapsed.

Before you run a data quality rule manually, the following prerequisites apply:

* The Data Quality option for the catalog source is enabled in Metadata Command Center.
* Your organization administrator has granted you the Execute permission on data quality rule occurrence assets through access policies in Metadata Command Center.
* You're a stakeholder of the data quality rule occurrence.
* The data quality rule occurrence is in the Published lifecycle status.

To run a data quality rule manually, go to the Score tab of the rule occurrence page and click the Run Now option on the top right corner of the page. This triggers a job that retrieves the latest data quality score for the rule occurrence. When the job is triggered successfully, you can monitor the job in Metadata Command Center.

The following image shows the Score tab of a data quality rule occurrence:

![Image depicting the Score tab of a rule occurrence.](../af-data-quality/images/GUID-54B5A313-5F08-48B0-9E86-8880E652401B-low.jpg)

For information about defining rules for business assets, see [Defining data quality rules for business assets](../af-data-quality/Defining_data_quality_rules_for_business_assets.html).
