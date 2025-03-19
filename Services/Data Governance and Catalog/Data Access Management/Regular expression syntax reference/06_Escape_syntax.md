You can escape special characters in an expression by preceding them with a backslash or enclosing them in double quotation marks.

For example, both of the following expressions will produce the same token of &&&&&:

- \&{5}
- "&"{5}

The expression [A-Z\-\\.]{3} will produce any three-character combination of capital English letters, dashes, backslashes, or periods. The following are examples:

- \FC
- -WL
- .KA
