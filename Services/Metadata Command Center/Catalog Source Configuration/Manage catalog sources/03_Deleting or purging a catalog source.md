Delete or purge a catalog source based on your business requirements.

When you delete a catalog source, you delete all the configuration specific to that catalog source, along with all the metadata that was extracted and any enrichment made to the associated metadata. Purging a catalog source deletes all the metadata that was extracted, along with any enrichment made to the associated metadata.

**Note:** Before you delete or purge a catalog source, manually unassign the connections that are assigned to that catalog source.

1. Go to the Explore page in Metadata Command Center.
2. Select Catalog Sources from the menu.
3. From the list of catalog sources, search for the catalog source that you want to delete or purge. 
4. Click the Action menu, and select Delete or Purge.

![Image of the Action menu highlighting Delete and Purge for a catalog source on the Explore page](https://onlinehelp.informatica.com/IICS/prod/MCC/en/metadata-command-center-catalog-source-configuration/images/GUID-BBC4F7D9-A8BF-4403-A238-95DEC82B1F0F-low.gif)

**Note:** You can't delete or purge a catalog source if the catalog source job is in the running state.

5. To confirm delete or purge, click OK.

The catalog source is triggered to delete or purge. You can monitor the status of the job on the Monitor page.

**Note:** If the deletion job succeeds, the catalog source disappears from Metadata Command Center. If it fails, some associated objects might still be present in Data Governance and Catalog. Such catalog sources continue to appear in the list of catalog sources in Metadata Command Center, but are marked as Deleted. Delete the catalog sources to remove them along with any remaining objects present in Data Governance and Catalog.
