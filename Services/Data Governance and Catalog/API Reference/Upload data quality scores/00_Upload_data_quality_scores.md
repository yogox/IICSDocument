Upload one or more data quality scores to Data Governance and Catalog. When you upload a score, specify the data quality rule occurrence for which the scores apply. After you upload the scores, you can see the new scores in Data Governance and Catalog by opening the asset that is related to the rule occurrence you specified.

To upload one or more data quality scores, send the request with the following method and endpoint:

| Method | Endpoint |
|--------|----------|
| PATCH | ccgf-ruleautomation/api/v1/dataQuality/publishScore?refBy=INTERNAL |

**Note:** Depending on the base URL for each pod, prefix the base URL to the endpoint in the following format:

`<baseApiUrl>`<endpoint>

For example, `https://cdgc-api.dm-em.informaticacloud.com`/ccgf-ruleautomation/api/v1/dataQuality/publishScore?refBy=INTERNAL
