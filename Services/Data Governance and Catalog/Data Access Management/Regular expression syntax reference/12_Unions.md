Use the pipe character to union together two distinct sub-expressions. This creates an expression that can produce either expression.

For example, the expression id|identification produces either of the following tokens:

- id
- identification

You can use parentheses to shorten the expression. For example, the expression id(""|entification) produces either of the following tokens:

- id
- identification

You can combine any number of elements into a union. For example, the expression oranges|berries|bananas|(red|green) apples produces any of the following tokens:

- oranges
- berries
- bananas
- red apples
- green apples
