# Creating a catalog source

When you configure a catalog source, you can specify the catalog source type, perform any additional capability on the extracted metadata, and optionally specify a schedule to run your catalog source.

Before you create a catalog source in Metadata Command Center, perform the following tasks:

1. Set up a runtime environment for your organization. For information about runtime environments, see Runtime Environments in the Administrator help.
2. Configure a connection to your catalog source. For more information about configuring a connection, see Connections in the Cloud Common Services help.

After you perform the tasks, you are ready to create your first catalog source. The following image shows the steps involved in the catalog source creation process:

![Image of the workflow for creating a catalog source](../metadata-command-center-catalog-source-configuration/images/GUID-71657ABD-CF9F-485A-A714-6E887F72DAFD-low.png)

**Note:** You can rename a catalog source after you create it, but to apply the change to all associated objects you must rerun the metadata extraction job. 

## Step 1. Register a catalog source

To add a catalog source to Metadata Command Center, first register the catalog service on the Registration page.

1. Log in to Informatica Intelligent Cloud Services and select Metadata Command Center from the My Services page.
2. Click New.

The following image shows the New dialog box:

![Image of the New dialog box](../metadata-command-center-catalog-source-configuration/images/GUID-51BFD760-4ED6-4E1F-862B-8F76B12719F9-low.png)

3. Select a source from the list of predefined source systems. For information about predefined source systems available in Metadata Command Center, see Source systems.
4. Click Create.

The following image shows the Registration page:

![Image of the Registration wizard](../metadata-command-center-catalog-source-configuration/images/GUID-E8BCFC53-A307-4440-821C-81119E2D4F5D-low.png)

5. In the Registration page, enter a name and an optional description for the catalog source.
6. In the Connection Information area, select a connection for the catalog source from the **Connection** list. The list contains all the connections that your organization administrator created in Administrator.

You can expand and view the connection properties for the selected connection. The connection properties differ for each catalog source type.

7. Click Test Connection to test your connection to the source system.

**Note:** The Test Connection function is available only for some catalog sources.

8. Click **Next** to move to the Configuration page.

## Step 2. Configure a catalog source

Configure metadata extraction and profiling options for the catalog source.

1. On the Configuration page, select one or more capabilities that you want to perform on the catalog source.

The following table describes the capabilities of the catalog source:

| Capability | Description |
| --- | --- |
| Metadata Extraction | Extracts source metadata and profile metadata from external source systems. |
| Data Profiling and Quality | - **Data Profiling.** Assesses source metadata and views the collected statistics to discover content and structure, such as value distribution, patterns, and data types.<br>- **Data Quality**. Measures the reliability of the data and enables data usage. <br>- **Data Observability**. Identifies anomalies in the characteristics of the data in your source system. |
| Data Classification | Identifies data elements, entities, and policies based on the extracted metadata. |
| Relationship Discovery | Identifies semantically similar pairs of columns and tables within a catalog source, and recommends columns and tables that can be joined. |
| Glossary Association | Recommends and associates business glossary terms with data elements in technical assets. |

The following image shows the Configuration page:

![Image of the catalog source Configuration page](../metadata-command-center-catalog-source-configuration/images/GUID-7E4F62ED-560D-478A-AE0E-EE88929B374D-low.png)

2. On the Metadata Extraction tab, select any runtime environment that is available in Informatica Intelligent Cloud Services to run the metadata extraction task.

A runtime environment is either Informatica Cloud Secure Agent or a serverless runtime environment.

3. Choose to retain or delete objects that are deleted from the source system in the catalog using the Metadata Change Option.

- **Retain**. Retains objects that are deleted from the source system in the catalog. If you update or add a filter, the catalog retains objects extracted from the previous job and extracts additional objects that match the current filter. Objects deleted from the source system are not deleted from the catalog. Enrichments added on deleted objects and relationships are retained.
- **Delete**. Deletes metadata from the catalog based on objects deleted from the source system and changes you make to the filter. Enrichments added on deleted objects and relationships are also permanently lost. Objects renamed in the source system are removed and recreated in the catalog.

**Note:** You can also change the configured metadata change option when you run a catalog source. 

4. You can add filter conditions to extract metadata from a specific set of objects in the source system. In the Filters section, select Filter Conditions to add filters.

The system extracts the source metadata based on the object types and conditions specified in this page.

a. From the first list, choose to include or exclude specific metadata in an extraction run. 
b. From the second list, you can choose the type of object from which you want to include or exclude metadata. 

The object type can be a table, view, schema, path, file or folder depending on the catalog source type that you configure.

c. From the third list, choose the filter condition based on the object type that you have selected. 

You can choose to specify the name or pattern of the path to an object that you want to include or exclude.

d. Click Select to enter one or more values for the specified object type that you want to include or exclude from the extraction run.

**Note:** The Select option appears depending on the catalog source type that you configure.

The values that you enter differ based on the catalog source types. The following table shows the different values that you can enter for different catalog source types:

| Catalog Source Type | Values |
| --- | --- |
| Relational database catalog sources, such as Oracle and Azure SQL Server | Full names of tables, schemas, or views. You can use wildcard characters in the name. |
| ETL catalog sources, such as Azure Data Factory | Fully qualified paths to the objects. You can use wildcard characters in the pattern. |
| File system based catalog sources, such as Amazon S3 and Azure Data Lake Storage | Full names of files or folders. You can use wildcard characters in the name. |

e. You can add multiple filter conditions for each catalog source to include and exclude specific metadata from the source systems. To add more filters, click the Add icon. 

The following images are a few examples of filters:

▪ The following filter extracts metadata from a table named Employee_Table that belongs to the Ora1 schema in an Oracle source system:

![The image shows the filter condition for an Oracle catalog source to include metadata from an Employee_Table table located in the Ora1 schema.](../metadata-command-center-catalog-source-configuration/images/GUID-3663C511-E450-4B91-A108-B39726570F90-low.png)

▪ The following filter excludes metadata from an activity named Activity1 located at AzureDatafactoryName/dev_pipeline/Activity1 in a Microsoft Azure Data Factory source system:

![The image shows the filter condition for a Microsoft Azure Data Factory catalog source to exclude metadata from the activity named Activity1 located in the AzureDataFactory1/Pipeline1/Activity1 path.](../metadata-command-center-catalog-source-configuration/images/GUID-55C74E46-1E9B-4406-87D7-96B20FA04BC0-low.png)

**Note:** For File System catalog sources, if you add multiple filters with different wildcard usage for the same object type, only the last wildcard condition is considered.

Some catalog sources have additional parameters that you can configure on this tab.

**Note:** Use expert parameters when it is recommended by Informatica Global Customer Support.

5. On the Data Profiling and Quality tab, enable the capabilities and enter values to determine the type of data that you want the data profiling and quality task to collect, the scope of the data profile and quality run, and the sample rows on which you want to run the data profiling and quality task.

Optionally, you can add filters conditions to create subsets of metadata that you can use to run a data profiling task on a catalog source.

For more information about data profiling and data quality configuration options, see the Metadata Command Center Administration help.

6. On the Data Classification tab, enable the capability and select one or both of the following options:

| Option | Description |
| --- | --- |
| Generated Data Classifications | A CLAIRE powered solution. The system automatically generates data classifications for the data elements in the catalog. |
| Data Classification Rules | Choose from predefined or custom data classifications. Click Add Data Classification and select the data element classification that you want to apply to the catalog source. **Note:** Data classifications that you create using the New > Data Classification menu appear in this list. |

For more information about creating data classifications, see the Administrator help.

7. On the Relationship Discovery tab, enable the capability and enter values for the following properties to determine column similarity and joinable table relationships:

The following table describes the properties:

| Property | Description |
| --- | --- |
| Relationship Inference Model | Select the predefined relationship inference model that Metadata Command Center provides for discovering column similarity relationships within the catalog source. You can also choose a relationship inference model that you have imported. |
| Containment Score Threshold | Specify a score from 0 to 1 inclusive to identify joinable table relationships within the catalog source. This score is an indicator of the data overlap between the two given columns which determines whether the tables are joinable. A higher score means more similarity of data and a greater probability of the tables being joinable. |

For more information about relationship discovery, see the Administrator help.

8. On the Glossary Association tab, enable the capability and configure settings for a catalog source to automatically associate or recommend glossary terms as business names for data elements in technical assets.

The following table describes the settings for a catalog source:

| Property | Description |
| --- | --- |
| Enable auto-acceptance | When enabled, this option automatically associates glossary terms with data elements based on the threshold limit that you specify. The automatically accepted glossary terms appear as business names of data elements in Data Governance and Catalog. |
| Confidence Score Threshold for Auto-Acceptance | Specify a percentage from 80 to 100 inclusive to set a threshold limit. If a glossary term matches a data asset within the threshold specified, Metadata Command Center automatically assigns the matching glossary term to the data element. The name and description of the glossary term with the highest confidence score appears as the name and description of the data element asset in Data Governance and Catalog. |
| Ignore Keywords | Choose to ignore specific parts of data elements when making recommendations. You can enter multiple unique prefix and suffix keywords. Keyword values are case insensitive. |
| Glossary Association Scope | Choose specific top-level business glossary assets to associate with technical assets. Selecting a top-level asset selects its child assets as well. |

For more information about the glossary association settings, see the Administrator help.

9. Click Next to move to the Associations step.

## Step 3. Associate stakeholders and asset groups

Associate users or user groups within a stakeholder role as stakeholders for technical assets in Data Governance and Catalog. Also, you can choose to assign technical assets extracted from the catalog source to asset groups. You can then use access policies to control permissions on assets that are assigned to asset groups.

Verify that the administrator assigned users and user groups to the stakeholder role that you want to associate with technical assets.

1. To associate users or user groups as stakeholders with technical assets extracted from the catalog source, perform the following steps:

a. On the Associations page, click Stakeholders.
b. Select Assign Stakeholders.
c. Select a stakeholder role.
d. Click Select to add users and user groups from the stakeholder role as stakeholders for the technical assets.

The Add Users & User Groups dialog box displays a list of users and user groups assigned to the selected stakeholder role.

![The image shows the Add Users and User Groups dialog box. You can choose to add a user or a user group. Depending on your choice, the page displays a list of users or user groups you can assign as stakeholders for the asset.](../metadata-command-center-catalog-source-configuration/images/GUID-3E933909-1E3C-4EDB-8136-1BFEF84336CE-low.gif)

e. Select one or more users or user groups to assign as stakeholders for the technical assets, and click OK.

Only the selected users and user groups belonging to the specified stakeholder role are granted the permissions to technical assets.

f. To assign users or user groups from another stakeholder role, click Add and then repeat the steps.

2. To assign asset groups to technical assets extracted from the catalog source, perform the following steps:

a. On the Associations page, click Asset Groups.
b. Select Assign Asset Groups.
c. Click Select.

The Select Asset Groups dialog box displays the list of asset groups.

If you enabled an access policy that includes an asset group, you can only view assets that belong to that asset group.

3. Select the asset groups to which you want to assign technical assets extracted from the catalog source, and click OK.

![The image shows the Select Asset Groups box with one asset group selected.](../metadata-command-center-catalog-source-configuration/images/GUID-FA8CA693-2C33-4251-8C61-AE10AEA49D87-low.png)

4. Choose to save and run the job or to schedule a recurring job.

- To save and run the job, click Save and then Run.
- To schedule a recurring job, click Next to open the Schedule page.

## Step 4. Schedule a job

Select a schedule to indicate how often you want to run the catalog source job.

1. On the Schedule tab, select Run on schedule to enter a schedule for each capability that you configured for the catalog source.

The schedule determines the frequency at which the metadata extraction and other configured capabilities run for the catalog source that you create.

2. Click the checkbox corresponding to each capability that you want to include in the schedule.

You can choose to perform a full or an incremental metadata extraction. A full metadata extraction extracts all objects from the source to the catalog. An incremental metadata extraction extracts only the changed and new objects since the last successful catalog source job run. Incremental metadata extraction doesn't remove deleted objects from the catalog and doesn't extract metadata of code-based objects if applicable.

When you run an incremental metadata extraction job with a filter to include metadata from objects, the job extracts only the objects that have the latest timestamp since the last successful job.

**Note:** The incremental extraction option appears if it is available for the catalog source. You can't choose incremental metadata extraction and full metadata extraction in the same schedule. To create a schedule for incremental metadata extraction, you must have completed at least one complete metadata extraction job successfully. If not, first create a schedule for a full metadata extraction.

If an incremental metadata extraction is scheduled to run when the last run details aren't available, the job first performs a full metadata extraction, followed by incremental metadata extraction on subsequent runs.

For example, this can happen in the following scenarios:

- You create schedules for both incremental metadata extraction and full metadata extraction, but schedule the incremental extraction to run before the first full metadata extraction job.
- You create schedules for both incremental metadata extraction and full metadata extraction, but delete the full metadata extraction schedule before its first run.

3. Enter the start date, time zone, and the interval at which you want to run the catalog source job.

You can also specify options for the job to repeat daily, weekly, indefinitely, or repeat until a specified time.

4. You can manage additional schedules using the following options:

a. To create a new schedule, click the Add button.
b. To delete a schedule, click the Delete button.
c. To enable or disable a schedule, click the Enable Schedule toggle button.

**Note:** You can create a maximum of one schedule per capability that you enable. If you purged a catalog source or did not run the metadata extraction job, the catalog source job runs metadata extraction before running other scheduled capabilities.

5. Click Save to save the schedule.

If you click Run, the catalog source job is immediately triggered.

**Note:** If the first run of the catalog source must happen on the schedule, then you need to save the catalog source and close the page.

## Step 5. Run the catalog source job

After you save the configuration details, you can run the catalog source job.

1. Click Run.

The Run Catalog Source Job dialog box appears.

**Note:** If you created a schedule for the catalog source and the first run of the catalog source must happen based on the schedule, then you need not run the catalog source.

2. In the Scope of Run section, select or clear the capabilities that you want to include or exclude for the catalog source job.

You can override the capabilities that you selected while configuring your catalog source on the Configuration page. The first time you run the catalog source job, the metadata extraction capability is mandatory. You can choose to override the configured metadata change option. You can retain or delete objects that are deleted from the source in the catalog. For subsequent runs of the catalog source job, the metadata extraction capability is optional.

**Note:** You can choose to perform a full or an incremental metadata extraction. The incremental extraction option appears if it is available for the catalog source. You can choose incremental metadata extraction for subsequent runs only after one full metadata extraction job completes successfully.

3. Click **Run**.

A job is triggered to run the catalog source. You can monitor the status of the job on the Overview page.

**Note:** You can't trigger more than one run at a time on a catalog source simultaneously. If a job for a catalog source is in progress, wait for the existing job to complete or cancel the ongoing job before you trigger a new job.

4. Optionally, you can run your catalog source job from the Explore page by selecting **Run** from the Action menu for the newly created catalog source.
