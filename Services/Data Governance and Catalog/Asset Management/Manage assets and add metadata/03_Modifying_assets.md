To modify an asset, you can modify the details of an asset, change its properties, add hierarchical assets, or assign new stakeholders.

If you want to modify business or technical assets, ensure that you meet the following prerequisites:

* The organization administrator must grant you the Update permission on the asset through access policies in Metadata Command Center.
* If there's a workflow configured for the asset, then the organization administrator must enable the Participate in Change Approvals privilege for your user role in Administrator. 
* To modify the stakeholders for assets, the organization administrator must grant you the Manage Access permission on the asset through access policies in Metadata Command Center.
* You cannot publish the draft version of an asset if there are inactive stakeholders associated with the asset. You must first delete the inactive stakeholders from the Stakeholders tab of an asset to start the workflow for the asset.

For more information about the available permissions and privileges for managing access to assets, see Manage access to assets.

Perform the following steps to modify an asset:

1. Open the asset that you want to modify. 
2. On the panel that you want to modify, click the Edit icon.
3. Modify the asset description or attributes, and click Save.

   If you are the stakeholder of the asset or if the organization administrator has configured a workflow for the asset, the Lifecycle status changes to Draft.

4. Click Submit to send the latest changes to the stakeholders defined in the workflow.

   ![Image depicting the Submit button on the asset page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ad-asset-management/images/GUID-CDB87594-BB9E-44F9-BF18-4C8EE5F00017-low.png)

**Note:** You can delete the modifications made to the asset if they're no longer needed by clicking the action menu on the asset page and selecting Delete Draft Version. You cannot delete the draft version of the asset in the following conditions:

- If the asset has incoming relationships with other assets.
- If the asset has outgoing parent-child relationships with other assets.
- If the asset has outgoing and indirect parent-child relationships with other assets.
- If the asset has tickets in the Open status.
