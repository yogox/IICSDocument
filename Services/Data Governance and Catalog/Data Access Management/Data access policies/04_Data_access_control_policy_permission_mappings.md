When you configure a data access control policy to grant data access permissions to a user in a catalog source, bear in mind that different catalog source systems apply the policy permissions in different ways.

The following table lists the permissions that you can configure in a data access control policy and the corresponding permissions that the policy enables in Databricks and Snowflake:

| Policy Permission in Data Access Management | Databricks Permission | Snowflake Permission |
|---|---|---|
| read | select | select |
| write | modify | insert
update |
| delete | [not applicable] | delete |

Note the following guidelines when you configure data access control policy permissions:

• Because views are read-only objects, a source system will ignore permissions other than read when a policy applies to a view.

• The delete permission does not apply to Databricks. The Databricks modify permission grants write and delete access. If you grant write permission to a Databricks object, you are also implicitly granting delete permission. If you select the delete permission, you do not grant any permission.

• For the Databricks Unity and Hive catalog types, Data Access Management grants usage permissions to catalogs and schemas.

• For Snowflake catalogs, Data Access Management grants usage permissions to databases and schemas.
