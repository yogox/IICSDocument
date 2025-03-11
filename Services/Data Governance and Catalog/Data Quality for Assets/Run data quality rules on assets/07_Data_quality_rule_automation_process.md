# Data quality rule automation process

Before you run a data quality rule automation process, ensure to enable the Data Quality and Data Quality Rule Automation options in Metadata Command Center for a catalog source. To define an automated data quality rule that you want to run on data elements, ensure that the assets are correctly associated with each other in Data Governance and Catalog.

### Before you define an automated rule

Before you define an automated data quality rule, your must link the technical assets that represent the data elements to the corresponding Glossary business assets.

**What is a technical asset?** When you define a data quality rule, the rule is run on the data that is located in the source systems in your organization. Metadata Command Center extracts the metadata from the source systems and sends the metadata to Data Governance and Catalog. This metadata appears as technical assets in Data Governance and Catalog. Therefore, technical assets in Data Governance and Catalog are metadata representations of the data in your organization. When you open a technical asset, you can see the constituent data elements. Technical assets also display catalog metadata such as profiling and classification information for the data. For more information about technical assets, see the Understanding Technical Assets help.

**What is a business asset?** Business assets are semantic representations of technical assets. You can enrich the metadata of technical assets by adding governance metadata to the business assets. For example, in a business asset, you can specify a meaningful name, enter a description, and denote the stakeholders of the data assets. For more information about business assets, see the Understanding business assets help.

**How are technical and business assets related?** Technical assets appear in Data Governance and Catalog because Metadata Command Center periodically extracts and sends the metadata. As a user, you create business assets in Data Governance and Catalog. The business assets that you create are independent assets. This is why you must link business assets with their corresponding technical assets. When the linking is complete, a business asset and a technical asset eventually represents the same data set that resides in your organization. You can define a data quality rule only for a business asset of the Glossary type. The rule, however, runs on the data elements that are represented by the Glossary asset or the corresponding technical asset.

The following diagram depicts the link that you must create between a technical asset and a Glossary asset:

![Image depicting the link between a Glossary asset and several technical assets.](https://onlinehelp.informatica.com/iics/prod/dgc/en/af-data-quality/images/GUID-FA6DD37C-4DDA-438F-ACEB-39A37C4F7F6C-low.jpg)

For example, you might have five tables in your organization that contain employee names and personal information. These five tables appear as five technical assets in Data Governance and Catalog. To govern these five tables, you can create a single business asset called "Employee Record" of the Glossary Business Term type, and link the business term to the five technical assets. If you now run a mobile number check rule for the business term, the rule is run on all five tables.

For more information about linking a technical asset to a Glossary asset, see the Asset Management help.

### Defining an automated rule

Define an automated data quality rule as a data quality rule template in Data Governance and Catalog, and associate a Glossary asset to the rule template.

**What is a data quality rule template?** A data quality rule template is the definition for a rule. It contains a textual description of the rule and other essential rule parameters such as dimension, threshold value, target value, and criticality. In the rule template, you must provide a reference to a rule specification in your data quality application. You can either provide a reference to an existing rule specification in your data quality application, or you can create a new rule specification in your data quality application from the rule template page in Data Governance and Catalog. When you provide this reference, a link between the rule template in Data Governance and Catalog and the rule specification in the data quality application is created. When this link is created, the rule template becomes the business representation of the data quality rule in your data quality application. For more information about the fields of a rule template asset, see the Data Quality Rule Template topic in the Understanding Business Assets help.

**How is a rule template and rule specification related?** When you create a data quality rule template, you must specify a Glossary asset that you want to associate with the rule template. This association specifies the data elements on which the data quality rule must run. The parameters that you define in the rule template are applicable to the data quality rule that is run on the data elements that are represented by the Glossary asset. If you do not associate the rule template with a Glossary asset, the rule template remains an independent asset, and there are no data elements on which the specified rule must run.

The following diagram depicts the association that you must create between a data quality rule template and a Glossary asset:

![Image depicting the link between a rule template and a Glossary asset, and between the rule template and a rule specification.](https://onlinehelp.informatica.com/iics/prod/dgc/en/af-data-quality/images/GUID-FF15F16D-3D6B-4382-9B71-DE420A9C9E2C-low.jpg)

For example, you can create a data quality rule template called "Mobile Number Check" in Data Governance and Catalog and link the rule template to the Default/mob_phno_check rule specification in your data quality application.

For more information about creating a data quality rule template, see Defining data quality rules for business assets.

### After you define an automated rule

When you create a rule template, the data quality rule is automatically run on the data elements represented by the Glossary asset, and Data Governance and Catalog displays the rule scores as rule occurrences.

**What happens when you create a rule template?** After you create a rule template, Data Governance and Catalog sends the data elements of the Glossary asset to the data quality application. The rule specification that you specified in the rule template is run on the data elements, and the data quality application generates a rule score for each data element. The data quality application sends the rule scores to Data Governance and Catalog, where it appears as data quality rule occurrences.

**What is a data quality rule occurrence?** A data quality rule occurrence is the representation of the data quality score of a single data element. While the data quality rule template is the definition of a rule, a data quality rule occurrence is the instance of the rule that is run on a single data element. For more information about the fields of a rule occurrence asset, see the Data Quality Rule Occurrence topic in the Understanding Business Assets help.

The following diagram depicts the rule occurrences that are created when a data quality rule is run on data elements:

![Image depicting the automatic generation of data quality scores for data elements.](https://onlinehelp.informatica.com/iics/prod/dgc/en/af-data-quality/images/GUID-B0F18F98-601A-4B69-B4C1-002522061018-low.jpg)

For more information about viewing data quality scores, see View data quality scores in assets.

### Putting it all together

The following diagram depicts the entire process of data quality rule automation:

![Image depicting the entire data quality rule automation process.](https://onlinehelp.informatica.com/iics/prod/dgc/en/af-data-quality/images/GUID-32747D12-39A1-465E-BDBC-420C0F982E11-low.jpg)

1. Link the technical assets that represent the data elements to the corresponding Glossary asset.
2. Create a data quality rule template.
   a. In the rule template, specify the Glossary asset that is linked to the technical assets on which you want to run the data quality rule.
   b. Create a reference between the rule template in Data Governance and Catalog and a rule specification in your data quality application.
3. When you save the data quality rule template, Data Governance and Catalog sends the data elements to the data quality application.
4. The data quality application runs the rule on the data elements and generates data quality scores.
   a. The data quality scores appear in Data Governance and Catalog as rule occurrences.
   b. Each rule occurrence corresponds to a data element on which the data quality rule was run.
