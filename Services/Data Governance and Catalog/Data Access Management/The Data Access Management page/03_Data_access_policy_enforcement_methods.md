# Data access policy enforcement methods

As a Data Steward, it's important that you know where enforcement occurs for each type of policy that you create in Data Access Management. Data Access Management works with other Informatica services to protect data and provide access to it.

The following diagram shows how policies that you create in Data Access Management protect data in Data Integration mappings and Data Marketplace orders:

![The diagram has four rows. The second row shows a Data Steward defining, creating, and approving policies and rules. An arrow points to the top row where a Data Integration Developer creates a mapping to deliver protected data. Another arrow points from the second row to the third bottom row where a Data User shops for data, orders data, and accesses protected data in Data Marketplace. Another arrow points from the second row to the bottom row where a Data User queries data and accesses it in a protected cloud data platform.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-5FEB717C-3FC4-4E60-A326-932A1EB1496F-low.png)

When you use Data Integration to build a data pipeline, you can connect an Access Policy transformation to the mapping. The Access Policy transformation applies data protection policies created in Data Access Management according to the properties of the Access Policy transformation. An access policy is a set of policies and associated data protection rules that apply data protection techniques and transform the data accordingly.

To learn more, see Citation in the Data Integration help.

The following table identifies the software environments in which enforcement occurs for each type of policy:

| Policy type | Enforcement environment |
|-------------|-------------------------|
| data filter policy | In Data Integration through Access Policy transformations and in Data Marketplace through the Managed Access setting in a delivery template. |
| data de-identification policy | In Data Marketplace through the Managed Access setting in a delivery template.
To learn more, see Citation in the Data Marketplace help. |
| data access control policy | In your source system after policy pushdown from Data Access Management.
You can enforce data access control policies in Databricks and Snowflake source systems.
For more information about configuring Databricks and Snowflake for use with data access control policies, see [Data access control policy prerequisites](../ae-data-accessmanagement/Data_access_control_policy_prerequisites.html). |

## Data Types

Lists data types that you can apply data access policies to when using the Managed Access setting in a delivery template in Data Marketplace or with access policy transformations in Data Integration.

### Azure SQL data types

The following table lists the data types that you can use with an Azure SQL data source when using access policy transformations in Data Integration: 

| Azure SQL data type | Data Access Management data type |
|---------------------|----------------------------------|
| bigint | integer |
| bit | integer |
| char | string |
| datetime | timestamp |
| datetime2 | timestamp |
| datetimeoffset | timestamp |
| decimal | decimal |
| float | decimal |
| geography | unknown |
| geometry | unknown |
| hierarchyid | unknown |
| int | integer |
| money | decimal |
| nchar | string |
| ntext | string |
| numeric | decimal |
| nvarchar | string |
| smalldatetime | timestamp |
| smallint | integer |
| smallmoney | decimal |
| sql_variant | unknown |
| text | string |
| time | timestamp |
| tinyint | integer |
| uniqueidentifier | unknown |
| varchar | string |
| xml | unknown |

### Azure Synapse data types

The following table lists the data types that you can use with an Azure Synapse data source when using access policy transformations in Data Integration: 

| Azure Synapse data type | Data Access Management data type |
|-------------------------|----------------------------------|
| bigint | integer |
| bit | integer |
| char | string |
| date | timestamp |
| datetime | timestamp |
| datetime2 | timestamp |
| datetimeoffset | string |
| decimal | decimal |
| float | decimal |
| int | integer |
| money | decimal |
| nchar | string |
| numeric | decimal |
| nvarchar | string |
| real | decimal |
| smallint | integer |
| smallmoney | decimal |
| smalldatetime | timestamp |
| tinyint | integer |
| uniqueidentifier | string |
| varchar | string |

### Databricks Delta data types

The following table lists the data types that you can use with a Databricks Delta Lake data source when using access policy transformations in Data Integration: 

| Databricks Delta data type | Data Access Management data type |
|----------------------------|----------------------------------|
| array | unknown |
| bigint | integer |
| char | string |
| date | date |
| decimal | decimal |
| double | decimal |
| float | decimal |
| int | integer |
| map | unknown |
| smallint | integer |
| string | string |
| struct | unknown |
| timestamp | timestamp |
| timestamp_ntz | timestamp |
| tinyint | integer |

### Microsoft SQL Server data types

The following table lists the data types that you can use with a Microsoft SQL Server data source when using the Managed Access setting in a delivery template in Data Marketplace and with access policy transformations in Data Integration: 

| Microsoft SQL Server data type | Data Access Management data type |
|--------------------------------|----------------------------------|
| bigint | integer |
| char | string |
| datetime | timestamp |
| datetime2 | timestamp |
| decimal | decimal |
| float | decimal |
| int | integer |
| money | decimal |
| nchar | string |
| ntext | string |
| numeric | decimal |
| nvarchar | string |
| smallmoney | decimal |
| text | string |
| varchar | string |

### PostgreSQL data types

The following table lists the data types that you can use with a PostgreSQL Server data source when using the Managed Access setting in a delivery template in Data Marketplace: 

| PostgreSQL data type | Data Access Management data type |
|----------------------|----------------------------------|
| int2 (smallint) | integer |
| int4 (integer) | integer |
| int8 (bigint) | integer |
| numeric (decimal) | decimal |
| float4 (real) | decimal |
| float8 (double) | decimal |
| varchar | string |
| text | string |
| date | date |
| timestamp | timestamp |
| timestampz | timestamp |
| smallserial | integer |
| money | decimal |

### Oracle data types

The following table lists the data types that you can use with an Oracle data source when using the Managed Access setting in a delivery template in Data Marketplace and with access policy transformations in Data Integration: 

| Oracle data type | Data Access Management data type |
|------------------|----------------------------------|
| CHAR | string |
| DATE | timestamp |
| DECIMAL | decimal |
| DOUBLE PRECISION | decimal |
| FLOAT | decimal |
| INTEGER | decimal |
| LONG | string |
| NCHAR | string |
| NUMBER | decimal |
| NVARCHAR2 | string |
| REAL | decimal |
| SMALLINT | decimal |
| TIMESTAMP | timestamp |
| TIMESTAMP WITH LOCAL TIME ZONE | timestamp |
| VARCHAR | string |
| VARCHAR2 | string |

### Available data protections

The following table lists the data protections that you can use with Data Access Management data types:

| Data Access Management data type | Description | Available data protections |
|----------------------------------|-------------|----------------------------|
| date | A calendar date | generalize date, redact to null, retain |
| decimal | A numeric value | redact to null, retain |
| integer | A positive natural number or zero | regular expression number generator, redact to null, retain |
| string | A sequence of characters | constant text value, truncate text, regular expression, redact to null, retain |
| timestamp | The date and time that an event occurred | generalize date, redact to null, retain |
| unknown | No corresponding data type in Data Access Management | redact to null, retain |
