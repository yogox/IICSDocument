# PostgreSQL

PostgreSQL is an open-source relational database management system (RDBMS) used as a data store or data warehouse for applications.

### Objects extracted

The metadata extraction service extracts the following objects from a PostgreSQL source system:

• Database
• Schema
• Table
• View
• Materialized View

**Note:** Objects of the Materialized View type appear as View in Data Governance and Catalog.

• Stored Procedure 

### Data profiling for PostgresSQL objects

Configure data profiling to run profiles on the metadata extracted from a PostgreSQL source system. You can run data profiles on the following PostgreSQL objects:

• Tables
• Views

Sampling type
: Determine the sample rows on which you want to run the data profiling task. You can choose any of the following sampling types for a PostgreSQL catalog source:
- All rows
- Limit N
- Custom query

### Prerequisites for configuring the PostgreSQL catalog source

Use the PostgreSQL connector to connect to PostgreSQL source system. For information about configuring a connection in Administrator, see Citations in the Cloud Common Services help. 

### Configure permissions or access to PostgreSQL

To extract metadata and run profiles, you need account access and permissions on the PostgreSQL source system.

Permissions to extract metadata
: Grant permissions that allow you to perform the following operations:
- select on pg_catalog.PG_ATTRIBUTE
- select on pg_catalog.PG_CLASS
- select on pg_catalog.PG_CONSTRAINT
- select on pg_catalog.PG_DATABASE
- select on pg_catalog.PG_DESCRIPTION
- select on pg_catalog.PG_LANGUAGE
- select on pg_catalog.PG_NAMESPACE
- select on pg_catalog.PG_PROC
- select on pg_catalog.PG_TYPE
- select on pg_catalog.PG_VIEWS
- select on information_schema.COLUMNS
- select on information_schema.TABLES
- select on pg_catalog.PG_TABLES
- select on pg_catalog.PG_MATVIEWS

To extract metadata from a table, you need to configure Select access on the table.

### Data classification for PostgreSQL objects

Configure data classification for PostgreSQL catalog sources to classify and organize data in your organization. You can view the data classification results in Data Governance and Catalog.

### Connection properties

When you configure a connection to the PostgreSQL source system in Administrator, you can view the connection properties for that connection on the Registration page in Metadata Command Center.

The following table describes the PostgreSQL connection properties:

| Property | Description |
|---|---|
| Runtime Environment | The name of the runtime environment where you want to run tasks. Select a Secure Agent, Hosted Agent, or serverless runtime environment. |
| Host Name | Host name of the PostgreSQL server to which you want to connect. |
| Port | Port number for the PostgreSQL server to which you want to connect. Default is 5432. |
| Database Name | The PostgreSQL database name. |
| Schema Name | The schema name. If you don't specify the schema name, all the schemas available in the database are listed when you import the source object. |
| User Name | User name to access the PostgreSQL database. |
| Password | Password for the PostgreSQL database user name. |
| Encryption Method | Determines whether the data exchanged between the Secure Agent and the PostgreSQL database server is encrypted. Select one of the following encryption methods: - noEncryption. Establishes a connection without using SSL. Data is not encrypted. - SSL. Establishes a connection using SSL. Data is encrypted using SSL. If the PostgreSQL database server cannot configure SSL, the connection fails. - requestSSL. Attempts to establish a connection using SSL. If the PostgreSQL database server cannot configure SSL, the Secure Agent establishes an unencrypted connection. Default is noEncryption |
| Validate Server Certificate | Determines if the Secure Agent validates the server certificate sent by the PostgreSQL database server. If you specify the Host Name In Certificate property, the Secure Agent also validates the host name in the certificate. |
| Truststore | This property applies if you select the Validate Server Certificate option. The path and name of the truststore file, which contains the list of the Certificate Authorities (CAs) that the PostgreSQL client trusts. |
| Truststore Password | This property applies if you select the Validate Server Certificate option. The password to access the truststore file that contains the SSL certificate. |
| Host Name In Certificate | Optional when you select the Validate Server Certificate option. A host name for providing additional security. The Secure Agent validates the host name included in the connection with the host name in the SSL certificate. |
| Keystore | This property applies when client authentication is enabled on the PostgreSQL database server. The path and the file name of the key store. The keystore file contains the certificates that the PostgreSQL client sends to the PostgreSQL server in response to the server's certificate request. |
| Keystore Password | This property applies when client authentication is enabled on the PostgreSQL database server. The password for the keystore file required for secure communication. |
| Key Password | This property applies when client authentication is enabled on the PostgreSQL database server. Required when individual keys in the keystore file have a different password than the keystore file. |
| Additional Connection Properties | Additional connection parameters that you want to use. Provide the connection parameters as semicolon-separated key-value pairs. |
| Crypto Protocol Versions | Required if you select SSL or requestSSL as the encryption method. A cryptographic protocol or a list of cryptographic protocols to use with an encrypted connection. You can select from the following protocols: - SSLv3 - TLSv1 - TLSv1_1 - TLSv1_2 |

### Configuration parameters for metadata extraction

Optionally, you can override default context values and job parameters on the Configuration tab.

**Note:** Click Show Advanced to view all configuration parameters.

The following table describes the configuration parameters that you enter for Catalog Source Configuration Options:

| Parameter | Description |
|---|---|
| Default variables values | Specify a default value for variables used in the programmable objects. |
| MetaTables Include Filter | Advanced parameter. When you process PL/SQL statements, Metadata Command Center does not read tables or view content by default. If you want to use the content, for example, to process dynamic SQL statements, use the MetaTables Include Filter parameter. This parameter prompts the database for the required metadata. Verify that the user has SELECT permissions for metatables. **Note:** Don't use this option to specify filters for tables that you want to include or exclude during the metadata extraction run. |

The following table describes the property that you can enter for additional settings:

**Note:** The Additional Settings section appears when you click Show Advanced.

| Property | Description |
|---|---|
| Expert Parameters | Enter additional configuration options to be passed at runtime. Required if you need to troubleshoot the catalog source job. **Caution:** Use expert parameters when it is recommended by Informatica Global Customer Support. |
