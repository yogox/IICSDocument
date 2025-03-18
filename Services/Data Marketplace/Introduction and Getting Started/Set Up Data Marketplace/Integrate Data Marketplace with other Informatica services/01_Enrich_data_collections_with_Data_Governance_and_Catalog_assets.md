To make business decisions, a user in your organization may seek a specific data. If the data is maintained in Data Governance and Catalog and well-governed, you can make the data available to the user via Data Marketplace. To achieve this, you can quickly load assets that are governed in Data Governance and Catalog into Data Marketplace.

On the Integration tab on the Setup page, you can connect Data Marketplace to Data Governance and Catalog.

To perform this task, verify the following prerequisites:

* Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
* Your user profile is assigned a role for which the View Set up page and Configure and Manage Data Marketplace privileges are enabled in Administrator.

The following image shows the Integration tab:

![Image depicting the Integration tab on the Setup page.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/cc-setup-data-marketplace/images/GUID-FE4D4A27-C6F5-4AEF-869D-9B90C4086824-low.png)

To connect to Data Governance and Catalog, set the Status toggle on the Integration Sources grid to Active.

After you connect Data Marketplace to Data Governance and Catalog, the Data Governance and Catalog Asset Types grid appears. On this grid, you can select the types of assets that you want to add to Data Marketplace. To perform this task, set the Status toggle for an asset type to Active. To ensure that assets from Data Governance and Catalog appear properly, consider using only the asset types that are labelled as Recommended. You can also use asset types that are labelled as Available. However, Data Marketplace may not display them correctly.

When you enable an integration source, the assets available in it can be used by stakeholders to enrich their data collections. For more information about how a stakeholder adds an asset to a data collection, see the Adding data assets to a data collection topic in the Working With Data Collections help.

When a stakeholder adds a Data Governance and Catalog asset to a data collection, the Overview page of the asset in Data Governance and Catalog indicates that the asset is published to Data Marketplace. Additionally, you can view in Data Governance and Catalog the details of the data collection to which the asset was added.

For more information about the assets that are imported from Data Governance and Catalog into Data Marketplace, see the Data assets topic in the Introduction and Getting Started help.
