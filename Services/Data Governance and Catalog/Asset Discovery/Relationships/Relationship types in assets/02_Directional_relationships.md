I'll convert this HTML into Markdown for you, following your requirements.

# Directional relationships

You can create the following types of directional relationships.

## Outbound and inbound relationships

The relationship that you create from the open asset to another asset is called an outbound relationship. A blue arrow pointing to the right direction represents an outbound direction.

Whereas, the relationship that you create from another asset to the open asset is called an inbound relationship. An orange arrow pointing to the left direction represents an inbound direction.

## Direct and indirect relationships

When you connect assets to each other in Data Governance and Catalog, the relationships can be direct or indirect.

When an asset is connected directly to the primary asset, the relationship is called a direct relationship. Direct relationships in Data Governance and Catalog are represented by plain lines.

When an asset is connected to the primary asset through another asset, the relationship is called an indirect relationship. Indirect relationships in Data Governance and Catalog are represented by dotted lines.

The following image shows an example of a direct and an indirect relationship created with the "Medical Reimbursement" policy asset. The "Costs Reimbursement" process asset is in a direct relationship with the primary policy asset. The "CostsReimb.pdf" technical asset is connected to the primary policy asset through the "Costs Reimbursement" process asset and is in an indirect relationship with the primary policy asset.

![Image depicting a direct and an indirect relationship of the primary policy asset with other assets.](https://docs.informatica.com/content/dam/source/GUID-0/GUID-02334EA6-2438-4E0B-9F6E-C649FEB33C45/1/en/GUID-862CA9E6-7B5D-4E03-ADCF-6F751B733A30-low.png)

## Relationship example

The following image shows a sample asset and the different types of relationships with other assets:

![Image depicting a sample asset depicting the directional relationships with other assets.](https://docs.informatica.com/content/dam/source/GUID-0/GUID-02334EA6-2438-4E0B-9F6E-C649FEB33C45/1/en/GUID-580B8B5B-AE65-4EF4-A455-93B454F9F6C6-low.png)

In the image, the business term 'Delivery Cost' is the open asset. The Relationships tab shows the grid view of all the assets related to 'Delivery Cost'.

1. The highlighted policy asset 'Gov Policy 01' is related to the open asset through an inbound relationship, which is indicated by the orange arrow pointing to the left direction. This indicates that the relationship between the business term 'Delivery Cost' and the policy 'Gov Policy 01' originated in the policy asset 'Gov Policy 01'. The relationship type 'is Regulating' indicates that the policy asset is regulating the business term.
2. The highlighted system asset 'Customer Call Analysis Reports' is related to the open asset through an outbound relationship, which is indicated by the blue arrow pointing to the right direction. This indicates that the relationship between the business term 'Delivery Cost' and the system 'Customer Call Analysis Reports' originated in the business term 'Delivery Cost'. The relationship type 'is a Strategic Source for' indicates that the business term is the preferred or recommended source of data for the system asset.
