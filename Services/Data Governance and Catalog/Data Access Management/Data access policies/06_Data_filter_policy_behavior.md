Data filter policies are additive and deny access to rows of data.

Data filter policies function in the following ways:

* If there are no data filter policies, Data Access Management grants access to all rows of data.
* For each data filter rule, if the condition is met, Data Access Management denies access to the row or rows.
* Data filter policies are additive. This means that if one policy denies access to one row, and a second policy denies access to a second row, the user will not have access to either row if both policies apply.
