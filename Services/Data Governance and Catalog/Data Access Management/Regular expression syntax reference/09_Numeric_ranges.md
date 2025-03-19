You specify numeric ranges by including its endpoints within angle brackets.

For example, the expression &lt;3-6&gt; produces any of the following tokens:

- 3
- 4
- 5
- 6

Note the following limitations when using numeric ranges:

- You must include the same number of digits in both endpoints. For example, &lt;000-999&gt; is valid syntax, but &lt;0-999&gt; is invalid syntax.
- Although the expression produces values within a numeric range, it produces them as strings, not integers.
- Numeric range expressions can produce tokens with leading zeros. For example, the expression &lt;000-999&gt; can produce the tokens 000, 009, and 095.
- You cannot use negative endpoints.
- The endpoints must fit within the Java int limit. The maximum allowed value is 2147483647.
