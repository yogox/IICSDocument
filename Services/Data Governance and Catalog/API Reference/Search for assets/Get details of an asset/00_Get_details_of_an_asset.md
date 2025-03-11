To retrieve complete details of a particular asset, send a GET request using the search API. Based on the request URL parameters that you pass, the response includes details such as profiling, classification, relationships, custom attributes, and lineage information of the specified asset. 

To get the details of an asset, submit a request with the following method and endpoint, and specify the asset ID: 

| Method | Endpoint |
| ------ | -------- |
| GET | &lt;baseApiUrl&gt;/data360/search/v1/assets/&lt;assetID&gt; |

The &lt;baseApiUrl&gt; differs for each pod. For more information about the base API URL, see Send Requests. 

The &lt;assetID&gt; that you enter can be the internal ID or the external ID of the asset. You can specify in the scheme parameter of the request URL whether you want to search the asset by external ID or internal ID. 

If you don't know the ID of a particular asset, you can first send a POST request using the &lt;baseApiUrl&gt;/data360/search/assets endpoint to view the list of assets in the catalog. The response for this request returns the internal ID of each asset in the core.identity parameter and the unique reference ID of the asset in the core.externalId parameter. For more information, see List assets in the catalog. 

Search for assets
Request parameters
Examples
Response body
