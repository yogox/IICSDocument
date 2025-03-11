# List details of multiple assets

Send a POST request to view the details of multiple assets in the catalog. While sending the request, you can specify the reference IDs of one or more assets in the body of the request. In the request parameters, specify the type of asset details that you would like to view.

To list the details of multiple assets, submit a request with the following method and endpoint, and specify the asset ID:

| Method | Endpoint |
|--------|----------|
| POST | `<baseApiUrl>/data360/search/v1/assets/details` |

The `<baseApiUrl>` differs for each pod. For more information about the base API URL, see [Send Requests](../cloud-data-governance-and-catalog-api-reference/Send_Requests.html).

## Request parameters

In the request URL parameters, specify the type of asset ID that you want to use to search for assets. To limit the API response to specific details of an asset, you can additionally specify the type of asset details that you want the request to return.

### Request parameters

Use the following parameters in the request URL:

| Parameter | Description |
|-----------|-------------|
| scheme | Specify the type of asset ID you want to use to query assets. Enter one of the following values:
- `internal`. Indicates that the asset ID that you specify in the request is the internal ID of the asset.
- `external`. Indicates that the asset ID that you specify in the request is the unique reference ID of the asset. |
| segments | Specify the type of asset details that you want the API request to return. The default value is `segments=all`.Enter any segment value from the following values:
- `all`. Returns the internal ID, external ID, summary, system attributes, and the API request link to view further details of the asset.
- `summary`. Returns the name, description, and location of the asset.
- `systemAttributes`. Returns the origin, class type, base types, user that created or updated the asset and the date on which the asset was created or updated.
- `stakeholdership`. Returns the type of user and role that are assigned as stakeholder for the asset.
- `customAttributes`. Returns the custom attributes specified for the asset.
- `selfAttributes`. Returns the properties of assets.
- `dataProfile`. Returns the profiling statistics of the asset.
- `dataClassification`. Returns the data classification associated with the asset.
- `glossary`. Returns the glossary associated with the asset.
- `dataQuality`. Returns the data quality score of the asset.
- `hierarchy`. Returns the immediate child assets of the asset.
- `hierarchy:all`. Returns all the attributes of the immediate child assets in the hierarchy.
- `hierarchy:selfAttributes`. Returns the properties of the immediate child assets in the hierarchy.
- `hierarchy:systemAttributes`. Returns the system attributes of the immediate child assets in the hierarchy.
- `hierarchy:customAttributes`. Returns the custom attributes of the immediate assets in the hierarchy.
- `neighborhood`. Returns assets that are in a direct relationship with the searched asset.
- `neighborhood:all`. Returns assets that are in a direct or indirect relationship with the searched asset.
- `neighborhood:<classtype>`. Returns assets of the specified class type that are in a direct relationship with the searched asset.
- `lineage-level`. Returns the lineage level of the asset, that is data element or data set level. The default value for `lineage-level` is `dataset`.
- `lineage-direction`. Returns the direction of the asset in the lineage, that is inbound or outbound. The default value for `lineage-direction` is `all`.
- `lineage-level:dataset`. Returns assets that have a direct relationship with the searched asset.
- `lineage-direction:all`. Returns assets that are in a direct inbound and outbound relationship with the searched asset.
- `lineage-direction:inbound`. Returns assets that are in a direct inbound relationship with the searched asset.
- `lineage-direction:outbound`. Returns assets that are in a direct outbound relationship with the searched asset.
- `descendants`. Returns the immediate children and related child assets.
- `descendants:all`. Returns all the details of the immediate and related child assets.
- `descendants:systemAttributes`. Returns the system attributes of the immediate and related child assets.
- `descendants:selfAttributes`. Returns the properties of the immediate and related child assets.
- `descendants:customAttributes`. Returns the custom attributes of the immediate and related child assets. |

## Request body

Use the request body to specify the external or internal IDs of assets that you want to view. You can specify in the `scheme` request parameter whether you want to search the asset by external ID or internal ID.

In the body of each API request, specify up to five comma-separated asset IDs. You can specify the asset IDs in the following format:

```
[
    "0c5777c2-ec04-4a57-8bf0-fc895c4579a2",
    "982cd858-b5b0-4cea-b120-cad3c325e38e",
    "e907f08f-6327-4214-9401-c794bc0c34db",
]
```

If you don't know the ID of a particular asset, you can first send a POST request to view the list of assets in the catalog. This request returns the internal ID of each asset in the `core.identity` parameter and the unique reference ID of the asset in the `core.externalId` parameter. For more information, see [List assets in the catalog](../cloud-data-governance-and-catalog-api-reference/List_assets_in_the_catalog.html).

## Example request

### Search for two assets using internal asset IDs

The following example shows the POST request to list all the details of a column and an associated business term by passing the internal IDs of both the assets in the request body.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets/details?scheme=internal&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
[
    "81e8ea5a-c888-4c40-a780-849ac48e66fd",
    "17b1e3ed-f64f-487a-b073-06b78ec30259"
]
```

The following example shows the response for the request. The response returns all the details of the business term 'AddressLine2' and the column 'CDGCTABL31COL2' because the `segments` parameter in the request is set to `all`.

```
[
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
                    },
                    {
                        "neighbor": "AddressLine2",
                        "details": "/data360/search/assets/00b1dbb0-ee68-43e9-a833-675b5c8f0ab2?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
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
                                        "fromLocation": "27397996-ad9a-3f32-8093-2e4b80fcd93c://27397996-ad9a-3f32-8093-2e4b80fcd93c/dqprofiling-dockerpod/courses/person1.csv/AddressLine2",
                                        "toLocation": "CDGC://17b1e3ed-f64f-487a-b073-06b78ec30259",
                                        "attributes": {
                                            "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.origin": "27397996-ad9a-3f32-8093-2e4b80fcd93c",
                                            "core.modifiedOn": 1688819441749,
                                            "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.confidenceScore": 100.0,
                                            "core.inferred": true,
                                            "core.associationKind": "com.infa.ccgf.models.governance.semanticKind",
                                            "core.producer": "discovery-capability",
                                            "core.createdOn": 1688819441749,
                                            "core.curationStatus": "AUTO_ACCEPTED"
                                        },
                                        "details": {
                                            "fromUri": "/data360/search/assets/00b1dbb0-ee68-43e9-a833-675b5c8f0ab2?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                            "toUri": "/data360/search/assets/lower-68?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                        },
                                        "fromProperties": {
                                            "core.identity": "00b1dbb0-ee68-43e9-a833-675b5c8f0ab2",
                                            "core.classType": "com.infa.odin.models.file.flat.FlatField",
                                            "core.location": "27397996-ad9a-3f32-8093-2e4b80fcd93c://27397996-ad9a-3f32-8093-2e4b80fcd93c/dqprofiling-dockerpod/courses/person1.csv/AddressLine2",
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
            },
            {
                "type": "com.infa.odin.models.relational.Column",
                "neighbors": [
                    {
                        "neighbor": "CDGCTABL31COL2",
                        "details": "/data360/search/assets/81e8ea5a-c888-4c40-a780-849ac48e66fd?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                        "paths": [
                            {
                                "serialized": "lower-68 ( AddressLine2 )  <-- com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase -- CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column ( CDGCTABL31COL2 ) ",
                                "collection": [
                                    {
                                        "association": "com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase",
                                        "curationStatus": "ACCEPTED",
                                        "from": "CDGCTABL31COL2",
                                        "to": "AddressLine2",
                                        "fromType": "com.infa.odin.models.relational.Column",
                                        "toType": "com.infa.ccgf.models.governance.BusinessTerm",
                                        "fromLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                        "toLocation": "CDGC://17b1e3ed-f64f-487a-b073-06b78ec30259",
                                        "attributes": {
                                            "core.modifiedOn": 1692806775314,
                                            "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.associationKind": "com.infa.ccgf.models.governance.semanticKind",
                                            "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.inferred": false,
                                            "core.producer": "CDGC",
                                            "core.origin": "CDGC",
                                            "core.createdOn": 1692806775314,
                                            "core.curationStatus": "ACCEPTED"
                                        },
                                        "details": {
                                            "fromUri": "/data360/search/assets/81e8ea5a-c888-4c40-a780-849ac48e66fd?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                            "toUri": "/data360/search/assets/lower-68?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                        },
                                        "fromProperties": {
                                            "core.identity": "81e8ea5a-c888-4c40-a780-849ac48e66fd",
                                            "core.classType": "com.infa.odin.models.relational.Column",
                                            "core.location": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                            "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
                                            "core.name": "CDGCTABL31COL2"
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
    },
    {
        "core.identity": "81e8ea5a-c888-4c40-a780-849ac48e66fd",
        "core.externalId": "d4865a0f-406b-363e-b850-2fc633b3f77b://CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
        "summary": {
            "core.location": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
            "core.name": "CDGCTABL31COL2",
            "core.description": ""
        },
        "systemAttributes": {
            "core.modifiedOn": 1692806773089,
            "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
            "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
            "core.classType": "com.infa.odin.models.relational.Column",
            "core.origin": "d4865a0f-406b-363e-b850-2fc633b3f77b",
            "type": [
                "core.IClassTechnical",
                "core.IClass",
                "core.DataElement",
                "com.infa.odin.models.relational.Column"
            ],
            "core.createdOn": 1688650669237
        },
        "selfAttributes": {
            "com.infa.odin.models.relational.DatatypeLength": "100",
            "core.reference": false,
            "core.Position": 2,
            "core.rankArray": [],
            "core.patternStatistics": [],
            "com.infa.odin.models.relational.PrimaryKeyColumn": "false",
            "core.mergedObjects": [],
            "core.businessName": "AddressLine2",
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
            "core.resourceName": "SnowFlake_CustCheck",
            "core.inferredDataTypeSummaries": []
        },
        "dataProfile": {
            "core.lastProfiledState": "Not Profiled",
            "core.topNValueFrequenciesSample": [],
            "core.rankArray": [],
            "core.patternStatistics": [],
            "core.profiled": false,
            "core.classType": "com.infa.odin.models.relational.Column",
            "core.identity": "81e8ea5a-c888-4c40-a780-849ac48e66fd",
            "core.origin": "d4865a0f-406b-363e-b850-2fc633b3f77b",
            "core.externalId": "d4865a0f-406b-363e-b850-2fc633b3f77b://CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
            "core.name": "CDGCTABL31COL2",
            "core.inferredDataTypeSummaries": [],
            "core.description": ""
        },
        "glossary": [
            {
                "core.identity": "17b1e3ed-f64f-487a-b073-06b78ec30259",
                "details": "/data360/search/assets/lower-68?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes",
                "core.externalId": "lower-68",
                "core.name": "AddressLine2",
                "core.curationStatus": "ACCEPTED"
            }
        ],
        "neighborhood": [
            {
                "type": "com.infa.odin.models.relational.Table",
                "neighbors": [
                    {
                        "neighbor": "CDGCTABLE3",
                        "details": "/data360/search/assets/44ef664f-90ef-4ac2-af4d-a99f7670081b?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
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
                                        "fromLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3",
                                        "toLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                        "attributes": {
                                            "core.modifiedOn": 1688650827020,
                                            "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.associationKind": "core.ParentChild",
                                            "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.origin": "d4865a0f-406b-363e-b850-2fc633b3f77b",
                                            "core.createdOn": 1688650827020
                                        },
                                        "details": {
                                            "fromUri": "/data360/search/assets/44ef664f-90ef-4ac2-af4d-a99f7670081b?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                            "toUri": "/data360/search/assets/81e8ea5a-c888-4c40-a780-849ac48e66fd?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                        },
                                        "fromProperties": {
                                            "core.identity": "44ef664f-90ef-4ac2-af4d-a99f7670081b",
                                            "core.classType": "com.infa.odin.models.relational.Table",
                                            "core.location": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3",
                                            "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3~com.infa.odin.models.relational.Table",
                                            "core.name": "CDGCTABLE3"
                                        },
                                        "toProperties": {
                                            "core.identity": "81e8ea5a-c888-4c40-a780-849ac48e66fd",
                                            "core.classType": "com.infa.odin.models.relational.Column",
                                            "core.location": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
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
                "type": "com.infa.odin.models.relational.ViewColumn",
                "neighbors": [
                    {
                        "neighbor": "CDGCVIEW3COL2",
                        "details": "/data360/search/assets/a1172b78-75cb-4485-88dd-8b407441187a?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                        "paths": [
                            {
                                "serialized": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column ( CDGCTABL31COL2 )  -- core.DirectionalDataFlow --> CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCVIEW3/CDGCVIEW3COL2~com.infa.odin.models.relational.ViewColumn ( CDGCVIEW3COL2 ) ",
                                "collection": [
                                    {
                                        "association": "core.DirectionalDataFlow",
                                        "curationStatus": "NONE",
                                        "from": "CDGCTABL31COL2",
                                        "to": "CDGCVIEW3COL2",
                                        "fromType": "com.infa.odin.models.relational.Column",
                                        "toType": "com.infa.odin.models.relational.ViewColumn",
                                        "fromLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                        "toLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCVIEW3/CDGCVIEW3COL2",
                                        "attributes": {
                                            "core.modifiedOn": 1688650826911,
                                            "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.associationKind": "core.DataFlow",
                                            "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.origin": "d4865a0f-406b-363e-b850-2fc633b3f77b",
                                            "core.createdOn": 1688650826911
                                        },
                                        "details": {
                                            "fromUri": "/data360/search/assets/81e8ea5a-c888-4c40-a780-849ac48e66fd?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                            "toUri": "/data360/search/assets/a1172b78-75cb-4485-88dd-8b407441187a?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                        },
                                        "fromProperties": {
                                            "core.identity": "81e8ea5a-c888-4c40-a780-849ac48e66fd",
                                            "core.classType": "com.infa.odin.models.relational.Column",
                                            "core.location": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                            "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
                                            "core.name": "CDGCTABL31COL2"
                                        },
                                        "toProperties": {
                                            "core.identity": "a1172b78-75cb-4485-88dd-8b407441187a",
                                            "core.classType": "com.infa.odin.models.relational.ViewColumn",
                                            "core.location": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCVIEW3/CDGCVIEW3COL2",
                                            "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCVIEW3/CDGCVIEW3COL2~com.infa.odin.models.relational.ViewColumn",
                                            "core.name": "CDGCVIEW3COL2"
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
                        "neighbor": "AddressLine2",
                        "details": "/data360/search/assets/lower-68?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes",
                        "paths": [
                            {
                                "serialized": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column ( CDGCTABL31COL2 )  -- com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase --> lower-68 ( AddressLine2 ) ",
                                "collection": [
                                    {
                                        "association": "com.infa.ccgf.models.governance.IClassTechnicalGlossaryBase",
                                        "curationStatus": "ACCEPTED",
                                        "from": "CDGCTABL31COL2",
                                        "to": "AddressLine2",
                                        "fromType": "com.infa.odin.models.relational.Column",
                                        "toType": "com.infa.ccgf.models.governance.BusinessTerm",
                                        "fromLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                        "toLocation": "CDGC://17b1e3ed-f64f-487a-b073-06b78ec30259",
                                        "attributes": {
                                            "core.modifiedOn": 1692806775314,
                                            "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.associationKind": "com.infa.ccgf.models.governance.semanticKind",
                                            "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                            "core.inferred": false,
                                            "core.producer": "CDGC",
                                            "core.origin": "CDGC",
                                            "core.createdOn": 1692806775314,
                                            "core.curationStatus": "ACCEPTED"
                                        },
                                        "details": {
                                            "fromUri": "/data360/search/assets/81e8ea5a-c888-4c40-a780-849ac48e66fd?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                            "toUri": "/data360/search/assets/lower-68?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes"
                                        },
                                        "fromProperties": {
                                            "core.identity": "81e8ea5a-c888-4c40-a780-849ac48e66fd",
                                            "core.classType": "com.infa.odin.models.relational.Column",
                                            "core.location": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                            "core.externalId": "CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2~com.infa.odin.models.relational.Column",
                                            "core.name": "CDGCTABL31COL2"
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
        ],
        "lineage": [
            {
                "direction": "outbound",
                "hops": [
                    {
                        "distance": 1,
                        "items": [
                            {
                                "from": "CDGCTABL31COL2",
                                "to": "CDGCVIEW3COL2",
                                "fromType": "com.infa.odin.models.relational.Column",
                                "toType": "com.infa.odin.models.relational.ViewColumn",
                                "fromLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCTABLE3/CDGCTABL31COL2",
                                "toLocation": "d4865a0f-406b-363e-b850-2fc633b3f77b://d4865a0f-406b-363e-b850-2fc633b3f77b/CDGC_QE_SNOWFLAKE/CDGC_QE_SCHEMA/CDGCVIEW3/CDGCVIEW3COL2",
                                "attributes": {
                                    "core.modifiedOn": 1688650826911,
                                    "core.createdBy": "5gwD6d18cwPeUaAJAyev2V",
                                    "core.associationKind": "core.DataFlow",
                                    "core.modifiedBy": "5gwD6d18cwPeUaAJAyev2V",
                                    "__meta.association": "core.DirectionalDataFlow",
                                    "core.origin": "d4865a0f-406b-363e-b850-2fc633b3f77b",
                                    "core.createdOn": 1688650826911
                                },
                                "details": {
                                "fromUri": "/data360/search/v1/assets/812526be-c8e0-48f9-a82c-53055cb5d0e3?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes",
                                "toUri": "/data360/search/v1/assets/7635cb3e-3425-4440-9244-ce516f197ec5?scheme=internal&segments=summary,systemAttributes,customAttributes,selfAttributes"
                            },
                            "fromProperties": {
                                "core.identity": "812526be-c8e0-48f9-a82c-53055cb5d0e3",
                                "core.classType": "core.DataElement",
                                "core.location": "f2c12406-bb40-377e-ae1d-56574cf056e5://f2c12406-bb40-377e-ae1d-56574cf056e5/f2c12406-bb40-377e-ae1d-56574cf056e5_S3__infagcstest/S3__infagcstest/rodfolder/bucket",
                                "core.externalId": "f2c12406-bb40-377e-ae1d-56574cf056e5_S3__infagcstest://S3__infagcstest/rodfolder/bucket~core.DataElement",
                                "core.name": "bucket"
                            },
                            "toProperties": {
                                "core.identity": "7635cb3e-3425-4440-9244-ce516f197ec5",
                                "core.classType": "com.infa.odin.models.relational.ExternalColumn",
                                "core.location": "f2c12406-bb40-377e-ae1d-56574cf056e5://f2c12406-bb40-377e-ae1d-56574cf056e5/ATHENA-DB/gcsinstance/account_managers/bucket",
                                "core.externalId": "f2c12406-bb40-377e-ae1d-56574cf056e5://ATHENA-DB/gcsinstance/account_managers/bucket~com.infa.odin.models.relational.ExternalColumn",
                                "core.name": "bucket"
                                }
                            }
                        ]
                    }
                ]
            }
        ]
    }
]
```
