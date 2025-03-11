When you send a POST request to import bulk assets into the catalog, the API triggers a job to import the assets.

The following example shows the response of the POST request to import bulk assets from the file `MyCurations.xls`:

```
{
    "jobId": "6a084b71-3696-4a50-b83b-9ef0f2c7f30d",
    "jobUri": "/data360/observable/v1/jobs/6a084b71-3696-4a50-b83b-9ef0f2c7f30d"
}
```

The following table describes the response body parameters for the import API request:

| Parameter | Description |
|-----------|-------------|
| jobId | Unique ID of the import job that the request triggers. |
| jobUri | Job tracking URI that you can use to send a GET request to monitor the status of the import job. |

For more information about using the jobs API to monitor the status of jobs, see Monitor jobs.
