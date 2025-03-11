Use the request body to upload the import file and specify the action that the request should take in case of errors or warnings.

Let us assume that you want to import the `MyCurations.xls` file containing bulk asset details. In the body of the request, specify the parameters in the following format:

```
file: MyCurations.xls

config: 
{
  "validationPolicy": "CONTINUE_ON_ERROR_WARNING"
}
```

The following table describes the parameters that you can specify in the body of the request:

| Parameter | Description |
|-----------|-------------|
| file | Specify the full path to the import file or upload the import file. This should be a Microsoft Excel file in the `.xlsx`, `.xlsm`, `.xlsb`, `.xls`, or `.csv` format. You can upload only one Microsoft Excel or CSV file in each request. |
| config | Specify one of the following validation policies to specify the action that the API request takes in case of errors and warning: |

- `STOP_ON_ERROR`. If the import file contains a row with errors, the process stops, and no data is imported. If there are no errors, the system imports valid data from the file, and warnings are marked as skipped.
- `STOP_ON_WARNING`. If the import file contains a row of data with warnings, the process stops, and no data is imported.
- `CONTINUE_ON_ERROR_WARNING`. All valid rows from the file are imported. Rows of data with warnings and errors are marked as skipped.

If you do not specify the validation policy, then the default value is `CONTINUE_ON_ERROR_WARNING`.
