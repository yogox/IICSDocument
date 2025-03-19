Use square brackets to define a character class. Data Access Management will choose one of the available options.

For example, the expression [abc] produces any of the following tokens:

- a
- b
- c

Within a character class, you can specify a character range with a dash. The range represents all of the characters between and including the start and end of the range. For example, both of the following expressions will produce a token of any letter from the English alphabet:

- [a-z]
- [abcdefghijklmnopqrstuvwxyz]

You can include multiple character ranges in a single character class. For example, the expression [A-Za-z0-9] will produce a token comprised of a single character that is either any English upper- or lower-case letter or any digit.

You can use the caret symbol to negate character classes. For example, the expression [^X] produces all possible Unicode characters, except for X. This is useful when you use it in combination with the intersection operator.
