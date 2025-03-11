# Get details of an asset

To retrieve complete details of a particular asset, send a GET request using the search API. Based on the request URL parameters that you pass, the response includes details such as profiling, classification, relationships, custom attributes, and lineage information of the specified asset.

To get the details of an asset, submit a request with the following method and endpoint, and specify the asset ID:

| Method | Endpoint |
|--------|----------|
| GET | `<baseApiUrl>/data360/search/v1/assets/<assetID>` |

The `<baseApiUrl>` differs for each pod. For more information about the base API URL, see [Send Requests](../cloud-data-governance-and-catalog-api-reference/Send_Requests.html).

The `<assetID>` that you enter can be the internal ID or the external ID of the asset. You can specify in the `scheme` parameter of the request URL whether you want to search the asset by external ID or internal ID.

If you don't know the ID of a particular asset, you can first send a POST request using the `<baseApiUrl>/data360/search/assets` endpoint to view the list of assets in the catalog. The response for this request returns the internal ID of each asset in the `core.identity` parameter and the unique reference ID of the asset in the `core.externalId` parameter. For more information, see [List assets in the catalog](../cloud-data-governance-and-catalog-api-reference/List_assets_in_the_catalog.html).

## Request parameters

In the request URL parameters, specify the type of asset ID that you want to use to search for assets. To limit the API response to specific details of an asset, you can additionally specify the type of asset details that you want the request to return.

### Request parameters

Use the following parameters in the request URL:

| Parameter | Description |
|-----------|-------------|
| scheme | Specify the type of asset ID you want to use to query assets. Enter one of the following values:<br>- `internal`. Indicates that the asset ID that you specify in the request is the internal ID of the asset.<br>- `external`. Indicates that the asset ID that you specify in the request is the unique reference ID of the asset. |
| segments | Specify the type of asset details that you want the API request to return. The default value is `segments=all`.Enter any segment value from the following values:<br>- `all`. Returns the internal ID, external ID, summary, system attributes, and the API request link to view further details of the asset.<br>- `summary`. Returns the name, description, and location of the asset.<br>- `systemAttributes`. Returns the origin, class type, base types, user that created or updated the asset and the date on which the asset was created or updated.<br>- `stakeholdership`. Returns the type of user and role that are assigned as stakeholder for the asset.<br>- `customAttributes`. Returns the custom attributes specified for the asset.<br>- `selfAttributes`. Returns the properties of assets.<br>- `dataProfile`. Returns the profiling statistics of the asset.<br>- `dataClassification`. Returns the data classification associated with the asset.<br>- `glossary`. Returns the glossary associated with the asset.<br>- `dataQuality`. Returns the data quality score of the asset.<br>- `hierarchy`. Returns the immediate child assets of the asset.<br>- `hierarchy:all`. Returns all the attributes of the immediate child assets in the hierarchy.<br>- `hierarchy:selfAttributes`. Returns the properties of the immediate child assets in the hierarchy.<br>- `hierarchy:systemAttributes`. Returns the system attributes of the immediate child assets in the hierarchy.<br>- `hierarchy:customAttributes`. Returns the custom attributes of the immediate assets in the hierarchy.<br>- `neighborhood`. Returns assets that are in a direct relationship with the searched asset.<br>- `neighborhood:all`. Returns assets that are in a direct or indirect relationship with the searched asset.<br>- `neighborhood:<classtype>`. Returns assets of the specified class type that are in a direct relationship with the searched asset.<br>- `lineage-level`. Returns the lineage level of the asset, that is data element or data set level. The default value for `lineage-level` is `dataset`.<br>- `lineage-direction`. Returns the direction of the asset in the lineage, that is inbound or outbound. The default value for `lineage-direction` is `all`.<br>- `lineage-level:dataset`. Returns assets that have a direct relationship with the searched asset.<br>- `lineage-direction:all`. Returns assets that are in a direct inbound and outbound relationship with the searched asset.<br>- `lineage-direction:inbound`. Returns assets that are in a direct inbound relationship with the searched asset.<br>- `lineage-direction:outbound`. Returns assets that are in a direct outbound relationship with the searched asset.<br>- `descendants`. Returns the immediate children and related child assets.<br>- `descendants:all`. Returns all the details of the immediate and related child assets.<br>- `descendants:systemAttributes`. Returns the system attributes of the immediate and related child assets.<br>- `descendants:selfAttributes`. Returns the properties of the immediate and related child assets.<br>- `descendants:customAttributes`. Returns the custom attributes of the immediate and related child assets. |

## Examples

### Search for a business term using the asset ID

The following example shows the GET request to get all the details of a business term by specifying its internal ID.

```
GET https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets/612adac1-5863-468f-a38c-fb3ba0a5686e?scheme=internal&segments=all
```

The following example shows the response for the request. The response returns all details of the business term 'AddressLine2' because the `segments` parameter in the request is set to `all`.

```
{
    "core.identity": "17b1e3ed-f64f-487a-b073-06b78ec30259",
    "core.externalId": "lower-68",
    "summary": {
        "core.location": "CDGC://17b1e3ed-f64f-487a-b073-06b78ec30259",
        "core.name": "AddressLine2"
    },
    "systemAttributes": {
        "core.modifiedOn": 1688816931942,
        "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
        "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
        "core.classType": "com.infa.ccgf.models.governance.BusinessTerm",
        "core.origin": "CDGC",
        "type": [
            "core.IClassBusiness",
            "core.IClass",
            "com.infa.ccgf.models.governance.GlossaryBase",
            "com.infa.ccgf.models.governance.BusinessTerm"
        ],
        "core.createdOn": 1688816931942
    },
    "customAttributes": {
        "com.infa.odin.models.custom.ca_2205258177888237465": "default",
        "com.infa.odin.models.custom.ca_5534006856514172118": "default"
    },
    "selfAttributes": {
        "com.infa.ccgf.models.governance.FormatType": "Text",
        "core.supplement.certified": [
            false
        ],
        "core.assetLifecycle": "Published",
        "core.producer": "CDGC",
        "com.infa.ccgf.models.governance.isCDE": false
    },
    "dataProfile": {
        "core.classType": "com.infa.ccgf.models.governance.BusinessTerm",
        "core.identity": "17b1e3ed-f64f-487a-b073-06b78ec30259",
        "core.producer": "CDGC",
        "core.origin": "CDGC",
        "core.externalId": "lower-68",
        "core.name": "AddressLine2"
    },
    "neighborhood": [
        {
            "type": "com.infa.odin.models.file.flat.FlatField",
            "neighbors": [
                {
                    "neighbor": "AddressLine2",
                    "details": "/data360/search/assets/86aa9780-99d3-4efb-95ea-b4d691bb97d0?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                    "paths": [
                        {
                            "serialized": "lower-68 ( AddressLine2 )  <-- com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase -- dqprofiling-dockerpod/courses/person1.csv/AddressLine2~com.infa.odin.models.file.flat.FlatField ( AddressLine2 ) ",
                            "collection": [
                                {
                                    "association": "com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase",
                                    "curationStatus": "AUTO_ACCEPTED",
                                    "from": "AddressLine2",
                                    "to": "AddressLine2",
                                    "fromType": "com.infa.odin.models.file.flat.FlatField",
                                    "toType": "com.infa.ccgf.models.governance.BusinessTerm",
                                    "fromLocation": "99068dfb-2c91-34e2-bd37-5232fde620b1://99068dfb-2c91-34e2-bd37-5232fde620b1/dqprofiling-dockerpod/courses/person1.csv/AddressLine2",
                                    "toLocation": "CDGC://17b1e3ed-f64f-487a-b073-06b78ec30259",
                                    "attributes": {
                                        "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                        "core.origin": "99068dfb-2c91-34e2-bd37-5232fde620b1",
                                        "core.modifiedOn": 1689076624370,
                                        "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                        "core.confidenceScore": 100.0,
                                        "core.inferred": true,
                                        "core.associationKind": "com.infa.ccgf.models.governance.semanticKind",
                                        "core.producer": "discovery-capability",
                                        "core.createdOn": 1689076624370,
                                        "core.curationStatus": "AUTO_ACCEPTED"
                                    },
                                    "details": {
                                        "fromUri": "/data360/search/assets/86aa9780-99d3-4efb-95ea-b4d691bb97d0?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                        "toUri": "/data360/search/assets/lower-68?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                    },
                                    "fromProperties": {
                                        "core.identity": "86aa9780-99d3-4efb-95ea-b4d691bb97d0",
                                        "core.classType": "com.infa.odin.models.file.flat.FlatField",
                                        "core.location": "99068dfb-2c91-34e2-bd37-5232fde620b1://99068dfb-2c91-34e2-bd37-5232fde620b1/dqprofiling-dockerpod/courses/person1.csv/AddressLine2",
                                        "core.externalId": "dqprofiling-dockerpod/courses/person1.csv/AddressLine2~com.infa.odin.models.file.flat.FlatField",
                                        "core.name": "AddressLine2"
                                    },
                                    "toProperties": {
                                        "core.identity": "17b1e3ed-f64f-487a-b073-06b78ec30259",
                                        "core.classType": "com.infa.ccgf.models.governance.BusinessTerm",
                                        "core.location": "CDGC://17b1e3ed-f64f-487a-b073-06b78ec30259",
                                        "core.externalId": "lower-68",
                                        "core.name": "AddressLine2"
                                    }
                                }
                            ]
                        }
                    ]
                }
            ]
        }
    ]
}
```

### Search for a column using the asset ID

The following example shows the GET request to get all the details of a column by specifying its internal ID.

```
GET https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets/6bb417e6-94bb-48eb-88b6-7c6887b58fb6?scheme=internal&segments=all
```

The following example shows the request response. The response includes all details of the column such as the summary, system attributes, glossary associations, data profiling statistics, and relationships with other assets.

```
{
    "core.identity": "5ab1fc47-68aa-4182-ab8e-80c8dc58e95d",
    "core.externalId": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
    "summary": {
        "core.location": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://ab2cc915-4b30-396a-9632-bd89f02ddf1c/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
        "core.name": "CDGCTABL31COL2",
        "core.description": ""
    },
    "systemAttributes": {
        "core.modifiedOn": 1692954334099,
        "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
        "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
        "core.classType": "com.infa.odin.models.relational.Column",
        "core.origin": "ab2cc915-4b30-396a-9632-bd89f02ddf1c",
        "type": [
            "core.IClassTechnical",
            "core.IClass",
            "core.DataElement",
            "com.infa.odin.models.relational.Column"
        ],
        "core.createdOn": 1689007685160
    },
    "selfAttributes": {
        "com.infa.odin.models.relational.DatatypeLength": "100",
        "core.reference": false,
        "core.Position": 2,
        "core.rankArray": [],
        "core.patternStatistics": [],
        "com.infa.odin.models.relational.PrimaryKeyColumn": "false",
        "core.mergedObjects": [],
        "core.businessName": "Customer Records",
        "core.profiled": false,
        "core.resourceType": "Snowflake",
        "core.businessDescription": "",
        "core.lastProfiledState": "Not Profiled",
        "com.infa.odin.models.relational.Datatype": "VARCHAR",
        "core.supplement.certified": [
            false
        ],
        "com.infa.odin.models.relational.Nullable": "true",
        "core.assetLifecycle": "Published",
        "core.resourceName": "SnowFlake_10June_22-10",
        "core.inferredDataTypeSummaries": []
    },
    "dataProfile": {
        "core.lastProfiledState": "Not Profiled",
        "core.topNValueFrequenciesSample": [],
        "core.rankArray": [],
        "core.patternStatistics": [],
        "core.profiled": false,
        "core.classType": "com.infa.odin.models.relational.Column",
        "core.identity": "5ab1fc47-68aa-4182-ab8e-80c8dc58e95d",
        "core.origin": "ab2cc915-4b30-396a-9632-bd89f02ddf1c",
        "core.externalId": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
        "core.name": "CDGCTABL31COL2",
        "core.inferredDataTypeSummaries": [],
        "core.description": ""
    },
    "glossary": [
        {
            "core.identity": "7bc6fa52-b563-48a2-9f3a-643b02cc4421",
            "details": "/data360/search/assets/MLMRSCOE-24?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes",
            "core.externalId": "MLMRSCOE-24",
            "core.name": "Customer Records",
            "core.curationStatus": "ACCEPTED"
        }
    ],
    "neighborhood": [
        {
            "type": "com.infa.odin.models.relational.Table",
            "neighbors": [
                {
                    "neighbor": "CDGCTABLE3",
                    "details": "/data360/search/assets/4e648258-9937-4197-a933-92d35889fbb0?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                    "paths": [
                        {
                            "serialized": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column ( CDGCTABL31COL2 )  <-- com.infa.odin.models.relational.TableToColumn -- CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3~com.infa.odin.models.relational.Table ( CDGCTABLE3 ) ",
                            "collection": [
                                {
                                    "association": "com.infa.odin.models.relational.TableToColumn",
                                    "curationStatus": "NONE",
                                    "from": "CDGCTABLE3",
                                    "to": "CDGCTABL31COL2",
                                    "fromType": "com.infa.odin.models.relational.Table",
                                    "toType": "com.infa.odin.models.relational.Column",
                                    "fromLocation": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://ab2cc915-4b30-396a-9632-bd89f02ddf1c/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3",
                                    "toLocation": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://ab2cc915-4b30-396a-9632-bd89f02ddf1c/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                    "attributes": {
                                        "core.modifiedOn": 1689007798639,
                                        "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                        "core.associationKind": "core.ParentChild",
                                        "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                        "core.origin": "ab2cc915-4b30-396a-9632-bd89f02ddf1c",
                                        "core.createdOn": 1689007798639
                                    },
                                    "details": {
                                        "fromUri": "/data360/search/assets/4e648258-9937-4197-a933-92d35889fbb0?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                        "toUri": "/data360/search/assets/5ab1fc47-68aa-4182-ab8e-80c8dc58e95d?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                    },
                                    "fromProperties": {
                                        "core.identity": "4e648258-9937-4197-a933-92d35889fbb0",
                                        "core.classType": "com.infa.odin.models.relational.Table",
                                        "core.location": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://ab2cc915-4b30-396a-9632-bd89f02ddf1c/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3",
                                        "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3~com.infa.odin.models.relational.Table",
                                        "core.name": "CDGCTABLE3"
                                    },
                                    "toProperties": {
                                        "core.identity": "5ab1fc47-68aa-4182-ab8e-80c8dc58e95d",
                                        "core.classType": "com.infa.odin.models.relational.Column",
                                        "core.location": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://ab2cc915-4b30-396a-9632-bd89f02ddf1c/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                        "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
                                        "core.name": "CDGCTABL31COL2"
                                    }
                                }
                            ]
                        }
                    ]
                }
            ]
        },
        {
            "type": "com.infa.ccgf.models.governance.BusinessTerm",
            "neighbors": [
                {
                    "neighbor": "Customer Records",
                    "details": "/data360/search/assets/MLMRSCOE-24?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes",
                    "paths": [
                        {
                            "serialized": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column ( CDGCTABL31COL2 )  -- com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase --> MLMRSCOE-24 ( Customer Records ) ",
                            "collection": [
                                {
                                    "association": "com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase",
                                    "curationStatus": "ACCEPTED",
                                    "from": "CDGCTABL31COL2",
                                    "to": "Customer Records",
                                    "fromType": "com.infa.odin.models.relational.Column",
                                    "toType": "com.infa.ccgf.models.governance.BusinessTerm",
                                    "fromLocation": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://ab2cc915-4b30-396a-9632-bd89f02ddf1c/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                    "toLocation": "CDGC://247e6a83-7ddb-4014-bd8b-eac7018a31e1/7bc6fa52-b563-48a2-9f3a-643b02cc4421",
                                    "attributes": {
                                        "core.modifiedOn": 1692954335818,
                                        "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                        "core.associationKind": "com.infa.ccgf.models.governance.semanticKind",
                                        "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                        "core.inferred": false,
                                        "core.producer": "CDGC",
                                        "core.origin": "CDGC",
                                        "core.createdOn": 1692954335818,
                                        "core.curationStatus": "ACCEPTED"
                                    },
                                    "details": {
                                        "fromUri": "/data360/search/assets/5ab1fc47-68aa-4182-ab8e-80c8dc58e95d?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                        "toUri": "/data360/search/assets/MLMRSCOE-24?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                    },
                                    "fromProperties": {
                                        "core.identity": "5ab1fc47-68aa-4182-ab8e-80c8dc58e95d",
                                        "core.classType": "com.infa.odin.models.relational.Column",
                                        "core.location": "ab2cc915-4b30-396a-9632-bd89f02ddf1c://ab2cc915-4b30-396a-9632-bd89f02ddf1c/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                        "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
                                        "core.name": "CDGCTABL31COL2"
                                    },
                                    "toProperties": {
                                        "core.identity": "7bc6fa52-b563-48a2-9f3a-643b02cc4421",
                                        "core.classType": "com.infa.ccgf.models.governance.BusinessTerm",
                                        "core.location": "CDGC://247e6a83-7ddb-4014-bd8b-eac7018a31e1/7bc6fa52-b563-48a2-9f3a-643b02cc4421",
                                        "core.externalId": "MLMRSCOE-24",
                                        "core.name": "Customer Records"
                                    }
                                }
                            ]
                        }
                    ]
                }
            ]
        }
    ]
}
```

## Response body

The GET request returns the details of the asset that you specify in the URL.

The details that the response body displays for business and technical assets are based on the values that you specify in the `segments` URL parameter while sending the GET request. For more information about the details returned in the response body, see `segments` in [Request parameters](../cloud-data-governance-and-catalog-api-reference/List_assets_in_the_catalog.html#ww3_9_7_7_1).
