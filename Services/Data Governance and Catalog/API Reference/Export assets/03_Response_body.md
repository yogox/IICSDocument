When you send a POST request to export bulk assets from the catalog, the API triggers a job to export the assets.

The following example shows the response of the POST request to export bulk assets from the catalog:

```
{
    "jobId": "6a5b273a-f816-4346-a8ae-f2d27f3e3240",
    "trackingURI": "/data360/observable/v1/jobs/6a5b273a-f816-4346-a8ae-f2d27f3e3240?expandChildren=OUTPUT-PROPERTIES",
    "outputURI": "/data360/observable/v1/jobs/6a5b273a-f816-4346-a8ae-f2d27f3e3240/outputProperties/files/Export_File"
}
```

The following table describes the response body parameters for the export API request:

| Parameter | Description |
|-----------|-------------|
| jobId | Unique ID of the export job that the request triggers. |
| trackingURI | Job tracking URI that you can use to send a GET request to monitor the status of the export job. |
| outputURI | Output file URI that you can use to send a GET request to download the exported file. |

For more information about using the jobs API to monitor the status of jobs, see Monitor jobs. Once the job completes, you can send a GET request to download the exported file using the outputURI. The exported file is a Microsoft Excel file in the `.xslx` format.
