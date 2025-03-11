Use the import API to import bulk assets into the catalog. You can import new business assets into the catalog, create, update or delete existing business assets in the catalog, or re-import curated technical assets that you previously exported from the catalog.

Send a POST request after uploading the import file in the body of the request. Send the request with the following method and endpoint:

| Method | Endpoint |
|--------|----------|
| POST | <baseApiUrl>/data360/content/import/v1/assets |

The base API URL differs for each pod. For more information, see Send Requests.

The following image shows the overall process of using the import API and the expected response for the endpoint:

![Image depicting the process for placing Import API requests and the responses that the endpoint returns.](../cloud-data-governance-and-catalog-api-reference/images/GUID-2F735AFB-64FC-4605-B83D-770B82D35FD8-low.png)
