# View relationships in assets

The **Relationships** tab of an asset page displays the relationships between the selected asset and other business and technical assets in Data Governance and Catalog. For example, you can see how a data set links to other assets such as a system, column, process, or a policy.

On the **Relationships** tab of an asset page, you can view the relationships of the asset either in a grid or graphical format.

### Grid view

The grid view displays the asset relationships in a table where you can view how other assets are related to the selected asset. The following image shows the **Relationships** tab of a data set in the grid view.

![Image depicting the Relationships tab of an asset.](https://onlinehelp.informatica.com/iics/prod/dgc/en/aa-asset-discovery/images/GUID-1AE52426-0F92-492C-A936-37C85EBD69F3-low.png)

1. Grid view icon.
2. Count of the types of assets related to this asset.
3. Table containing the names of assets that are related to the open asset. The **How it is Related** column displays the type of relationship that each asset has with the open asset. To learn more about the different types of relationship types, see [Relationship types in assets](https://onlinehelp.informatica.com/iics/prod/dgc/en/aa-asset-discovery/Relationship_types_in_assets.html).

### Graph view

In the graph view, the source asset appears at the center of the view, and the related asset types appear around the source asset. You can expand each asset type to view the assets that are in a relationship with the source asset. The following image shows the **Relationships** tab of a data set in the Graph view.

![Image depicting an asset in graph view where you can see the seed asset at the center, surrounded by the related asset types.](https://onlinehelp.informatica.com/iics/prod/dgc/en/aa-asset-discovery/images/GUID-FAECBB98-CF21-4444-9A00-BF4063E987B2-low.png)

1. Source asset to which the other assets are related.
2. Asset types related to the source asset.
3. The expanded asset type node that shows all the assets of that type that are related to the source asset.
4. The tooltip for the asset in the expanded asset type node.

In the above example, the data set 'Customer Contact Details' is the source asset at the center. The related system asset type node is expanded and it shows two system assets related to the source data set. The hover tooltip for the 'Customer Master' system asset shows the details of the asset such as the asset name, type, lifecyle and hierarchy.

**Note:** The following guidelines apply for the graph view of an asset:

• By default, you can expand 20 assets and can go up to 100 assets with increments of 20 assets.
• If there are more than ten asset types related to the source asset, then the corresponding asset types are grouped under a single related asset type called **Others**.

## Additional navigation options for relationships

You can use the following controls on the **Relationships** tab to navigate the relationships and explore additional options:

### Relationships Options

The following image shows the available controls to view relationship options:

![Image depicting the available controls to view relationship options.](https://onlinehelp.informatica.com/iics/prod/dgc/en/aa-asset-discovery/images/GUID-1BE37D87-A5AC-4FA9-9282-6152B3018A45-low.png)

1. Add relationships
2. Filters
3. Find
4. Overlays
5. Action menu
6. Full Screen
7. Show Preview

### Add relationships

Click **Add relationships** in the graph view or grid view to add relationships for the asset. For more information about adding relationships to an asset, see [Creating relationships between assets](https://onlinehelp.informatica.com/iics/prod/dgc/en/aa-asset-discovery/Creating_relationships_between_assets.html).

### Filters

Click **Filters** in the graph view or grid view to filter the corresponding search results and to narrow down to an individual asset or categorize a group of assets.

![Image depicting the Filters dialog box.](https://onlinehelp.informatica.com/iics/prod/dgc/en/aa-asset-discovery/images/GUID-897300FC-3D24-46F4-8388-0C421E8984F0-low.png)

### Find

Use the **Find** option in the graph view or grid view to search any related asset by its name.

### Overlays

In the graph view, click **Overlays** and select one of the following options to add more information about the relationships to the graph:

• Relationship Labels. Adds information about the type of the relationship between the related assets.
• Stakeholders. Adds the name of the stakeholder of the related assets.

### Export

In the graph view, click the action menu to export a snapshot image of the related assets to your computer in `.PDF` or `.PNG` file format.

### Legend

In the graph view, click the Action menu to use the legend options to identify the assets and the directions of related assets with the seed asset.

![Image depicting the Legend dialog box.](https://onlinehelp.informatica.com/iics/prod/dgc/en/aa-asset-discovery/images/GUID-0BF4269E-A570-431E-8ED5-CAF2C8BBB017-low.png)

### Full screen

In the graph view, click **Full Screen** to display the graphical relationships view in full screen on your computer.

### Preview

Select an asset and click **Show Preview** in the graph view or grid view to view more details about the related asset.

© Copyright Informatica LLC 2021, 2025
