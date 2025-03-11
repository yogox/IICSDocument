Define a data quality rule to be run on a Glossary asset in Data Governance and Catalog. To define the rule to run on glossary assets, create a data quality rule template, specify the properties of the rule template, and associate the rule template with the glossary asset on which you want to run the rule. The rule that you define is created in the data quality application that is integrated with Data Governance and Catalog. The data quality application runs the rule on the technical assets that are linked to the Glossary asset. After the rule is run, Data Governance and Catalog retrieves and displays the data quality scores of the rule.

Before you create a data quality rule template, make sure that the Glossary asset is linked to the technical assets on which you want to run the rules. For more information about linking Glossary assets to technical assets, see the Asset Management help.

To manually create a data quality rule template that runs on the data elements linked to the glossary asset, perform the following steps:

1. Open the glossary asset on which you want to run the rule, and click the Action menu on the right header of the asset page.

2. From the Action menu, select Create Data Quality Rule Template.

![Image depicting the business term page highlighting the Create Data Quality Rule Template option on the Action menu.](https://onlinehelp.informatica.com/iics/prod/dgc/en/af-data-quality/images/GUID-A24B90ED-39B9-4B7D-A8AC-5EE56EF99414-low.png)

3. Alternatively, click New > Business Rules and select Data Quality Rule Template.

4. Enter the following properties of the rule template:

| Field | Description |
|-------|-------------|
| Name | Name of the rule template. |
| Description | Description of the rule template. |
| Reference ID | Unique reference identifier for the rule template. |
| Dimension | Data quality dimension that applies to the data quality rule that is defined by the rule template. |
| Measuring Method | Method by which the data quality rule for the rule template is evaluated. Select one of the following values:
- Business Extract. The rule is measured on data that is exported for a particular business case.
- System Function: The rule is measured by a data quality system.
- Technical Script. The rule is measured by a script that is manually run by an analyst.
- Informatica Cloud Data Quality. The rule is measured by Informatica Cloud Data Quality. |
| Primary Glossary | Glossary asset that is linked to the technical assets on which you want to run the data quality rule. |
| Secondary Glossary | Additional glossary assets to which the data quality rule in the rule template applies. |
| Technical Rule Reference | Create a reference to a rule specification in the data quality application. You can create a new rule specification, or select from an existing rule specification.
- To create a new rule specification in the data quality application, click Create a new rule. Enter a description for the rule using natural language construction, and click View Recommendations. CLAIRE® reads the description that you enter and intelligently recommends a rule that it can create in the data quality application.

For more information about creating rules that CLAIRE® can interpret, see Guidelines for entering rule descriptions.
- To select from an existing rule specification in the data quality application, click Pick an existing rule.

After you select a rule option, click OK to go back to the rule template creation page. |
| Criticality | Criticality of the rule template. Select one of the following values:
- High
- Medium
- Low |
| Automation | Select the check box to indicate that you want the data quality rule to run automatically on the data elements that are linked to the Primary Glossary. If you select the check box, Data Governance and Catalog automatically runs the rule according to the schedule you specify in the Frequency field. |
| Target | Minimum acceptable data quality value for the asset to be considered "Good."
The target value is higher than the threshold value. For example, you can set the threshold value to 50 and the target value to 85. |
| Threshold | Minimum acceptable data quality value for the asset to be considered "Acceptable."
The target value is higher than the threshold value. For example, you can set the threshold value to 50 and the target value to 85. |
| Frequency | Frequency of running the data quality rule that is defined by the rule template.
- Select Daily to run the rule once in a day.
- Select Weekly to run the rule once in a week.
- Select Monthly to run the rule once in a month.

The rule is run when you click Create. |

![Image depicting an example description and the corresponding rule interpretation by CLAIRE®.](https://onlinehelp.informatica.com/iics/prod/dgc/en/af-data-quality/images/GUID-A0918AB9-6115-4A16-8C6A-04E00F319C8C-low.jpg)

5. When all the details of the rule template are ready, click Create.

When you click Create, the data quality application runs the rule on the data elements linked to the Glossary assets. If you selected the Automation check box, the data quality application runs the rule according to the schedule you specified in the Frequency field. You can now view the data quality scores when you open the rule template, the corresponding rule occurrences, the Glossary asset, and the linked technical assets. If a rule occurrence is created from an automated rule template, the term Auto- is prefixed to the name of the rule occurrence.
