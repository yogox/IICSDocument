### Import a bulk asset file in the catalog

The following example shows a POST request to import a bulk asset Microsoft Excel file named `MyCurations.xls`.The validation policy is set to import all valid rows from the file and skip rows with warnings and errors.

```
POST https://idmc-api.dm-us.informaticacloud.com/data360/content/import/v1/assets
Authorization: Bearer <jwt_token>
X-INFA-ORG-ID:<Org ID>

Body
--form 'file=@"/path/to/file"' \

--form 'config="{

  \"validationPolicy\": \"CONTINUE_ON_ERROR_WARNING\"

}";type=application/json'
```
