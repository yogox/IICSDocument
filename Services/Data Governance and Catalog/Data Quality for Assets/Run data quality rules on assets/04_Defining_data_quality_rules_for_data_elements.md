Define a data quality rule to be run on a data element that is the part of the metadata extracted by Metadata Command Center. To define the rule, create a data quality rule occurrence, specify the properties of the rule occurrence, and associate the rule occurrence with the data element on which you want to run the rule.

Before you run the data quality rules, enable the Data Quality capability for the catalog source in Metadata Command Center.

The rule you define is created in the data quality application that is integrated with Data Governance and Catalog. The data quality application runs the rule on the data element. After the rule is run, Data Governance and Catalog retrieves and displays the data quality scores of the data element in the rule occurrence.

**Note:** The following guidelines apply for associating rule occurrences to data elements:

* The rule occurrences can be manually created, automatically generated, or can be associated with a data quality score card. For automatically generated rule occurrences, you can view the individual data quality scores of the data elements on which the automated data quality rules have been run. You can also manually run a data quality rule to generate manually created rule occurrences.
* In data profiling, when you run a profile that has a rule associated with it, you can view the data quality score card in Data Governance and Catalog after a successful profile run. Rule occurrences related to the score card are generated in Data Governance and Catalog. You can associate a data element to a rule occurrence that is generated from a score card.
* If you manually associate rule occurrences with data elements and then you purge the catalog source that the data element belongs to, the associated rule occurrences are also deleted. 

To manually create a rule occurrence that runs on a data element, perform the following steps:

1. Open the data element on which you want to run the rule, and click the Action menu on the right header of the data element page. 

2. From the Action menu, select Create Data Quality Rule Occurrence.

![Image depicting the column asset page highlighting the Create Data Quality Rule Occurrence option on the Action menu.](../af-data-quality/images/GUID-FAFA22D4-DF20-438E-9E5F-951B6472EBB1-low.png)

3. Alternatively, click New > Business Rules and select Data Quality Rule Occurrence.

4. Enter the following properties of the rule occurrence: 

| Field | Description |
|-------|-------------|
| Rule Template | Data quality rule template that defines the parameters of the rule that you want to run on the data element. |
| Sync with Rule Template | Select to sync the rule occurrence with the rule template that you have specified.
If the rule occurrence is synced, the parameters defined in the rule template are applied for the data quality rule. The rule occurrence score inherits the technical rule reference, target and threshold values that you have specified in the rule template. The rule occurrence scores are updated according to the rule automation schedule that you have specified in the rule template.
If the rule occurrence is not synced, the rule occurrence is an independent asset that is not affected by the rule template parameters. |
| Name | Name of the rule occurrence. |
| Description | Description of the rule occurrence. |
| Reference ID | Unique identifier for the rule occurrence. |
| Dimension | Data quality dimension for which the data quality rule is run. |
| Measuring Method | Method by which the data quality rule for the rule occurrence is evaluated. This field can have one of the following values:
- Business Extract. The rule is measured on data that is exported for a particular business case.
- System Function: The rule is measured by a data quality system.
- Technical Script. The rule is measured by a script that is manually run by an analyst.
- Informatica Cloud Data Quality. The rule is measured by Informatica Cloud Data Quality.

**Note:** If you select Informatica Cloud Data Quality as the measuring method, the Technical Rule Reference field is mandatory. This field is not mandatory for other measuring methods. |
| Primary Data Element | Data element on which the data quality rule is run.
This data element is the input port for the rule in the integrated data quality system. The data quality score is always generated for the primary data element.
To add a primary data element, select a system asset or a catalog source. Next, select a technical data set or a business data set depending on whether you selected a catalog source or a system. Finally, select data elements from the selected data set.
If you do not enable the Data Quality option in Metadata Command Center for a catalog source, the options in this field are disabled. When you manually create a data quality rule occurrence and enter the primary data element to specify the data element on which the data quality rule is run, you cannot edit or change this primary input port for the data quality rule after the rule occurrence is created.
When you create a data quality score card in Data Profiling, a rule occurrence is generated from the data quality score card. You can now associate this rule occurrence with the primary data element. If you do not add the primary data element, no data quality score is displayed . Thus, the Primary Data Element option is only editable for rule occurrences associated with data quality score cards. |
| Secondary Data Element | Secondary input port for the data quality rule that is run on the Primary Data Element. |
| Technical Rule Reference | Create a reference to a rule specification in the data quality application. You can create a new rule specification, or select from an existing rule specification.
- To create a new rule specification in the data quality application, click Create a new rule. Enter a description for the rule using natural language construction, and click View Recommendations. CLAIRE® reads the description that you enter and intelligently recommends a rule that it can create in the data quality application.

To create rules that CLAIRE® can interpret, see [Guidelines for entering rule descriptions](../af-data-quality/Guidelines_for_entering_rule_descriptions.html).
- To select from an existing rule specification in the data quality application, click Pick an existing rule.

After you select a rule option, click OK to go back to the rule occurrence creation page.

**Note:** If you select Informatica Cloud Data Quality as the measuring method, the Technical Rule Reference field is mandatory. This field is not mandatory for other measuring methods.

When you manually create a rule occurrence, you can also specify the input parameters of the primary and secondary data elements gathered from multiple input parameters in the integrated data quality system. This helps you to evaluate the quality of an asset based on the inputs from multiple fields as defined in the data quality rule. For example, if you want to create a rule that validates the hire date of a candidate, you can use the hire date of the candidate as one input parameter and the date of birth of the candidate as another input parameter. You can then use the data of the two input parameters to view the data quality scores and validate the hire date of the candidate.

Input parameter mapping is mandatory for a data quality rule occurrence if you are using a multi input parameter rule from the integrated data quality system. Data quality scores are always reported on the primary data element.

Map each rule input parameter to a unique data element. Make sure that at least one rule input parameter is mapped to a primary data element. |
| Criticality | Criticality of the rule occurrence. The value can be High, Medium, or Low. |
| Target | Minimum acceptable data quality value for the asset to be considered "Good."
The target value is higher than the threshold value. For example, you can set the threshold value to 50 and the target value to 85. |
| Threshold | Minimum acceptable data quality value for the asset to be considered "Acceptable."
The target value is higher than the threshold value. For example, you can set the threshold value to 50 and the target value to 85. |
| Frequency | Frequency of running the data quality rule that is defined by the rule template.
- Select Daily to run the rule once in a day.
- Select Weekly to run the rule once in a week.
- Select Monthly to run the rule once in a month.

The rule is run when you click Create. |

The following image shows the dialog box to select the primary data element: 
![Image depicting the dialog box to select the primary data element of a rule occurrence.](../af-data-quality/images/GUID-23084767-3448-4EA9-B3B5-118C5BA0E425-low.png)

The following example image shows a rule description and its CLAIRE® recommendation:

![Image depicting the description and the corresponding rule interpretation by CLAIRE®.](../af-data-quality/images/GUID-A83C6B7E-A3F9-4F5C-8673-B3883C94441A-low.png)

The following image shows the addition of rule reference for a single input parameter from an existing rule specification:

![Image depicting the addition of rule reference from an existing rule specification.](../af-data-quality/images/GUID-727EF770-0542-4D93-9E85-99A58273F4E7-low.jpg)

The following image shows the addition of a rule with multiple input parameters and the Show Preview icon to view the rule:

![Image depicting the addition of a rule with multiple input parameters and the Show Preview icon to view the rule.](../af-data-quality/images/GUID-8C88BBDD-C031-4480-952F-3DD718AD63F6-low.png)

The following image shows how to map multiple input parameters to data elements:

![Image depicting how to map multiple input parameters to data elements.](../af-data-quality/images/GUID-06322BF4-043F-4B4C-80F5-591CE4B65811-low.png)

The following image shows the input parameters mapped to the primary and secondary data elements:

![Image depicting the mapping of input parameters of the primary and secondary data elements.](../af-data-quality/images/GUID-BD9529CD-5CA7-48CA-9F72-C9D47D38DFC0-low.jpg)

5. When all the details of the rule occurrence are ready, click Create.

When you click Create, the data quality application runs the rule on the data element. If you selected a schedule in the Frequency field, the data quality application runs the rule on the data element according to the rule schedule you specified in the Frequency field. When the data quality score is ready, Data Governance and Catalog displays the score in the rule occurrence.

**Technical hierarchy of a rule occurrence**
For an automatically generated rule occurrence, the catalog source is the highest unit and the data elements are the smallest units in the technical hierarchy.

![Image depicting technical hierarchy of a rule occurrence.](../af-data-quality/images/GUID-1D4472A6-EFDC-486A-AC0B-B4382E823FDC-low.jpg)

**Note:** If you bulk import the assets, the rule occurrences do not have the mentioned technical hierarchy. As a result, the rule occurrences are not removed when you purge a catalog source.

For more information, see the following topics:
- [Run an automated data quality rule](../af-data-quality/Run_an_automated_data_quality_rule.html)
- [Run a data quality rule manually](../af-data-quality/Run_a_data_quality_rule_manually.html)
- [View data quality scores in assets](../af-data-quality/View_data_quality_scores_in_assets.html)
