You can create expressions with intersections that exclude select values. To do this, you use a tilde character (~) to introduce a complement operator to an expression.
For example, the expression ([0-9]{3})&~(111) can produce any three-digit number between 000 and 999, except for 111.
The & indicates an intersection.
