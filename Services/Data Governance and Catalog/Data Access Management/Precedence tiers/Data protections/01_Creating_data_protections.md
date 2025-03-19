# Creating data protections

You create data protections and add them to data de-identification rules, which determine where and when to apply the data protections to data. You start by selecting a data type, then a relevant data de-identification technique, and finally defining how it transforms data.

A data protection can apply a different data de-identification technique per data type. For example, you can stipulate that the same data protection apply the truncate technique to a string, the tokenize technique to an integer, and the redact to null technique to unknown data types.

1. Click Data Access in the left navigation.
2. Click Data De-identification.
3. Click Data Protection.

   A list of current data protections appears.

   The following image shows the Data Protection tab:

   ![The image shows a table on the Data Protection tab that lists the names and descriptions of each data protection, data types associated with each data protection, the lifecycle stage, and the date a user last updated it.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-52FB793B-23FE-4ACA-BCA9-C865B2D66F73-low.png)

4. Click the plus sign. 

   The new data protection page appears.

   The following image shows the new data protection page:

   ![The image shows the new data protection page, which has the following fields: Name, Description, and Reference ID. A Stakeholders section appears at the bottom of the page. "Create" and "X" buttons appear at the top of the page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-A52A6E30-1BD6-4382-8196-C915B264A4AF-low.png)

5. Enter a name for the data protection.
6. Optionally enter a description, a reference ID, and select stakeholders.
7. Click Create.

   The overview page appears.

8. Click Techniques.

   The Unknown/Any technique appears.

9. Click the plus sign to add data types relevant to this data protection.

   When you select a type, the Create Technique window appears.

10. Select a technique type.

    Fields appear to allow you to define the behavior of the data protection. The fields vary depending on the type of data de-identification technique that you select. See De-identification techniques for an explanation of each data de-identification technique.

    The following image shows an example of the fields used to define the behavior of one type of data protection:

    ![The image shows an example of the fields used to define the behavior of a data de-identification technique. The example shows the Truncate data de-identification technique with an "Add Technique" button. Another field is titled "Number of characters to truncate." The user entered the number 3 and selected "Retain First Few Characters." An "X" button appears at the top of the page.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-8AD3A8E4-7B3A-45CA-AAF7-78E7BF722CF0-low.png)

11. Complete the relevant fields to determine the behavior. 
12. Click Add Technique.
13. Click Publish.

    The data protection is now available to add to data de-identification rules.

## Creating default data protections

Before creating any data de-identification policies, Informatica recommends that you create default data protections for retaining values and redacting values to NULL.

1. Follow the instructions in Creating data protections.
2. Name one data protection "Retain Value."
3. Set this data protection for the "Any/Unknown" data type.
4. Assign the Retain data de-identification technique to the data protection.
5. Create a second data protection with the name "Redact With Null."
6. Set this data protection for the "Any/Unknown" data type.
7. Assign the Redact with null data de-identification technique to the data protection.

   You can now select these data protections when creating data de-identification rules.
