# Manage access to data with Data Access Management

You can leverage data access policies that you define in Data Access Management to streamline the data delivery experience in Data Marketplace.

The following image shows the overall process of ordering a data collection using a Managed Access enabled delivery target:

![Image depicting the overall process of ordering a data collection using a Managed Access enabled delivery target.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/cc-setup-data-marketplace/images/GUID-5F62F2B2-3F20-405B-BADD-D14E9FEA4F5F-low.png)

1. a. In Data Marketplace, the Data User searches for a data collection that meets their requirements. After the Data User finds the relevant data collection, they place an order to gain access to the data.
   b. In Data Access Management, the Data Access Owner creates data access policies based on the guidelines of the organization.
2. The Data Marketplace Data Owner reviews the order and approves it.
3. After the order is approved in Data Marketplace, the Technical Owner fulfills the order using a delivery target for which the Managed Access option is enabled.
4. Data Marketplace generates a URL using the location details specified in the delivery target used to fulfill the order.
   - Data User accesses the data using the location URL.
   - In Data Access Management, the system applies the data access policies to customize the data that the Data User tries to access.

**Note:** The process flow is illustrated using the predefined roles for Data Marketplace.

When you create a delivery template in Data Marketplace, you can use the Managed Access option to create a location that is unique to each order that is fulfilled using a target that is based on the template. For more information about how you can create a new delivery template, see [Creating delivery templates](../cc-setup-data-marketplace/Delivery_options.html#ww3_9_15_14_1).

Data Access Management customizes the delivered data based on the data access policies that are defined in your organization. For this reason, a stakeholder of a data collection may be more likely to approve an order if a Data User has selected a delivery target for which the Managed Access option is enabled.

If a data collection has a delivery target for which the Managed Access option is enabled, Data Marketplace displays an icon for the data collection. This icon allows users to easily identify collections that can be ordered using a Managed Access enabled delivery option.

For more information about how a Data User orders a data collection and how a stakeholder approves an order, see the Working With Data Collections help. For more information about how the data is customized, see the Data Access Management help.

### Example 1. Example

In a cosmetics company, Alex and Arthur are analysts in the marketing team. They are responsible for compiling reports about demand trends across all the regions in which the company operates. Arthur is responsible for compiling the report for the European region and Alex is responsible for the North American region.

Sam is a data steward in the sales team. He manages the SQL database that contains all the sales data, including customer details, units sold, profit margin, and so on. As a Data Owner, he also publishes the data to the "Sales Data" data collection within the "Sales" category in Data Marketplace.

Jill works in the sales department with Sam. She is the Technical Owner of the "Sales Data" data collection. She uses a Managed Access enabled delivery template to create the delivery target of the "Sales Data" data collection. She is also a Data Access Owner for Data Access Management. In Data Access Management, Jill has defined data access policies in accordance with those of the company.

To compile the reports for latest financial year, Alex and Arthur order the "Sales Data" data collection. At the time of order, Arthur specifies the usage context as "Analytics - EU" and Alex specifies the usage context as "Analytics - NA". Sam reviews and approves their orders. After the order is reviewed, Jill fulfills the orders in Data Marketplace.

After their orders are fulfilled, Alex and Arthur receive access links to the data. Both their access links are unique. Despite ordering the same data collection, Alex is granted access to only the sales data for the North American region and Arthur is granted access to only the sales data for the European region. Furthermore, to comply with the data protection policies, the personal information of customers that Arthur receives is obfuscated.

**Note:** The preceding example uses the predefined roles for Data Marketplace.
