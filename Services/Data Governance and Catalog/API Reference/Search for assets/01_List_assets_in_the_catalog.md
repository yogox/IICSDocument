# List assets in the catalog

Send a POST request to view the list of assets in the catalog that match your search query. While sending the request, you can specify the search query as request URL parameters and specify the filter criteria in the body of the request.

To view the list of assets in the catalog, submit a request with the following method and endpoint:

| Method | Endpoint |
|--------|----------|
| POST | `<baseApiUrl>/data360/search/v1/assets` |

The base API URL differs for each pod. For more information, see [Send Requests](../cloud-data-governance-and-catalog-api-reference/Send_Requests.html).

## Request parameters

To view the list of specific assets, enter the search queries using URL parameters for POST request.

You can use the following request URL parameters to specify your search query:

| Parameter | Description |
|-----------|-------------|
| `knowledgeQuery` | Specify the asset type or name along with any search criteria. For information about search query examples, see [Search query examples](../cloud-data-governance-and-catalog-api-reference/Search_query_examples.html). For example, `knowledgeQuery=Business Terms` and `knowledgeQuery=data elements related to business term`. |
| `segments` | Specify the level of asset detail that you want the API request to return. Enter any segment value from the following values: - `all`. Returns the summary, system attributes, and the API request link to view further details of the asset. - `summary`. Returns the name, description, and location of the asset. - `systemAttributes`. Returns the origin, class type of the asset, base types, user that created or updated the asset, and the date on which the asset was created or updated. - `customAttributes`. Returns the custom fields specified for the asset. - `selfAttributes`. Returns the properties of assets. - `details`. Returns the URI for the asset that you can click to send a request to view further details of a specific asset. The default value is `segments=all`. |

## Request body

Use the request body to specify parameters to filter, rank, and sort your search results. The API response returns a maximum of 100 results that match the specified criteria.

In the body of the request, specify the parameters in the following format:

```
{
    "from": 0,       
    "size": 10,       
    "searchFields": [     
        "string"
    ],
    "filterSpec": [    
        {
            "type": "dsl",
            "attribute": "string",
            "values": [
                "string"
            ],
            "expr": "string"
        }
    ],
   "rankingSpec":
    { "boostSpec": [       
            {
                "fields": [
                    "string"
                ]
            }
        ],
      "scoringSpec": [{
            "type": "simple",
            "attribute": "core.identity",
            "order":"asc"
        },
        {
            "type": "simple",
            "attribute": "core.name",
            "order":"asc"
         }]
    }
    ,
   "after":["03c1883a-dcb7-4ae0-a6a5-c2743e52fb69",
                "column67"]
}
```

The following table describes the important parameters that you can specify in the body of the request:

| Parameter | Type | Description |
|-----------|------|-------------|
| pagination parameters `from` and `size` | Numeric | Use the following parameters to retrieve records using pagination: - `from`. Specify a numeric value to set an offset for pagination. The default value is zero. - `size`. Specify a numeric value to set the maximum number of results to display on each page starting from the offset value. The default value is 10. You can set a maximum page size of 100 results. The following examples show how you can use the `from` and `size` parameters: ```{    "from": 0,    "size": 50}``` Retrieves 50 records per page starting from the first record, assuming that the total_hits is more than 50 records. ```{    "from": 50,    "size": 50}``` Retrieves 50 records per page starting from the 50th record, assuming that the total_hits is more than 50 records. |
| `searchFields` | String | Specify the asset fields that you want to search. For example, you can search for assets whose name and description fields match the term `SSN`. This does not influence the ordering of the search results. |
| `filterSpec` | String | Specify a list of fields and values that you want the API to use to filter search results. You can use any of the following filter type or a combination of both filter types: **Simple**. Specify the asset attribute and one or more values to match the assets. For example, the following `filterSpec` parameter returns the assets that are in the 'Published' lifecycle status: ```{    "from": 0,    "size": 100,    "filterSpec": [        {            "type": "simple",            "attribute": "core.assetLifecycle",            "values": [                "Published"            ]        }    ]}``` **dsl**. Specify an advanced filter expression to match the assets. For example, the following `filterSpec` parameter returns business terms that are created in the last one hour: ```{  "from": 0,  "size": 100,  "filterSpec": [    {      "type": "dsl",      "expr": "core.classType core.infa.ccfg.models.governance.BusinessTerm and core.createdOn within last 1 hour"    }  ]}``` |
| `rankingSpec` | NA | Determines the order in which the assets appear in the search response. You can order the assets by specifying the asset scoring or boosting criteria or both. |
| `boostSpec` | String | Specify one or more fields by which you want to sort the search results. If you specify multiple fields, all specified fields are treated equally for sorting. For example, the following `boostSpec` parameter first returns assets whose names match the search criteria, followed by the assets whose descriptions match the criteria. ```{    "explain": false,    "from": 0,    "size": 100,    "rankingSpec": {        "boostSpec": [            {                "fields": [                    "core.name"                ]            },            {                "fields": [                    "core.description"                ]            }        ]    }}``` |
| `scoringSpec` | String | Specify one of the following two types of scoring criteria: **Simple**. Specify the sorting order (ascending or descending) on attributes such as name or identity. For example, the following `scoringSpec` parameter returns business terms that are sorted in the descending order of their names. ```{    "from": 0,    "size": 100,    "rankingSpec": {        "scoringSpec": [            {                "type": "simple",                "attribute": "core.name",                "order": "desc"            }        ]    },    "filterSpec": [        {            "type": "dsl",            "expr": "core.classType com.infa.ccgf.models.governance.BusinessTerm"        }    ]}``` **dsl**. Specify an advanced filter criteria in an expression to sort the search results. For example, the following `scoringSpec` parameter returns the list of business term assets sorted by assets that have an average rating greater than one. ```{    "from": 0,    "size": 100,    "rankingSpec": {        "scoringSpec": [            {                "type": "dsl",                "expr": "core.supplement.averageRating greater than 1"            }        ]    },    "filterSpec": [        {            "type": "dsl",            "expr": "core.classType com.infa.ccgf.models.governance.BusinessTerm"        }    ]}``` |
| `after` | Object | Enter the value from the `SortValues` field of an asset that the API response returns. When you run the API request with this value, the response returns the next set of specified assets after the asset that you have specified the value for. |

### Search for more than 10000 assets

To search more than 10000 assets, set the `scoringSpec` type in the `rankingSpec` parameter to **Simple**. Among the attributes that you specify for the sorting order, specify at least one attribute that has unique values. For example, you can sort the order on the `core.identity` attribute, which is the internal ID of the asset.

You can retrieve a maximum of 100 assets with each API request. To see the next 100 assets, copy the value from the `SortValues` field of the last asset that the response returns and enter it in the `after` field of the request body before you send the request again.

## Example requests

### List the next set of results from the catalog

The following request returns the first 50 assets sorted in the ascending order of their internal IDs.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=*&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
{
    "from": 0,
    "size": 50,
    "rankingSpec": {
        "scoringSpec": [
            {
                "type": "simple",
                "attribute": "core.identity",
                "order": "asc"
            }
        ]
    }
}
```

To see the next 50 assets and so on, copy the value from the `SortValues` parameter of the 50th asset that the response returns and enter it in the `after` parameter of the request body as shown in the following example.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=*&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
{
    "size": 50,
    "rankingSpec": {
        "scoringSpec": [
            {
                "type": "simple",
                "attribute": "core.identity",
                "order": "asc"
            }
        ]
    },
    "after" : ["<The value from the sortValues field of the 50th asset>"]
}
```

To continue retrieving more assets from the catalog, replace the value of the `after` parameter in the request body during each API request.

### List business terms

The following request returns up to 100 business terms based on the `size` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=*&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
{
    "from": 0,
    "size": 100,
    "filterSpec": [
        {
            "type": "simple",
            "attribute": "core.classType",
            "values": [
                "com.infa.ccgf.models.governance.BusinessTerm"
            ]
        }
    ]
}
```

### List business terms in the 'Draft' lifecycle status

The following request returns business terms that are in the 'Draft' lifecycle status. The response displays up to 100 business terms based on the `size` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=*&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
    "from": 0,
    "size": 100,
    "filterSpec": [
        {
            "type": "simple",
            "attribute": "core.classType",
            "values": [
                "com.infa.ccgf.models.governance.BusinessTerm"
            ]
        },
        {
            "type": "simple",
            "attribute": "core.assetLifecycle",
            "values": [
                "Draft"
            ]
        }
    ]
}
```

### List business terms created in the last 30 days

The following request returns business terms created in the last 30 days based on the `filterSpec` body parameter. The response displays up to 50 business terms based on the `size` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=*&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
    "from": 0,
    "size": 50,
    "filterSpec": [
        {
            "type": "dsl",
            "expr": "core.classType com.infa.ccgf.models.governance.BusinessTerm and core.createdOn within last 30 day"
        }
    ]
}
```

### List data elements related to business terms

The following request returns data elements that are related to business terms based on the `knowledgeQuery` parameter. The response displays up to 50 data elements based on the `size` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=data elements related to business term&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
    "from": 0,
    "size": 50
}
```

### List assets related to the business term 'email'

The following request returns up to 100 assets related to the business term 'email' based on the `knowledgeQuery` URL parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=all related to business term email&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
    "from": 0,
    "size": 100
}
```

### List the tables that are profiled

The following request returns up to 50 tables that are profiled based on the `knowledgeQuery` URL parameter. The list of tables appear in the order of the average rating as specified in the `scoringSpec` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=tables which are profiled&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
    "from": 0,
    "size": 50,
    "rankingSpec": {
        "scoringSpec": [
            {
                "type": "simple",
                "attribute": "core.supplement.averageRating",
                "values": [
                    "5"
                ]
            }
        ]
    }
}
```

### List data elements related to business terms that are critical data elements

The following request returns up to 50 data elements that are marked as critical data element and related to the business terms 'Country' and 'First Name' as specified in the `filterSpec` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=data elements related to business term which are critical data element&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
  "from": 0,
  "size": 50,
  "filterSpec": [
    {
      "type": "simple",
      "attribute": "core.name",
      "values": [
        "Country", "FirstName"
      ]
    }
  ]
}
```

### List the system assets

The following request returns the system assets with the names 'Consumer Website' and 'Snowflake Product' as specified in the `filterSpec` body parameter. The response displays up to 100 system assets based on the `size` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=system&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
    "from": 0,
    "size": 100,
    "filterSpec": [
        {
            "type": "simple",
            "attribute": "core.name",
            "values": [
                "Consumer Website",
                "Snowflake Product"
            ]
        }
    ]
}
```

### List data classifications

The following request returns up to 100 data classifications as specified in the `size` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=classification&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
    "from": 0,
    "size": 100
}
```

### List data entity classifications

The following request returns data entity classifications as specified in the `filterSpec` body parameter. The response returns up to 50 classifications as specified in the `size` body parameter.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/v1/assets?knowledgeQuery=classification&segments=all
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID: <Org ID>

Body
{
  "from": 0,
  "size": 50,
  "filterSpec": [
    {
      "type": "dsl",
      "expr": "core.classType core.DataEntityClassification"
    }
  ]
}
```

## Response body

The POST request response returns the list of assets that match the search criteria.

The response displays the `total_hits` parameter that shows the total number of assets that match the search criteria. The response returns 100 assets per page.

The following table describes the possible response body parameters for each asset in the response body:

| Parameter | Description |
|-----------|-------------|
| `identity` | The internal ID of the asset. You can derive this ID by looking at the URL of the asset page in the Data Governance and Catalog application. |
| `externalID` | The unique reference ID of the asset. |
| `summary` | Contains the name, description, and location of the asset in the catalog. |
| `systemAttributes` | Contains the following meta parameters: - `modifiedOn`. The date on which the asset was last modified - `createdBy`. The user who created the asset. - `modifiedBy`. The user who last modified the asset. - `classType`. The type of asset. - `origin`. The origin of the assets in the catalog. - `createdOn`. The date on which the asset was created. |
| `customAttributes` | Contains the user-configured attributes of the asset. |
| `selfAttributes` | Contains different types of details depending on whether the asset is a business asset or a technical asset. Details include the lifecycle status, profiling and classification status, rating, information about whether the asset is a certified asset or a critical data element, and so on. |
| `details` | Contains the URI for the particular asset. Click the URI to send a request to view complete details of that asset. |
| `sortValues` | Contains a value to indicate the position of the asset in the response body. Enter this value in the `after` field of the request body to return the next set of specified assets after this asset. |

### Example response

The following example is an excerpt from a POST request to view business terms in the 'Draft' lifecycle status.

```
{
    "summary": {
        "total_hits": "1038"
    },
    "hits": [
        {
            "core.identity": "2f8e6839-14fe-4b25-a868-a6324be30164",
            "core.externalId": "BT-06092022-24",
            "summary": {
                "core.location": "CDGC://2f8e6839-14fe-4b25-a868-a6324be30164",
                "core.name": "BT-06092022-24",
                "core.description": " Desc Create using admin user from group and \nDeleteed stakeholder user."
            },
            "systemAttributes": {
                "core.modifiedOn": 1689252674028,
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
                "core.createdOn": 1689252674028
            },
            "customAttributes": {
                "com.infa.odin.models.custom.ca_2205258177888237465": "default",
                "com.infa.odin.models.custom.ca_5534006856514172118": "default"
            },
            "selfAttributes": {
                "com.infa.ccgf.models.governance.FormatType": "Text",
                "core.mergedObjects": [],
                "com.infa.ccgf.models.governance.BusinessLogic": "BusinessLogic",
                "com.infa.ccgf.models.governance.isCDE": true,
                "core.supplement.certified": [
                    false
                ],
                "core.assetLifecycle": "Draft",
                "com.infa.ccgf.models.governance.Examples": [
                    "Example-1",
                    "Exampl25"
                ],
                "com.infa.ccgf.models.governance.securityClassification": "Confidential",
                "com.infa.ccgf.models.governance.AliasNames": [
                    "BT",
                    "BTObject"
                ],
                "core.producer": "CDGC",
                "com.infa.ccgf.models.governance.FormatDescription": "Format Description"
            },
            "details": "/data360/search/assets/BT-06092022-24?scheme=external&segments=summary,systemAttributes,customAttributes,selfAttributes"
            "sortValues":[
                "03c1ea71-cac8-4e39-9f4a-6774c657a8cf",
                "idsltc"
            ]
        }
    ]
}
```
