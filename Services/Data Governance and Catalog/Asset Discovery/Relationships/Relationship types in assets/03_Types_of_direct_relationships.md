# Types of direct relationships

You can establish various types of direct relationships between two assets. 
  
NOTE: Apart from the predefined relationships that are listed in this help, the Data Governance and Catalog interface can also list other relationship types that are defined exclusively for your organization. For more information about such relationship types, contact your administrator. For more information about how your administrator can customize relationship types, see the Administration help in Metadata Command Center. 
 
## AI Model 

The following table lists the predefined relationships between AI Model assets and other assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| AI Model | AI Model | Contains | An AI model asset contains data of another AI Model asset. |
| AI Model | AI Model | is Used In | An AI model asset's data is used in another AI Model asset. |
| AI Model | Business Term | is Related to | An AI Model asset is related to a Business Term asset type. |
| AI Model | Data Element | is Generating (Target) | An AI model asset generates data that is of the Data Element asset type |
| AI Model | Data Element | is Using (Source) | An AI model asset uses a Data Element asset's data as source. |
| AI Model | Data Process | is Used in | An AI model asset's data is used in a Data Process asset. |
| AI Model | Data Set | is Generating (Target) | An AI model asset generates data that is of the Data Set asset type. |
| AI Model | Data Set | is Using (Source) | An AI model asset uses a Data Set asset's data as source. |
| AI Model | Data Set (Technical asset) | is Generating (Target) | An AI model asset generates data that is of the Data Set asset type. |
| AI Model | Data Set (Technical asset) | is Using (Source) | An AI model asset uses a Data Set asset's data as source. |
| AI Model | Domain | is Related to | An AI Model asset is related to a Domain asset type. |
| AI Model | Metric | is Related to | An AI Model asset is related to a Metric asset type. |
| AI Model | Notebooks or Scripts | is Used in | An AI model asset's data is used in a Notebooks or Scripts asset. |
| AI Model | Subdomain | is Related to | An AI Model asset is related to a Subdomain asset type. |

## Business Area 

The following table lists the predefined relationships between Business Area assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Business Area | Business Area | is the Parent of | A Business Area asset type is the parent of another Business Area asset. |
| Business Area | Geography | is Related to | A Business Area asset is related to a Geography asset. |
| Business Area | Legal Entity | is Related to | A Business Area asset is related to a Legal Entity asset. |

## Business Term 

The following table lists the predefined relationships between Business Term assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Business Term | Business Area | is Related to | A Business Term asset is related to a Business Area asset. |
| Business Term | Business Term | is Classified by | A Business Term asset is classified by another Business Term asset. |
| Business Term | Business Term | is Described by | A Business Term asset is described by another Business Term asset. |
| Business Term | Business Term | is Identified by | A Business Term asset is identified by another Business Term asset. |
| Business Term | Business Term | is Related to | A Business Term asset is related to another Business Term asset. |
| Business Term | Business Term | is Variant of | A Business Term asset is similar to but still different from another Business Term asset. |
| Business Term | Business Term | is the Parent of | A Business Term asset is the parent of another Business Term asset. |
| Business Term | Metric | is Classified by | A Business Term asset is classified by a Metric asset. |
| Business Term | Metric | is Described by | A Business Term asset is described by a Metric asset. |
| Business Term | Metric | is Identified by | A Business Term asset is identified by a Metric asset. |
| Business Term | Metric | is Related to | A Business Term asset is related to a Metric asset. |
| Business Term | Metric | is Variant of | A Business Term asset is similar to but still different from a Metric asset. |
| Business Term | Metric | is the Parent of | A Business Term asset is the parent of a Metric asset. |
| Business Term | System | is a Strategic source for | A System asset is an approved source of data that a Business Term asset represents. |

## Data Quality Rule Occurrence 

The following table lists the predefined relationships between Data Quality Rule Occurrence assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Data Quality Rule Occurrence | Data Element | applies to | A data quality rule occurrence applies to a Data Element for generating data quality scores. |

## Data Quality Rule Template 

The following table lists the predefined relationships between Data Quality Rule Template assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Data Quality Rule Template | Business Term | applies to | A data quality rule template applies to a business term for generating data quality scores. |
| Data Quality Rule Template | Metric | applies to | A data quality rule template applies to a Metric for generating data quality scores. |

## Data Set 

The following table lists the predefined relationships between Data Set assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Data Set | Business Area | is Related to | A Data Set asset is related to a Business Area asset. |
| Data Set | Business Term | is Defined by | A Business Term asset subject area best describes the overall content of a Data Set asset. |
| Data Set | Data Set | is in Lineage with | A Data Set asset is in lineage with another Data Set asset. |
| Data Set | Data Set | is a Source for | A Data Set asset is a source for another Data Set asset. |
| Data Set | Domain | is Defined by | A Domain asset subject area best describes the overall content of a Data Set asset. |
| Data Set | Legal Entity | is Related to | A Data Set asset is related to a Legal Entity asset. |
| Data Set | Manual Data Element | is the Parent of | A Manual Data Element asset is the business representation of data that is not available in the catalog but which is essential to capture for governance purposes in your organization. |
| Data Set | Metric | is Defined by | A Metric asset subject area best describes the overall content of a Data Set asset. |
| Data Set | Subdomain | is Defined by | A Subdomain asset subject area best describes the overall content of a Data Set asset. |
| Data Set | Report | is Derived from | A Data Set asset is derived from a Report asset. |

## Domain 

The following table lists the predefined relationships between Domain assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Domain | Business Area | is Related to | A Domain asset is related to a Business Area asset. |
| Domain | Business Term | is Related to | A Domain asset is related to a Business Term asset. |
| Domain | Business Term | is the Parent of | A Domain asset is the parent of a Business Term asset. |
| Domain | Data Set | is Defined by | A Data Set asset subject area best describes the overall content of a Domain asset. |
| Domain | Data Set | is Related to | A Domain asset is related to a Data Set asset. |
| Domain | Domain | is Related to | A Domain asset is related to another Domain asset type. |
| Domain | Metric | is the Parent of | A Domain asset is the parent of a Metric asset. |
| Domain | Subdomain | is Related to | A Domain asset is related to a Subdomain asset. |
| Domain | Subdomain | is the Parent of | A Domain asset is the parent of a Subdomain asset. |

## Geography 

The following table lists the predefined relationships between Geography assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Geography | Geography | is the Parent of | A Geography asset is the parent of another Geography asset. |

## Legal Entity 

The following table lists the predefined relationships between Legal Entity assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Legal Entity | Geography | is Related to | A Legal Entity asset is related to a Geography asset. |
| Legal Entity | Legal Entity | is the Parent of | A Legal Entity asset type is the parent of another Legal Entity asset. |

## Manual Data Element 

The following table lists the predefined relationships between Manual Data Element assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Manual Data Element | Manual Data Element | is in Manual Lineage with | A Manual Data Element asset is in lineage with another Manual Data Element. |
| Manual Data Element | Technical Data Element | is in Manual Lineage with | A Manual Data Element asset is in lineage with a Technical Data Element. |

NOTE: The *is in Manual Lineage with* relationship type is created by Data Governance and Catalog when you create a manual lineage in the Lineage tab of an asset. 

## Metric 

The following table lists the predefined relationships between Metric assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Metric | Business Area | is Related to | A Metric asset is related to a Business Area asset. |
| Metric | Business Term | is Classified by | A Metric asset is classified by a Business Term asset. |
| Metric | Business Term | is Described by | A Metric asset is described by a Business Term asset. |
| Metric | Business Term | is Identified by | A Metric asset is identified by a Business Term asset. |
| Metric | Business Term | is Related to | A Metric asset is related to a Business Term asset type. |
| Metric | Business Term | is Variant of | A Metric asset is similar to but still different from a Business Term asset. |
| Metric | Business Term | is the Parent of | A Metric asset is the parent of a Business Term asset. |
| Metric | Data Set | is Related to | A Metric asset is related to a Data Set asset. |
| Metric | Metric | Is Classified by | A Metric asset is classified by another a Metric asset type. |
| Metric | Metric | is Described by | A Metric asset is described by another Metric asset type. |
| Metric | Metric | is Identified by | A Metric asset is identified by another Metric asset type. |
| Metric | Metric | is Related to | A Metric asset is related to another Metric asset type. |
| Metric | Metric | is Variant of | A Metric asset is similar to but still different from another Metric asset. |
| Metric | Metric | is the Parent of | A Metric asset is the parent of another Metric asset. |
| Metric | Metric | Semantic Relationship | A Metric asset has semantic relationship with another Metric asset. |
| Metric | System | is a Strategic source for | A System asset is an approved source of the data that a Metric asset represents. |

## Policy 

The following table lists the predefined relationships between Policy assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Policy | AI Model | is Regulating | A Policy asset influences some aspects of an AI model asset. |
| Policy | Business Area | is Related to | A Policy asset is related to a Business Area asset. |
| Policy | Business Term | is Regulating | A Policy asset exerts a regulatory influence over a Business Term asset. |
| Policy | Data element | is Regulating | A Policy asset exerts a regulatory influence over a data element. |
| Policy | Data Set | Policy defined by Business | A Policy asset defines some aspects of a Data Set asset. |
| Policy | Data Set | is Regulating | A Policy asset influences some aspects of a Data Set asset. |
| Policy | Domain | is Regulating | A Policy asset influences some aspects of a Glossary asset. |
| Policy | Geography | is Related to | A Policy asset is related to a Geography asset. |
| Policy | Legal Entity | is Related to | A Policy asset is related to a Legal Entity asset. |
| Policy | Manual Data Element | is Related to | A Policy asset is related to a Manual Data Element asset. |
| Policy | Metric | is Regulating | A Policy asset influences some aspects of a Glossary asset. |
| Policy | Policy | is the Parent of | A Policy asset is the parent of another Policy asset. |
| Policy | Process | is Related to | A Policy asset influences some aspects of a Process asset. |
| Policy | Process | is Compliant with | A Process asset adheres to a Policy asset in whole or in part. |
| Policy | Subdomain | is Regulating | A Policy asset influences some aspects of a Glossary asset. |
| Policy | System | is Regulating | A Policy asset influences some aspects of a System asset. |
| Policy | Policy | support Implementation of | A Policy asset supports some aspect of implementation to another Policy asset. |
|  |  |  |  |
| Policy | Report | is Regulating | A Policy asset influences some aspects of a Report asset. |
| Policy | Report Element | is Regulating | A Policy asset influences some aspects of a Report Element asset. |
| Policy | Classification | is Regulating | A Policy asset influences some aspects of a Classification asset. |

## Process 

The following table lists the predefined relationships between Process assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Process | AI Model | is Related to | A Process asset type is related to an AI model asset type. |
| Process | Business Area | is Related to | A Process asset is related to a Business Area asset. |
| Process | Business Term | is using CDE | A Process asset uses a Critical Data Element of a Business Term asset. |
| Process | Business Term | is Related to | A Business Term asset is relevant to the execution of a Process asset. |
| Process | Data Element | is Related to | A Data Element is relevant to the execution of a Process asset. |
| Process | Data Element | is Using | A Process asset uses a Data Element asset's data. |
| Process | Data Set | is Related to | A Data Set asset is relevant to the execution of a Process asset. |
| Process | Data Set | is Using Data from | A Data Set asset is dependent on the Process asset data. |
| Process | Domain | is used for Process | A Process asset's data is used in a Domain asset. |
| Process | Geography | is Related to | A Process asset is related to a Geography asset. |
| Process | Legal Entity | is Related to | A Process asset is related to a Legal Entity asset. |
| Process | Manual Data Element | is Related to | A Process asset is related to a Manual Data Element asset. |
| Process | Metric | is Related to | A Metric asset is relevant to the execution of a Process asset. |
| Process | Metric | is Using CDE | A Process asset uses a Critical Data Element of a Metric asset. |
| Process | Policy | is Related to | A Process asset evidences execution of, or adherence to, a Policy asset. |
| Process | Process | is Predecessor To | A source Process asset precedes a target Process asset. |
| Process | Process | is Related to | Different processes or process steps are complimentary or otherwise related to other business activities. |
| Process | Process | is the Parent of | A Process asset is the parent of another Process asset. |
| Process | Subdomain | is using CDE | A Process asset uses a Critical Data Element of a Subdomain asset. |
| Process | Subdomain | is Related to | A Subdomain asset is relevant to the execution of a Process asset. |
| Process | System | is Related to | A Process asset is related to a System asset. |
| Process | System | is Using Data from | A Process asset is dependent on a System asset's data. |
| Process | System | Process Applicable System | A Process asset creates or consumes data relevant to a System asset. |

## Project 

The following table lists the predefined relationships between Project assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Project | AI Model | is Related to | A Project asset type is related to an AI model asset type. |
| Project | Business Area | is Related to | A Project asset is related to a Business Area asset. |
| Project | Business Term | is Related to | A Project asset is related to a Business Term asset. |
| Project | Data Set | is Related to | A Project asset is related to a Data Set asset. |
| Project | Domain | is Related to | A Project asset is related to a Domain asset. |
| Project | Geography | is Related to | A Project asset is related to a Geography asset. |
| Project | Legal Entity | is Related to | A Project asset is related to a Legal Entity asset. |
| Project | Manual Data Element | is Related to | A Project asset is related to a Manual Data Element asset. |
| Project | Metric | is Related to | A Project asset is related to a Metric asset. |
| Project | Policy | is Related to | A Project asset is related to a Policy asset. |
| Project | Project | is the Parent of | A Project asset type is the parent of another Project asset type. |
| Project | Process | is Related to | A Project asset is related to a Process asset. |
| Project | Regulation | is Related to | A Project asset is related to a Regulation asset. |
| Project | Subdomain | is Related to | A Project asset is related to a Subdomain asset. |
| Project | System | is Related to | A Project asset is related to a System asset. |

## Regulation 

The following table lists the predefined relationships between Regulation assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Regulation | Business Area | is Related to | A Regulation asset is related to a Business Area asset. |
| Regulation | Geography | is Related to | A Regulation asset is related to a Geography asset. |
| Regulation | Legal Entity | is Related to | A Regulation asset is related to a Legal Entity asset. |
| Regulation | Policy | is Related to | A Regulation asset is related to a Policy asset. |
| Regulation | Regulation | is the Parent of | A Regulation asset type is the parent of another Regulation asset type. |

## Subdomain 

The following table lists the predefined relationships between Subdomain assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Subdomain | Business Area | is Related to | A Subdomain asset is related to a Business Area asset. |
| Subdomain | Business Term | is Classified by | A Subdomain asset type is classified by a Business Term asset type. |
| Subdomain | Business Term | is Described by | A Subdomain asset type is described by a Business Term asset type. |
| Subdomain | Business Term | is Identified by | A Subdomain asset type is identified by a Business Term asset type. |
| Subdomain | Business Term | is Related to | A Subdomain asset type is related to a Business Term asset type. |
| Subdomain | Business Term | is Variant of | A Subdomain asset is similar to but still different from a Business Term asset. |
| Subdomain | Business Term | is the Parent of | A Subdomain asset type is the parent of a Business Term asset type. |
| Subdomain | Data Set | is Related to | A Subdomain asset type is related to a Data Set asset type. |
| Subdomain | Data Set | Subdomain defined by Data | A Subdomain asset may indicate the contents or primary purpose of a Data Set asset. |
| Subdomain | Metric | is Classified by | A Subdomain asset type is classified by a Metric asset type. |
| Subdomain | Metric | is Described by | A Subdomain asset type is described by a Metric asset type. |
| Subdomain | Metric | is Identified by | A Subdomain asset type is identified by a Metric asset. |
| Subdomain | Metric | is Related to | A Subdomain asset is the related to a metric asset type. |
| Subdomain | Metric | is Variant of | A Subdomain asset is similar to but still different from a Metric asset. |
| Subdomain | Metric | is the Parent of | A Subdomain asset is the parent of a Metric asset type. |
| Subdomain | Subdomain | is Related to | A Subdomain asset is related to another Subdomain asset type. |
| Subdomain | Subdomain | is the Parent of | A Subdomain asset type is the parent of another Subdomain asset type. |

## System 

The following table lists the predefined relationships between System assets and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| System | Business Area | is Related to | A System asset is related to a Business Area asset. |
| System | Data Set | is a Strategic Source for | A System asset is a strategic source for a Data Set asset. |
| System | DataSource (Technical Asset) | is Derived from | A System asset is derived from a DataSource asset. |
| System | Geography | is Related to | A System asset is related to a Geography asset. |
| System | Legal Entity | is Related to | A System asset is related to a Legal Entity asset. |
| System | System | is the Parent of | A System asset type is the parent of another System asset type. |
| System | System | is a Source for | A System asset is a source for another System asset. |

## Technical Data Element 

The following table lists the predefined relationships between technical data elements and target assets. 

| Source Asset Type | Target Asset Type | Relationship Type | Meaning of Relationship Type |
|-------------------|-------------------|-------------------|------------------------------|
| Technical Data Element | Manual Data Element | is in Manual Lineage with | A technical data element is in lineage with a Manual Data Element asset. |
| Technical Data Element | Technical Data Element | is in Manual Lineage with | A technical data element is in lineage with a technical data element. |

NOTE: The *is in Manual Lineage with* relationship type is created by Data Governance and Catalog when you create a manual lineage in the Lineage tab of an asset.
