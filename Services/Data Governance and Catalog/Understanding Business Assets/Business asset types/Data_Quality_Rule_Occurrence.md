# Data Quality Rule Occurrence

A data quality rule occurrence is the business representation of a data quality rule that is run on data elements. You can rate a Data Quality Rule Occurrence asset to indicate your assessment of the quality of the asset or add your comments to the asset to provide your inputs on the data present within the asset. This enables different users to collaborate on assets and make collective decisions on using the data.

You can rate a Data Quality Rule Occurrence asset to indicate your assessment of the quality of the asset, or add your comments to the asset to provide your inputs on the data present within the asset. This enables different users to collaborate on assets and make collective decisions on using the data. For more information about collaborating on an asset, see the Asset Management help.

You can view the number of open tickets and overdue tickets. Open tickets indicate the tickets pending in progress to track changes to the data quality rule occurrence. Overdue tickets indicate the tickets beyond due date that require your action. You can also view the lifecycle of the asset to know the particular stage of the lifecycle in the asset workflow.

### Association of data elements with rule occurrences

You can associate data elements with rule occurrences through the following ways:

- Data quality automation. Automatically associate rule occurrences with their corresponding data elements when data quality checks are run automatically as per the schedule defined by the administrator in Metadata Command Center.
- Bulk import. Manually associate rule occurrences with their corresponding data elements by uploading the data quality scores using a bulk upload template.
- Profiling. Manually associate rule occurrences with data elements when the rule occurrences in Data Governance and Catalog are generated from Data Quality scorecards.

### Overview tab

On the Overview page, you can view basic information about the rule occurrence. If the rule occurrence is created from an automated rule template, the term Auto- is prefixed to the name of the rule occurrence.

The following table describes the properties of the Overview tab:

| Field | Description |
| --- | --- |
| Rule Template | Data quality rule template that defines the parameters of the rule for which the rule occurrence is generated. |
| Sync with Rule Template | Indicates whether the rule occurrence is synced with the rule template that you have specified.
If the rule occurrence is synced, the parameters defined in the rule template are applied for the data quality rule. The rule occurrence score inherits the technical rule reference, target and threshold values that you have specified in the rule template. The rule occurrence scores are updated according to the rule automation schedule that you have specified in the rule template.
If the rule occurrence is not synced, the rule occurrence is an independent asset that is not affected by the rule template parameters. |
| Description | Description of the rule occurrence. The size of the field should not exceed 1 MB. |
| Reference ID | Unique identifier for the rule occurrence. |
| Dimension | One of the six data quality dimension that applies to the data quality rule occurrence.
Default value is Accuracy.
**Note:** If the default value of the Dimension field that is specified here differs from what is displayed on the Data Governance and Catalog interface, the administrator may have defined a different list of dimensions. For more information about how your administrator can customize the data quality dimensions, see the Administration help in Metadata Command Center. |
| Measuring Method | Method by which the data quality rules for the rule occurrence are evaluated. The default value is Informatica Cloud Data Quality. You can choose one of the following values:
- Business Extract. The rule is measured on data that is exported for a particular business case.
- System Function. The rule is measured by a data quality system.
- Technical Script. The rule is measured by a script that is manually run by an analyst.
- Informatica Cloud Data Quality. The rule is measured by Informatica Cloud Data Quality. |
| Primary Data Element | Data element on which the data quality rule is run.
This data element is the input port for the rule in the integrated data quality system. The data quality score is always generated for the primary data element. |
| Secondary Data Element | Secondary input port for the data quality rule that is run on the Primary Data Element. |
| Technical Rule Reference | Rule specification in the data quality application that runs on the data element.
**Note:** If you add a rule specification that has an associated exception task, ensure that the rule specification contains only one additional output other than the exception task outputs. |
| Criticality | Criticality of the rule occurrence. The value can be High, Medium, or Low. The default value is Medium. |
| Target | Minimum acceptable data quality value for the asset to be considered "Good". The default value is 90. |
| Threshold | Minimum acceptable data quality value for the asset to be considered "Acceptable". The default value is 70. |
| Frequency | Frequency of running the data quality rule that is defined in the rule template. The default value is Weekly. You can choose one of the following values:
- Daily
- Weekly
- Monthly
**Note:** If the administrator has configured data quality automation in Metadata Command Center to run as per a schedule defined for the catalog source, you cannot specify a frequency value for individual rule occurrences. In this case, the Frequency field is disabled. |
| Latest Data Quality Score | Data quality scores of the last rule run. The panel displays the composite score and score trend for the data element that is represented by the rule occurrence.
The panel displays the score trend in color according to the target and threshold values that are defined for the rule occurrence. For example, if the threshold value is 40 and the target value is 80, the scores appear in the following color:
- A score below 40 appears in red and is considered "Not Acceptable".
- A score between 40 and 79 appears in amber and is considered "Acceptable".
- A score above 80 appears in green and is considered "Good". |
| Profile Reference | The data quality rule that runs on the data element. Click the reference link to access the rule in the integrated data quality application. |
| Stakeholders | Users or user groups responsible for the rule occurrence or interested in the rule occurrence. |
| Asset Groups | One or more asset groups assigned to this asset. Asset groups allow users access to a set of assets in the organization.
You can assign asset groups to an asset if your organization administrator has granted you the Manage Access permission on the asset through access policies in Metadata Command Center. |
| Created By | User that created the rule occurrence and the date on which it was created. |
| Updated By | User that last updated the rule occurrence and the date on which it was updated. |

For more information about running automated rules on assets, see the Data Quality for Assets help.

### Score tab

View details of the data quality scores that comprise the rule occurrence.

The Latest Data Quality Score panel displays the composite score, the total rows and failed rows from the rule occurrence, and the score trend.

The Total Runs table shows all the data quality rules that have been run so that the composite score is calculated. The following table describes the properties of the Total Runs table:

| Field | Description |
| --- | --- |
| Date | Date on which the data quality rule is run. |
| Latest Score | Data quality score from the rule run. |
| Total Rows | Total number of rows on which the data quality rule is run. |
| Failed Rows | Number of failed rows as determined by the data quality rule run. |

### Stakeholders tab

View users that have been designated as stakeholders for the data quality rule occurrences. Stakeholders are authorized users who are responsible for the rule occurrences, and can approve or reject change requests for the occurrence. If your role has permissions, you can add or remove stakeholders on this page.

The following table describes the properties of the Stakeholders tab:

| Field | Description |
| --- | --- |
| Name | Name of the user or user group. |
| Role | Role of the user or user group in the organization. |
| Email | Email address of the user.
**Note:** This property does not appear for user groups. |
| User Origin | The origin of the users. For example, when a user logs in using SSO, the value for this field is displayed as SAML. |

### Tickets tab

View change request tickets that users have created for the data quality rule occurrence.

The following table describes the properties of the Tickets tab:

| Field | Description |
| --- | --- |
| Name | Name of the ticket. |
| Description | Description of the ticket. |
| Type | Type of ticket. |
| Created On | Date on which the ticket was created. |
| Created By | User that created the ticket. |
| Status | Status of the change ticket. |

You can filter the list of tickets by selecting available filter options.

### History tab

View changes that users have made to the data quality rule occurrence. The History tab provides an audit log that you can use for compliance requirements.

The following table describes the properties of the History tab:

| Field | Description |
| --- | --- |
| Date | Displays the created and last updated dates of the asset. |
| Event Type | Displays the type of the event that is performed on the asset:
- Asset. Displays changes in the name, description, certification, or the reference ID of the asset. 
- Relationship. Displays additions, deletions, and the updates of the relationships between the assets.
- Stakeholder. Displays additions and deletions of stakeholders to the asset. |
| Action | Displays the following actions that are performed on the asset:
- Create. Displayed if the asset is created.
- Updated. Displayed if the asset is updated.
- Deleted. Displayed if the asset is deleted. |
| Current Attributes | Displays the recently changed attributes of the asset. |
| Previous Attributes | Displays the earlier attributes of the asset. |
| Changed By | Displays the user who has performed any action on the asset. |
| Asset Name | Displays the name of the asset. |
| Asset Path | Displays the origin path of the asset. |
| Asset Type | Displays the type of the asset. |
| From Asset Type | Displays the source asset type for which the change is applicable. This is applicable when the event type is Relationship. |
| To Asset Type | Displays the target asset type for which the change is applicable. This is applicable when the event type is Relationship. |
