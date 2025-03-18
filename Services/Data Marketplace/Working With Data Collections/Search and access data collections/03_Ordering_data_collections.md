After you find a data collection that meets your requirements, you can place an order to gain access to the data collection.

To order a data collection, verify one of the following prerequisites:

• Your user profile is assigned at least one of the predefined roles for Data Marketplace. For more information about the predefined roles for Data Marketplace, see the Predefined roles topic in the Introduction and Getting Started help.
• Your user profile is assigned a role for which the following privileges and permissions are enabled:
  - Access Data Marketplace privilege is enabled in Administrator.
  - Create and Read permissions are enabled in Metadata Command Center for orders.
  - Read permission is enabled in Metadata Command Center for cost centers, data collections, delivery targets, terms of use and usage contexts.

The following image shows the overall process of ordering a data collection in Data Marketplace:

![Image depicting the overall process of ordering a data collection in Data Marketplace.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/images/GUID-4A7EF824-6188-4BE6-91A3-DDABFD790A72-low.png)

**Note:** The process flow is illustrated using the predefined roles for Data Marketplace.

1. **Open a data collection.**

   For more information about how you can find a data collection, see [Browsing for data collections](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Browsing_for_data_collections.html).

2. **On the data collection page, click the Checkout button in the Order section.**

   **Note:** You can't order data collections that belong to an inactive category.

   If you can't find a data collection that meets your requirements, you can request for the creation of a new collection. For more information about how you can submit a request for a new data collection, see [Requesting new data collections](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Requesting_new_data_collections.html).

3. **On the Request Details page, enter the order details.**

   The following table describes the fields that you can configure on the Request Details page:

   | Field | Description |
   |-------|-------------|
   | Usage Context | Select the option that accurately describes how you intend to use the data after you receive access to the collection.<br><br>If none of the listed options accurately describe how you intend to use the data, select the option that bears the most resemblance to your usage. |
   | Business Justification | Enter a brief description how you intend to use the data after you receive access to the collection.<br><br>A stakeholder of the data collection reads this description to decide whether the order for this the data assets is valid. |
   | Delivery Target | Select a delivery target for the data collection.<br><br>If a default delivery target is configured for the data collection, that delivery target is selected by default.<br><br>If no delivery targets are configured for the data collection, the default delivery template that is configured for Data Marketplace is selected by default.<br><br>If no delivery targets are configured for the data collection and if a default delivery template isn't configured for Data Marketplace, you won't see this field. In such a scenario, a stakeholder of the data collection creates a new delivery target when they fulfill your order.<br><br>If you select a delivery target for which the Managed Access option is enabled, a stakeholder may be more likely to approve your order. With Managed Access, the data will be delivered in a location that is accessible only to you. Additionally, the delivered data may get customized based on the characteristics of the data and the usage context that you specify in the Usage Context field. For more information, see the Manage access to data with Data Access Management topic in the Set Up Data Marketplace help. |
   | Delivery Requests | Enter any additional information that pertains to your request. For example, you can specify the urgency or the preferred delivery method in this field. |
   | Cost Center | Select your cost center.<br><br>If you are not aware of your cost center or if the listed options don't list your cost center, you can enter your cost center. A stakeholder of the data collection can select an alternate cost center value when they approve or fulfill the orders. |

   You can also reuse the information from your previous order. To do this, click Reuse Last Details. If your previous order was for a different data collection, only the Business Justification and Delivery Request fields are automatically populated. If you order the same data collection that you previously ordered, all the fields are automatically populated.

   ![Image depicting the Request Details page of the Order Checkout wizard.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/images/GUID-269C3F68-4FC8-4B77-AEA3-36D877F42642-low.png)

4. **Click Next.**

5. **On the Usage Guide page, review the terms of use.**

   ![Image depicting the Usage Guide page of the Order Checkout wizard.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/images/GUID-605AE163-9F09-4589-85B1-B0FFAAD2D82B-low.png)

6. **Click Submit Order.**

7. **On the Order Placed page, you can view the details of the order that you placed.**

   ![Image depicting the Order Placed page of the Order Checkout wizard.](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/images/GUID-B1559AAA-EB80-4309-80FE-F192D133D1E6-low.png)

   If you want to navigate to the order page, click View Order. On the order page, you can view the timeline, summary, and delivery details of the data collection for which you have requested access.

After you place an order, the stakeholders of the data collection receive a notification in Data Marketplace about the order that you submitted. For more information about how a stakeholder responds to an order, see [Responding to orders](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Orders.html#ww3_12_6_12_1).

If your order is fulfilled, you can navigate to the consumer access page by clicking the consumer access link on the order page. For more information about consumer access, see [Consumer accesses](https://onlinehelp.informatica.com/IICS/prod/DMP/en/bb-working-with-data-collections/Consumer_accesses.html).
