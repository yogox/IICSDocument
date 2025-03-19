You use a number in curly brackets to indicate how often an expression can output repeated elements.

For example the expression [a-z]{3} can produce the following three-letter tokens:

- iwx
- hxz
- pfm
- ggi

You can produce variable length strings by using digits separated by a comma. This indicates the range of lengths of the tokens.

For example the expression [a-z]{2,4} can produce strings comprised of two, three, or four lowercase English letters. These might include the following tokens:

- py
- hxz
- pfmz
- gg
