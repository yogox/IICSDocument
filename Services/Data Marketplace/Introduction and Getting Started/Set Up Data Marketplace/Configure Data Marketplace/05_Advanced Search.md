# Advanced Search

Advanced search allows you to search for data without needing to know in advance whether the data is represented in Data Marketplace as a data element, data asset or data collection.

The following image shows the Advanced Search panel on the Configuration tab of the Setup page:

![Image depicting the Configuration tab on the Search page. Advanced search is enabled.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/cc-setup-data-marketplace/images/GUID-ED308A27-7B34-47DB-882E-563E17779A43-low.png)

## Advantages of enabling advanced search

If you enable the Advanced Search option, Data Marketplace runs your search query on the following items when you search for data collections:

- Name and description of a data element that is associated with a data collection.
- Name and description of a data asset that is associated with a data collection.
- Name and description of a data collection.

If you have integrated Data Marketplace with Data Governance and Catalog, your search query is also run on the names and descriptions of Data Governance and Catalog assets and elements that are associated with a data collection.

By default, advanced search is enabled. If you disable it, Data Marketplace runs your search query on only the names and descriptions of data collections.

For more information about how you can search for data collections, see the Searching for data collections topic in the Working With Data Collections help.

## Configure advanced search

To configure advanced search, verify the following prerequisites:

- Your user profile is assigned one of the following roles:
  - Technical Administrator
  - Data Marketplace Administrator
- Your user profile is assigned a role for which the View Set up page and Configure and Manage Data Marketplace privileges are enabled in Administrator.

In the Advanced Search section on the Setup > Configuration tab, enable the Advanced Search option.
