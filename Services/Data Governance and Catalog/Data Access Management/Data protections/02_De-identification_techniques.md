# De-identification techniques

Data de-identification techniques are behaviors for Data Access Management to apply to a field in a data set to de-identify it, while still preserving data utility. This section provides comprehensive descriptions of available data de-identification techniques.

## Constant value

The constant value data de-identification technique allows you to mask all string values of a given data class with the same piece of text. The input value is always replaced with the constant value. The technique makes a permanent change in the target source system or query output and cannot be re-identified.

The technique supports the string data type.

The following table lists examples of constant values that you might use:

| Field | Formats | Constant value | Output |
|-------|---------|----------------|--------|
| Password | - P@ssw0rd1<br>- MyP@$$w0rd!2345 | ******** | ******** |
| Postal Code | - 12345<br>- AB1 2CD | 00000 | 00000 |

The following image shows the technique on the Create Technique for String type window:

![The image shows the constant value data de-identification technique on the Create Technique for String type window. There is a Technique Type field with "Constant Value" selected. There is a "Constant Value" field. The user has entered five asterisks. "Add Technique" and "X" buttons appear on the window.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-16C7B44D-3873-4CE8-99AD-1AF49D16B510-low.png)

## Generalize date

The generalize date data de-identification technique replaces the input date with a generalized version of the date or a constant date if the input date is outside of your defined date range. The technique makes a permanent change in the target source system or query output and cannot be re-identified.

For timestamp and datetime data types, the format is HH:mm:ss, and the output time is always set to midnight (00:00:00). For example, 16-09-2018T11:33:00 becomes 01-01-2018T00:00:00 if the date is generalized to only preserve the year.

The technique supports the date and timestamp data types.

The following table describes the date generalization options that you can use in the Generalize section:

| Option | Description |
|--------|-------------|
| Preserve **Year** (YYYY) | Retains the year from the input values and generalizes the day and month to 01-01.<br>Note that Data Access Management might still change the year depending on the settings that you select in Protect elderly individuals and Protect minor or underage individuals. |
| Preserve **Month and Year** (MM-YYYY) | Retains the month and year from the input values and generalizes the day to 01.<br>Note that Data Access Management might still change the month and year depending on the settings that you select in Protect elderly individuals and Protect minor or underage individuals. |
| Preserve **Day, Month and Year** (DD-MM-YYYY) | Retains the day, month, and year from the input values.<br>**Note:** You must select either **Protect elderly individuals** or **Protect minor or underage individuals** when you select this option.<br>Note that Data Access Management might still change the day, month, and year depending on the settings that you select in Protect elderly individuals and Protect minor or underage individuals. |

The following table describes the date generalization options that you can use in the Generalize user-defined date range section:

| Option | Description |
|--------|-------------|
| Protect elderly individuals | Returns a constant date value when an input date is above an age threshold that you specify. You enter the threshold in years in the Age field. You can use the option to obscure the birth dates of individuals who are older than an age that you enter.<br>If the difference between the input date and the current date is greater than or equal to the age threshold, Data Access Management returns a constant date.<br>Data Access Management generates the constant date dynamically as the date of data provision minus the number of years in the Age field.<br>If the difference between the input date and the current date is less than the age threshold, Data Access Management returns the input date with no change.<br>**Note:** The Generalize Date option works in conjunction with any Preserve option that you set. If the date difference is greater than or equal to the age threshold, the Generalize Date option takes precedence over the Preserve option. If the date difference is less than the age threshold, Data Access Management applies the Preserve option and does not generate a constant date. |
| Protect minor or underage individuals | Returns a constant date value when an input date is below an age threshold that you specify. You enter the threshold in years in the Age field. You can use the option to obscure the birth dates of individuals who are younger than an age that you enter.<br>If the difference between the input date and the current date is less than or equal to the age threshold, Data Access Management returns a constant date.<br>Data Access Management generates the constant date dynamically as the date of data provision minus the number of years in the Age field.<br>If the difference between the input date and the current date is greater than the age threshold, Data Access Management returns the input date with no change.<br>**Note:** The Generalize Date option works in conjunction with any Preserve option that you set. If the date difference is less than or equal to the age threshold, the Generalize Date option takes precedence over the Preserve option. If the date difference is greater than the age threshold, Data Access Management applies the Preserve option and does not generate a constant date. |

The Protect elderly individuals and Protect minor or underage individuals options can help you comply with the U.S. Health Insurance Portability and Accountability Act (HIPAA) requirement for the storage of ages and dates contained in patient healthcare data.

For example, if you select "Preserve **Month and Year** (MM-YYYY)," and you specify to generalize the birth date for all individuals older than 90 years old, this would result in the following:

If Data Access Management transforms the data on December 31, 2022, then Data Access Management will generalize any date that is after December 31, 1932 (2022-90=1932) to 01-[original month value]-[original year value]. Data Access Management will generalize any date that is before December 31, 1932 to 01-12-1932. For example, Data Access Management would change the input date of June 2, 1929 (02-06-1929) to 01-12-1932.

Data Access Management would not generalize any date that is equal to December 31, 1932.

Alternatively, if you select "Preserve **Month and Year** (MM-YYYY)," and you specify to generalize the birth date for all individuals younger than 16 years old, this would result in the following:

If Data Access Management transforms the data on December 31, 2022, then Data Access Management will generalize any date that is before December 31, 2006 (2022-16=2006) to 01-[original month value]-[original year value]. Data Access Management will generalize any date that is after December 31, 2006 to 01-12-2006. For example, Data Access Management would change the input date of June 2, 2007 (02-06-2007) to 01-12-2006.

Data Access Management would not generalize any date that is equal to December 31, 2006.

The following image shows the technique on the Create Technique for Date type window:

![The image shows the generalize date data de-identification technique on the Create Technique for Date type window. There is a Technique Type section with "Generalize Date" selected. The Generalize section has "Preserve Month and Year (MM-YYY) selected. The "Generalize user-defined date range" section has "Protect minor or underage individuals" selected. "Add Technique" and "X" buttons appear on the window.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-C4F7E900-B268-48C9-94C9-80017619D861-low.png)

## Hashing

The hashing data de-identification technique replaces input values with hashed values. You can configure the data protection to use one of several hashing functions. The technique makes a permanent change in the target source system or query output. The data can't be re-identified.

The hashing data de-identification technique supports the string data type.

The following table lists the fields you use to configure a hashing data protection:

| Option | Description |
|--------|-------------|
| Hashing Function | Specifies the function used to hash the values. |
| Hashing Mode | Specifies which mode to use when hashing values.<br>"Secret Key Mode (default)" combines the input value with a secret key before hashing the outputs. This is known as "adding pepper" to the values. Use this mode if your organization does not need to combine these values with previously hashed values.<br>"Compatibility Mode" uses the hash function with no secret key to be compatible with other systems. Choose this mode if your organization needs to combine these values with previously hashed values. |

The following image shows the technique on the Create Technique for String type window:

![The image shows the hashing data de-identification technique. A field titled "Hashing Function" includes a list where a user can select a hash function. The user has selected the function SHA-512. There is another field where the user can select a hashing mode. The user has selected the default, which is Secret Key Mode. "Add Technique" and "X" buttons appear on the window.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-6082A67D-3E2F-4E45-8785-78AC80BEAD4A-low.png)

## Redact with null

The redact with null data de-identification technique allows you to replace all field values in a column with null. All users see the column. The technique makes a permanent change in the target data source or query output and the data cannot be re-identified.

The technique supports all data types.

The technique is useful when you want to remove field values while preserving the schema of the asset after the data transformation. Maintaining the original schema is often critical to correct processing by data integration, data replication, or data virtualization tools. Maintaining the original schema might be required to support software development and testing and when working with third-party applications.

## Retain

The retain data de-identification technique allows you to retain field values. No masking behavior takes place.

The retain data de-identification technique supports all data types.

## Substitute value

The substitute value data de-identification technique replaces input values with human-readable substitutes that you provide. In some use cases, you might prefer these substitutes to tokenized values. You can configure the data protection to substitute values consistently or randomly. The technique makes a permanent change in the target source system or query output. The data can't be re-identified.

The substitute value data de-identification technique supports the string data type. Regardless of the content of a value, the technique treats it as a string. The technique supports Unicode characters.

When you create the substitute values file, organize it as follows:

- Create a single list of values in one column.
- Do not include a header row.
- Separate each value with a line break.

The following table lists the fields you use to configure a substitute value data protection:

| Option | Description |
|--------|-------------|
| File Name | Specifies the name of the file that includes the substitution values.<br>To make the substitution values file available for use with Data Integration, verify that the file is in the following location where the Secure Agent is installed:<br>`<Secure Agent installation directory>\apps\Data_Integration_Server\data`<br>To make the substitution values file available for use with Data Marketplace, verify that the file is in the following location where the Secure Agent is installed:<br>`<Secure Agent installation directory>\apps\Data_Access_Management_Proxy\conf\vaultless-lookup-dictionaries` |
| Consistency Behavior | Specifies whether to substitute values consistently or randomly.<br>"Consistently Substitute" means that the same substitute value always replaces the same input value. However, the same substitute value might replace more than one input value. The cardinality of the input set and the size of the substitution list determines the likelihood that the same substitute value replaces more than one input value. |

In consistent substitution, substitute values replace input values consistently but not uniquely.

The following table illustrates this concept with an example of using the "Consistently Substitute" option:

| Input Values | Possible Substitution Values | Output Values |
|--------------|------------------------------|---------------|
| Rodrigo | James | Briana |
| Rodrigo | Jonathan | Briana |
| Kim | Jose | Jose |
| Kim | Karim | Jose |
| Carl | Briana | Briana |
| Carl | Luanne | Briana |

Note that Briana always substitutes Rodrigo and Jose always substitutes Kim. However, Briana also always substitutes Carl. Therefore, Briana is not unique, but it consistently replaced input values.

In random substitution, each row is distinct from others.

The following table illustrates an example of using the "Randomly substitute values" option:

| Input Values | Possible Substitution Values | Output Values |
|--------------|------------------------------|---------------|
| Rodrigo | James | Briana |
| Rodrigo | Jonathan | Karim |
| Kim | Jose | Briana |
| Kim | Karim | James |
| Carl | Briana | Luanne |
| Carl | Luanne | Karim |

Note that while Briana substitutes Rodrigo in the first row, any possible substitution value can replace Rodrigo in the second row.

The following image shows the technique on the Create Technique for String type window:

![The image shows the substitute value data de-identification technique on the Create Technique for String type window. In a field titled "File Name," the user has entered "Substitute.xls" as a file name. Another field is titled "Consistency Behavior." The user has selected "Consistently Substitute." "Add Technique" and "X" buttons appear on the window.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-F91BC404-3CD3-4D84-92AC-840D11E7F382-low.png)

**Note:** For details on using the File Name field, see the "File Name" row in the table that lists the fields you use to configure a substitute value data protection at the beginning of this section.

## Tokenize

The tokenize data de-identification technique replaces sensitive data with randomly generated equivalents, called tokens. Tokens are synthetic, alphanumeric values that stand in for the original sensitive data. You define the input value and output token format using the regular expression syntax.

**Note:** To create tokens, Data Access Management uses the FF1 format-preserving encryption cipher. This cipher is based on the Advanced Encryption Standard (AES) cipher.

The tokenize data de-identification technique supports the string and integer data types. The regular expression syntax specifies a pattern for the generated string.

For example, to replace the value abcdef with a randomly generated six-letter string, use the regular expression syntax [a-z]{6}. This produces the value mvskyc.

To replace the initial value 1234 with a randomly generated four-digit number, use the regular expression syntax [1-9]{4}. This produces the value 4159.

For integers, the range of potential minimum and maximum values that Data Access Management can generate based on the expression must be compatible with the data types the technique is applied to. For example, if your input data type stores numbers from -100 to 100, define an expression that limits output to that range.

The following table lists the fields you use to configure a tokenize data protection:

| Option | Description |
|--------|-------------|
| Regular Expression | The syntax that specifies a pattern for the generated string.<br>For details on the supported regular expression-style syntax, see Regular expression syntax reference. |
| Consistency Behavior | Consistently Tokenize ensures that Data Access Management always replaces the same input value with the same token.<br>Randomly Tokenize ensures that Data Access Management always replaces the same input value with unique tokens. Data Access Management does not preserve data consistency and might duplicate tokens. |

With Consistently Tokenize, Data Access Management replaces raw text or numeric values with a token derived from the encrypted value of the input. In this case, the application of a tokenize data de-identification technique to tokenize data is *consistent*, meaning that the same input value always results in the same token whenever the same rule processes it.

With Randomly Tokenize, Data Access Management replaces raw text or numeric values with randomly generated tokens. In this case, the application of a tokenize data de-identification technique to tokenize data is *inconsistent*, meaning that token duplication is allowed. There will likely be multiple tokens for the same input value if it occurs more than once in the data.

Using Consistently Tokenize is required if a keyed relationship, such as maintaining referential integrity, is to be maintained across several de-identified tables. For rules that you configure to mask or tokenize consistently, you might optionally allow for unmasking of original values. That is, you can enable re-identification of data that was de-identified through that rule.

**Note:** When using consistent tokenize, Data Access Management expects all data values to match the regular expression. If all the data values do not match the regular expression, the request will fail and return an error. For example, if a tokenize data de-identification technique specifies a capital letter, for example [A-Z][a-z]{1,15}, and the data doesn't include a capital letter, Data Access Management returns an error.

When creating tokenize data de-identification techniques, you can use any UTF-8 character block. For example, Data Access Management supports the regular expression [a-z]{10}[ก-ฯ]{10}, which includes both Basic Latin and Thai characters.

However, you cannot mix UTF-8 blocks within the same regular expression component. For example, you cannot use both Basic Latin and Thai characters in the same regular expression component, for instance [a-ก]{3}.

The following table lists examples of regular expressions that you can use to replace the value in a given format:

| Field | Sample Input | Expression |
|-------|--------------|------------|
| Email Address | williamjohnson@samplecompany.com | [a-z]{7}\@[a-z]{5}\.com |
| Last Name | johnson | [a-z]{15} |
| Employee ID (For example, 52938486) | 12345678 | [1-9]{8} |
| U.S. ZIP Code (For example, 93612) | 12345 | [1-9]{5} |

The following image shows the technique on the Create Technique for String type window:

![The image shows the tokenize data de-identification technique on the Create Technique for String type window. The user has entered [0-9]{5} in the "Regular Expression" field. In the "Consistency Behavior" field, the user has selected "Consistently Tokenize." "Add Technique" and "X" buttons appear on the window.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-7CA9D466-F718-4FC2-A1CC-A25619273AFC-low.png)

## Truncate

The truncate data de-identification technique removes part of the input value. You can configure the data protection to start from the beginning or end of the value. By default, the technique starts from the left. The technique makes a permanent change in the target source system or query output. The data can't be re-identified.

The truncate data de-identification technique supports the string data type.

The following table lists the fields you use to configure a truncate data protection:

| Option | Description |
|--------|-------------|
| Number of characters to truncate | Specifies the number of characters to remove or preserve in an input value. |
| Truncate Options | Select Clip First Few Characters to remove characters from the left side of the string.<br>Select Clip Last Few Characters to remove characters from the right side of the string.<br>Select Retain First Few Characters to retain characters from the left side of the string.<br>Select Retain Last Few Characters to retain characters from the right side of the string. |

For example, you want to remove three characters from the United Kingdom post code SE1 8DJ. If you specify three characters, starting from the left, and you select Preserve characters, Data Access Management returns SE1 for the post code. If you specify three characters, starting from the left, and you do not select Preserve characters, Data Access Management returns 8DJ for the post code.

The following image shows the technique on the Create Technique for String type window:

![The image shows the truncate data de-identification technique. In the field titled "Number of characters to truncate," the user entered the number 4. In the "Truncate Options" section, the user selected "Clip First Few Characters." "Add Technique" and "X" buttons appear on the window.](https://onlinehelp.informatica.com/iics/prod/dgc/en/ae-data-accessmanagement/images/GUID-8C2E46B9-8729-4DAE-B514-658A82EEBD6F-low.png)
