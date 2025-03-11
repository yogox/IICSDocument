A referenced catalog source indicates that the catalog source that you configured includes references from other source systems. Assets from reference catalog sources are known as reference assets.

When you configure a catalog source in Metadata Command Center, it might contain lineage information and connection data from other source systems that don't exist in the catalog. Though the information about the source system does not exist in the catalog, you can still view the source system as a reference catalog source and view lineage for the assets in the configured catalog source with the reference assets from the reference catalog source.

You can configure predefined or custom catalog sources to view the lineage with reference assets from reference catalog sources. After extracting reference assets,Data Governance and Catalog displays the reference catalog source and the lineage for the asset in the catalog with the reference assets. To link the reference assets to actual objects and to view the complete lineage, assign connections between the reference catalog source and the actual catalog source that you configure in Metadata Command Center. For example, you have configured an Informatica PowerCenter catalog source that contains mappings that point to tables or columns in an Oracle database. The Oracle database is the reference catalog source and the tables and columns in the Oracle database are reference assets from the reference catalog source. To view the column details from an Oracle table referenced by the PowerCenter catalog source, configure the Oracle catalog source in Metadata Command Center and then perform connection assignments between the reference catalog source and the schema in the Oracle source system.

You can also assign glossary terms to reference assets to enrich them.

## Assign connections to reference catalog sources

Assigning a connection to reference catalog source involves assigning connections from the reference catalog source to the catalog source that represents the source system.

Assign connections for reference catalog sources to link the reference assets to actual objects in the source system and to view complete lineage. Before you assign connections, configure the catalog source for the reference source system. See Creating a catalog source.

You can then assign connections between the reference catalog source and the configured catalog source. For information about assigning connections, refer to the Administration help. When you assign connections to reference catalog sources, the reference assets map to the actual objects in the configured source system.

After you assign connections to reference catalog sources, you can view the complete lineage including actual assets from the source that you configured the connection to. If you had enriched reference assets with business terms, the terms are associated with the catalog source after connection assignment.
