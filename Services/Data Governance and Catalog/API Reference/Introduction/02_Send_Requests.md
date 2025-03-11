# Send Requests

When you make an API call in the REST client, the request is sent in JSON format. Depending on the request, the REST client receives a response in JSON format that contains the information for the request that was sent.

To make an API call, enter the URL to access the API, header requests, methods, and request parameters.

### URL

Here's the URL structure for requests:

```
<baseApiUrl><endpoint>
```

The base API URL differs for each pod. The following table describes the base API URL to use for different regions:

| Region | Base API URL |
|--------|--------------|
| APJ | https://idmc-api.dm-ap.informaticacloud.com/ |
| Canada | https://idmc-api.dm-na.informaticacloud.com/ |
| EMEA | https://idmc-api.dm-em.informaticacloud.com/ |
| North America | https://idmc-api.dm-us.informaticacloud.com/ |
| United Kingdom | https://idmc-api.dm-uk.informaticacloud.com/ |

### Headers

The following table describes the header request that you should use to send the Data Governance and Catalog API requests:

| Header | Description |
|--------|-------------|
| Content-Type:application/json | This header is required for the POST method. It indicates that the client is sending a JSON request. |
| Authorization:Bearer <jwt_token> | This header is required to secure all your API requests. |
| X-INFA-ORG-ID:<Org ID> | This header is required for POST and GET methods. It indicates the user's organization to send API requests to.
The org ID is obtained from the Login API. |
| IDS-SESSION-ID | This header is required for sending API requests to upload your data quality scores to Data Governance and Catalog. |
