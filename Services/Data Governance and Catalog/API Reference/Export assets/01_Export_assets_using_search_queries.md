# Export assets using search queries

Send a POST request to search for assets in the catalog using search queries and export the assets to a Microsoft Excel or a CSV file. Use the request URL parameters and the request body to enter your search queries and specify the details of the assets you want to export.

To search and export assets using search queries, submit a request with the following method and endpoint:

| Method | Endpoint |
|--------|----------|
| POST | `<baseApiUrl>/data360/search/export/v1/assets` |

The base API URL differs for each pod. For more information, see Send Requests. 

## Request parameters

To limit the scope of the exported assets, enter search queries using the request URL parameters and filter the search results.

You can use the following request URL parameters to filter and limit your search results before you export the assets:

| Parameter | Description |
|-----------|-------------|
| `knowledgeQuery` | Specify the asset type or name along with any search criteria. For information about search query examples, see Search query examples.
For example, you can enter `knowledgeQuery=Business Terms` and `knowledgeQuery=data elements related to business term`. |
| `segments` | Specify the level of asset detail that you want the API request to return. Enter any segment value from the following values:
- `all`. Returns the summary, system attributes, and the API request link to view further details of the asset.
- `summary`. Returns the name, description, and location of the asset.
- `systemAttributes`. Returns the origin, class type of the asset, base types, user that created or updated the asset, and the date on which the asset was created or updated.
- `customAttributes`. Returns the custom fields specified for the asset.
- `selfAttributes`. Returns the properties of assets.
- `stakeholdership`. Returns the type of user and role that are assigned as stakeholder for the asset.
- `dataProfile`. Returns the profiling statistics of the asset.
- `dataClassification`. Returns the data classification associated with the asset.
- `glossary`. Returns the glossary associated with the asset.
- `dataQuality`. Returns the data quality score of the asset.
- `hierarchy`. Returns the hierarchy of the asset.
The default value is `segments=all`. |
| `fileName` | Specify the name of the Microsoft Excel output file that you want to export. The file name should not contain spaces. |
| `summaryViews` | If you set this parameter, the exported Microsoft Excel file includes a summary sheet. Specify the type of assets you want to see in the summary sheet. You can specify one of the following values:
- `all`. The summary sheet in the exported file contains a summary of all the assets you have exported.
- `Technical`. The summary sheet in the exported file contains a summary of only the technical assets you have exported.
- `Business`. The summary sheet in the exported file contains a summary of only the business assets you have exported. |

## Request body

Use the request body to specify the pagination parameters. The API response exports the specified number of assets that match the search criteria.

In the body of the request, specify the pagination parameters in the following format:

```
{
    "from": 0,       
    "size": 10,       
}
```

The following list describes the pagination parameters that you can use to specify the number of assets that you want to export:

• `from`. Specify a numeric value to set an offset for pagination. The default value is zero.
• `size`. Specify a numeric value for the number of assets that you want to export. The default value is 10.

Consider the following scenarios when you specify the number of assets to export using this API:

• To export more than 10000 assets that match the search criteria, remove the `from` parameter and specify the number of assets to export in the `size` parameter of the request body. If `size` is set to more than 10000 assets, then the exported file is in the ZIP format containing multiple files. Each file is limited to 10K rows.
• To export all assets that match the search criteria, remove the `from` parameter and specify zero as the value of the `size` parameter in the request body.

## Example requests

### Export more than 10000 assets

The following example shows the POST request to export and download 15000 assets that start with the name 'Customer'. The summary sheet in the exported file will contain a summary of the assets.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/export/v1/assets?knowledgeQuery=Customer*&fileName=Export__all_assetse&summaryViews=all

Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
{
    "size": 15000
}
```

### Export all assets in the catalog

The following example shows the POST request to export and download all assets in the catalog. The summary sheet in the exported file will contain a summary of the assets.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/export/v1/assets?knowledgeQuery=all&fileName=Export__all_assetse&summaryViews=all

Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
{
    "size": 0
}
```

### Export all details of all business assets

The following example shows the POST request to export all details of business assets in the catalog and downloads 500 assets based on the `size` body parameter. The summary sheet in the exported file will contain a summary of the assets.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/export/v1/assets?knowledgeQuery=Business Assets&segments=all&fileName=Export_32_all_segment_all_view&summaryViews=all

Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
{
    "from": 0,
    "size": 500
}
```

### Export the summary and custom attributes of all business assets

The following example shows the POST request to export the summary and custom attributes of business assets in the catalog and downloads 10 business assets based on the `size` body parameter. The summary sheet in the exported file will contain a summary of the business assets.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/export/v1/assets?knowledgeQuery=Business Assets&segments=summary,customAttributes&fileName=Export_32_all_segment_all_view&summaryViews=Business

Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
{
    "from": 0,
    "size": 10
}
```
