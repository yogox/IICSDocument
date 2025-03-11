# Guidelines for entering rule descriptions

When you enter a description for a data quality rule template, CLAIRE® reads the description and, using Natural Language Processing (NLP) technology, recommends a rule that it can create in the data quality application. You can review the recommended rule and decide whether the rule meets your requirement. If you agree to the recommendation, Data Governance and Catalog creates the rule in the data quality application and associates the rule with the rule template.

Consider the following guidelines when you enter a rule description so that CLAIRE® can recommend appropriate rules: 

* The description can be in any language.
* The description must be within 200 characters and 30 words.
* The description must be in one sentence, and can contain letters, numbers, spaces, and special characters.
* The description can contain UTF-8 characters, spaces, and the following symbols: comma (,), hyphen (-), semi-colon (;), backslash (\), single quote ('), double quotes ("), angle brackets (< and >), equal sign (=), parentheses ({ and }), braces (( and )), square brackets ([ and ]), and period (.)
* Avoid spelling errors while creating a rule.

**Note:** If the business asset name for which you want to run a data quality rule contains an unsupported character, omit the character in the rule description. For example, if a business term is called "Customer_Name", do not enter the underscore in the rule description.

## NLP texts to consider

You can use the following types of NLP rule descriptions. If the text you enter is insufficient or unclear, CLAIRE® might recommend that you rephrase the rule description.

### Empty Value Rules

The following examples show descriptions of null value rules that CLAIRE® NLP technology can read:

* Sum may be NULL
* keep the section field empty
* Box value should be nullified
* Title should be Nothing
* Blank values are equal to null

### Non-Empty Value Rules

The following examples show descriptions of rules that are not null values that CLAIRE® NLP technology can read:

* Age is always NOT NULL
* Name field cannot be blank or empty
* RFID values is not Null
* Radius must not be blank or empty
* doc number is not NULL

### Comparison Rules

The following examples show descriptions of comparison rules that CLAIRE® NLP technology can read:

* Down payment number is greater or equal to thousand
* Down payment is going to either be 1000 or be above 1000
* Value cannot be less than 1,000
* Intensity is lesser than 1,000 lumes
* Bill number is larger or equal to zero

### Range Rules

The following examples show descriptions of range rules that CLAIRE® NLP technology can read:

* Diameter exceeds 0 and doesn't exceed 5
* Diameter is bigger than zero and also Diameter is smaller than five
* Diameter is between one and five, but it cannot be one or five
* Diameter is at least 1 or higher, but not as high as 10
* Diameter can be equal to 1, or be between 1 and 10

### Length Rules

The following examples show descriptions of length rules that CLAIRE® NLP technology can read:

* Zip code must not be longer than 6 characters
* Description should not be greater than 180 letters
* house rent should not exceed beyond 3000
* Only one sentence
* Oil Rig ID is 9 characters long

### List Rules

To define a list, enter markups or delimiters, such as curly braces ({}) and semicolon (;). To facilitate naturally written sentences, you can include conjunctions in the delimiters. Enclose each item of a list within double quotes ("").

The following examples show descriptions of list rules that CLAIRE® NLP technology can read:

* The value of Index is "0", "1" or "2"
* Index shall be equivalent to "yes", "no" or "NA"
* Index will be one of these: "yes", "no", "NA"
* Index should have values within the limit of "yes", "no" and "NA"
* "Yes", "no" or "na" can only be the values that Index can hold
* The values "NA", "Nil", or "None" shouldn't be present in an email ID
* Employee ID should not have values within the limit of "0", "1", or "2"

**Note:** Use double quotes to indicate lists. If at least one double quote is found in the sentence, CLAIRE® NLP technology attempts to read the description as a list rule.

### Date Rules

The following examples show descriptions of date value rules that CLAIRE® NLP technology can read:

* Expiration Date must be a date
* Birthday must be a date
* DOB can have values of type date only
* Joining Date should contain the value of date
* SSN is not of type date

### Number Rules

The following examples show descriptions of number value rules that CLAIRE® NLP technology can read:

* Last name isn't a number
* Number of Seats must be a number
* Salary is numeric
* Phone Number is of type Numeric

## NLP texts to avoid

Avoid the following types of NLP rule descriptions. If the text you enter is insufficient or unclear, CLAIRE® might recommend that you rephrase the rule description.

### Double Negation Sentences

The following examples show descriptions of double negation sentences that CLAIRE® NLP technology cannot read:

* It is not defined city name to be not null
* Distance is not equal to or lesser than NOT NULL
* Date of birth cannot be not null
* It is not acceptable for Phone Number to be not NULL

### Complex Sentences

The following examples show descriptions of complex sentences that CLAIRE® NLP technology cannot read:

* It's not acceptable for date to equal NULL
* Nothing should be populated in name field
* Joining Date should not contain the value of date but contains numbers
* Product is not equal to 2 or not larger than 1

### Grammatically Incorrect Sentences and Incorrect Spellings

The following examples show descriptions of grammatically incorrect sentences and incorrect spellings that CLAIRE® NLP technology cannot read:

* First name should be $NULL
* Serial cannot contain numerics
* Last_name is not a number and alphasnumeric
* Product is nt equal to or nt larger then 1
