# Export assets using asset IDs

Send a POST request to search for assets in the catalog using asset IDs and export the assets in a Microsoft Excel or a CSV file. Specify the asset IDs in the request body and use the request parameters to specify the details of the assets that you want to export.

To search and export assets using asset IDs, submit a request with the following method and endpoint and specify the asset IDs in the request body:

| Method | Endpoint |
|--------|----------|
| POST | `<baseApiUrl>/data360/search/export/v1/assets/details` |

The base API URL differs for each pod. For more information, see [Send Requests](../cloud-data-governance-and-catalog-api-reference/Send_Requests.html). 

## Request parameters

To export specific details of the exported assets, use the request URL parameters and specify the details that you want to export.

You can use the following request URL parameters to specify the details of the assets that you want to export:

| Parameter | Description |
|-----------|-------------|
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
- `neighborhood`. Returns assets that are in a direct relationship with the searched asset.

The default value is `segments=all`. |
| `fileName` | Specify the name of the Microsoft Excel output file that you want to export. The file name should not contain spaces.Specify the file extension. The exported file will either be in the `.xlsx` or in the `.csv` format. |
| `summaryViews` | If you set this parameter, the exported Microsoft Excel file includes a summary sheet. Specify the type of assets you want to see in the summary sheet. You can specify one of the following values:
- `all`. The summary sheet in the exported file contains a summary of all the assets you have exported.
- `Technical`. The summary sheet in the exported file contains a summary of only the technical assets you have exported.
- `Business`. The summary sheet in the exported file contains a summary of only the business assets you have exported. |
| `scheme` | Specify the type of asset ID you want to use to query assets. Enter one of the following values:
- `internal`. Indicates that the asset ID that you specify in the request is the internal ID of the asset.
- `external`. Indicates that the asset ID that you specify in the request is the unique reference ID of the asset. |

## Request body

Use the request body to specify the external or internal IDs of assets you want to export. You can specify in the `scheme` parameter of the request URL whether you want to search the asset by external ID or internal ID.

In the body of the request, specify comma-separated asset IDs in the following format:

```
[
    "0c5777c2-ec04-4a57-8bf0-fc895c4579a2",
    "982cd858-b5b0-4cea-b120-cad3c325e38e",
    "e907f08f-6327-4214-9401-c794bc0c34db",
]
```

If you don't know the ID of a particular asset, you can first send a POST request to view the list of assets in the catalog. This request returns the internal ID of each asset in the `core.identity` parameter and the unique reference ID of the asset in the `core.externalId` parameter. For more information, see [List assets in the catalog](../cloud-data-governance-and-catalog-api-reference/List_assets_in_the_catalog.html).

## Example request

### Export technical assets along with the specified details

The following example shows the POST request to export the summary, data profile statistics, data classifications, and the associated glossary details of seven technical assets in a file named `Export_technical_assets`. The IDs of the technical assets are specified in the body of the request.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/search/export/v1/assets/details?segments=summary,dataProfile,dataClassification,glossary&fileName=Export_technical_assets&summaryViews=all&scheme=internal
Authorization: Bearer <jwt_token>
Content-Type: application/json
X-INFA-ORG-ID:<Org ID>

Body
[
    "0c5777c2-ec04-4a57-8bf0-fc895c4579a2",
    "982cd858-b5b0-4cea-b120-cad3c325e38e",
    "e907f08f-6327-4214-9401-c794bc0c34db",
    "a378e9fa-e4b1-427d-ae9b-978111d431dd",
    "7d01c99f-f57b-44f0-8dd9-ff3721f1eb93",
    "23fd6de2-b0aa-4c79-aa5f-c83205164fc1",
    "aaace41b-3dff-4a74-82f7-f4e7874dacb8"
]
```
