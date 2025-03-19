The regular expression syntax that Data Access Management uses natively supports Unicode characters.

Note the following about using Unicode characters: 

* Not all Unicode characters are printable.
* In character ranges, Data Access Management interprets the endpoints as points in the Unicode character table. Data Access Management forms a continuous range of all the characters between the endpoints. For example, the expression [A-z] includes the characters: [\]^_` as well as all upper- and lower-case letters.
* In character ranges, if you use an endpoint that comes before the start point in a Unicode table, the expression will produce no values.
