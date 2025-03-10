If a business asset is no longer relevant, you can delete the asset.

To delete assets in Data Governance and Catalog, ensure that you meet the following prerequisites:

* Your organization administrator must grant you the **Delete** permission on the asset through access policies in Metadata Command Center.
* If the organization administrator enables the **Force Delete** privilege for your user role in Administrator, you can delete assets along with all its inbound relationships and the child assets involved in the hierarchy.

For example, let us consider a scenario where a domain asset called 'Finance' is the parent of the subdomain asset 'Retail Finance', and the subdomain asset 'Retail Finance' is the parent asset of the business term asset 'Org Finance'. If a user with the **Force Delete** privilege deletes the 'Retail Finance' subdomain, all the parent-child relationships are deleted and the child business term asset 'Org Finance' is also deleted.

* You cannot delete an asset that has inbound or outbound parent-child relationships with other assets. This is because the other assets are directly dependent on this asset. However, if there is a business asset that has data quality scores, you can delete the asset if it has an outbound parent-child relationship with another asset. To see if the asset is involved in any inbound or outbound relationship, see the Relationships tab on the asset page.
* You cannot delete any asset that has an associated workflow ticket in the **Open** status. If you delete an asset that has associated workflow tickets in the **Closed** status, the asset is deleted along with the closed workflow tickets.

You can delete business assets from Data Governance and Catalog if the asset that you are trying to delete or its child assets do not have open tickets associated with them.

To delete an asset that you no longer need, perform the following steps:

1. Open the business asset that you want to delete.
2. From the Action menu on the top right corner of the page, select **Delete Asset**.

The following image shows the Action menu on a sample Metric asset page:

![Image depicting the asset page with Delete Asset selected.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ad-asset-management/images/GUID-39412993-FEE4-4219-A606-B2CD4A00713F-low.png)

3. A delete warning appears. If there are any tickets in the **Open** status associated with the asset or its child assets, ensure that the tickets are in the **Closed** status in order to delete the asset. Click **Delete** to confirm.
