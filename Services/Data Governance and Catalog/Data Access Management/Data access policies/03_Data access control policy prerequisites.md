# Data access control policy prerequisites

Data Access Management を有効にして、データアクセス制御ポリシーをソースシステムにプッシュするには、次のタスクを完了します:

**General prerequisites**
: データアクセス制御ポリシーを、Data Governance and Catalog がサポートするカタログソースタイプに関連付けます。

**Prerequisites for Snowflake**
: Snowflake ソースシステムに関連付けられた接続に次の権限を付与します:

```
GRANT MANAGE GRANTS ON ACCOUNT TO [IDMC_USER_ROLE];
GRANT CREATE ROLE ON ACCOUNT TO [IDMC_USER_ROLE];
```

**Prerequisites for Databricks**
: ポリシーをプッシュするために使用されるカタログソース接続で構成されているユーザーが、カタログソースのワークスペース管理者権限を持っていることを確認します。

**Note:** Data Access Management を通じて Databricks インスタンスに接続するには、個人用アクセストークンを使用してください。

: カタログソースを構成するには、Informatica Intelligent Cloud Services 管理者 Connections ドキュメントの「Connect to Databricks」の手順に従ってください。
