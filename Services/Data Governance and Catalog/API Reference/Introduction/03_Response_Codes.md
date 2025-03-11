When you call any of the Data Governance and Catalog APIs, the response returns one of the standard HTTP response codes with information about the success or failure of the API call.

The standard response codes are defined in the following table:

| Response Code | Description |
|--------------|-------------|
| 200 OK | The request was completed successfully. |
| 201 Created | The request was completed and the new resource is created successfully. |
| 202 Accepted | The request was accepted for processing, but has not been completed. |
| 204 | No content to send back. |
| 400 Bad Request | The request could not be processed because it contains missing or invalid information. |
| 401 Unauthorized | The request is not authorized. The authentication may be missing or invalid. |
| 403 Forbidden | The user cannot be authorized to perform this request. |
| 404 Not Found | The request includes a resource URL that does not exist. |
| 405 Method Not Allowed | The HTTP method specified in the request is not supported for this request. |
| 429 Too Many Requests | The user has sent too many requests in a given amount of time and has reached the API rate limit. |
| 500 Internal Server Error | The server encountered an error because of which the request is not fulfilled. |
