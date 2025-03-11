# Supported assets for automated data quality rules

You can define and run automated data quality rules for the business and technical asset types.

## Business assets

The following list shows the supported business assets:

- Data Set
- Data Quality Rule Template
- Glossary Business Term
- Glossary Domain
- Glossary Subdomain
- Glossary Metric
- Process
- Policy
- System

## Technical assets

The following table shows the supported technical assets and the associated data types:

### Amazon Athena

The following list shows the supported data types for the asset:
- bigint
- boolean
- char
- date
- decimal
- double
- float
- int
- smallint
- string
- timestamp
- tinyint
- varchar

### Amazon Redshift

The following list shows the supported data types for the asset:
- smallint
- integer
- bigint
- decimal
- real
- double precision
- boolean
- char
- varchar
- date
- timestamp
- timestamptz
- geometry
- geography
- hllsketch
- super
- time
- timetz
- varbyte

### Amazon S3

The string data type is supported for delimited CSV technical asset.
- The following list shows the supported data types for Avro technical asset:
  - boolean
  - int
  - long
  - double
  - string
  - record
  - array
- The following list shows the supported data types for Parquet technical asset:
  - boolean
  - int32
  - int64
  - int96
  - float
  - double
  - date
  - decimal
  - string
  - time
  - map
  - struct

### Google BigQuery

The following list shows the supported data types for the asset:
- boolean
- date
- datetime
- float
- integer
- numeric
- string
- time
- timestamp

### Google Cloud Storage

- The following list shows the supported data types for Avro technical asset:
  - boolean
  - int
  - long
  - double
  - string
  - record
  - array
- The following list shows the supported data types for Parquet technical asset:
  - boolean
  - int32
  - int64
  - int96
  - float
  - double
  - date
  - decimal
  - string
  - time
  - map
  - struct

### JDBC

The following list shows the supported data types for the asset:
- bigint
- char(L)
- date
- decimal (p,s)
- float
- graphic
- integer
- numeric (p,s)
- smallint
- time
- timestamp
- varchar
- vargraphic

### Microsoft Azure Data Lake Storage Gen2

- The following list shows the supported data types for Avro technical asset:
  - boolean
  - int
  - long
  - double
  - string
  - record
  - array
- The following list shows the supported data types for Parquet technical asset:
  - boolean
  - int32
  - int64
  - int96
  - float
  - double
  - date
  - decimal
  - string
  - time
  - map
  - struct

### Microsoft Azure SQL Server

The following list shows the supported data types for the asset:
- bigint
- numeric
- bit
- decimal
- int
- money
- smallint
- smallmoney
- tinyint
- float
- real
- date
- datetime2
- smalldatetime
- datetime
- time
- char
- varchar
- text
- nchar
- nvarchar
- ntext

### Microsoft Azure Synapse

The following list shows the supported data types for the asset:
- datetime2
- datetime
- date
- time
- float
- real
- decimal
- numeric
- money
- smallmoney
- bigint
- int
- smallint
- tinyint
- bit
- nvarchar
- nchar
- varchar
- char

### Microsoft SQL Server

The following list shows the supported data types for the asset:
- bigint
- numeric
- bit
- decimal
- int
- money
- smallint
- smallmoney
- tinyint
- float
- real
- date
- datetime2
- smalldatetime
- datetime
- time
- char
- varchar
- text
- nchar
- nvarchar
- ntext

### Oracle

The following list shows the supported data types for Oracle and Oracle RDS assets:
- char
- date
- number
- number (p,s)
- timestamp
- varchar
- varchar2
- nchar
- nvarchar2
- double precision / float (126)
- timestamp with timezone
- timestamp with local timezone
- long
- interval day to second
- interval year to month
- binary float
- binary double
- float
- urowid
- rowid

### SAP ERP

The following list shows the supported data types for SAP ERP assets:
- char
- clnt
- cuky
- curr
- dats
- dec
- int1
- int2
- lang
- lchr
- numc
- quan
- sstrg
- strg
- tims
- unit

### Salesforce

The following list shows the supported data types for the asset:
- id
- reference
- boolean
- string
- datetime
- date
- double
- url
- percent
- currency
- phone
- textarea
- email

### Snowflake

The following list shows the supported data types for the asset:
- number
- float/double
- varchar
- boolean
- date
- time
- timestamp_ltz
- timestamp_ntz
- timestamp_tz
- object
- array
- variant
