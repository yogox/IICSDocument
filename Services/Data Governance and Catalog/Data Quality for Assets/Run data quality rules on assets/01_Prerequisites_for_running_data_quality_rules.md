# Prerequisites for running data quality rules

According to the data quality application that you use, you must configure the system and the users so that the data quality rules can be run properly. Before running data quality rules, ensure to enable the Data Quality option in Metadata Command Center for each catalog source.

### Running data quality rules in Informatica Cloud Data Quality

If you want to define data quality rules in Data Governance and Catalog and run the rules in Informatica Cloud Data Quality, the following prerequisites apply:

* Data Governance and Catalog must be integrated with Informatica Cloud Data Quality.
* You must be able to access Informatica Cloud Data Quality using the same login credentials that you use for Data Governance and Catalog.
* To associate an existing rule in Data Quality with a Glossary asset in Data Governance and Catalog, you must have view permission for the rule specification in Data Quality.
* To create a rule in Data Quality and associate it with a Glossary asset in Data Governance and Catalog, you must have view and execute permissions for rules and profiles in Data Quality.

The organization administrator can assign you the required permissions and privileges in the Administrator service. For more information about assigning asset permissions and feature privileges to users, see the Citation Organization Administration help in the Administrator.

### Running data quality rules in another data quality application

If you want to define data quality rules in Data Governance and Catalog and run the rules in another data quality application, the following prerequisites apply:

* Data Governance and Catalog must be integrated with the data quality application.
* You must have appropriate permissions and privileges to view, create and execute rules and profiles in the data quality application.
