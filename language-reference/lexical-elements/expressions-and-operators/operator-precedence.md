# Operator Precedence

When an expression contains multiple operators, such as

`a + b * function()`

the operators are grouped based on rules of precedence.

For instance, the meaning of that expression is to call the function f with no arguments, multiply the result by b, then add that result to a. That's what the Sodium rules of operator precedence determine for this expression.

The following is a list of types of expressions, presented in order of highest precedence first. Sometimes two or more operators have equal precedence; all those operators are applied from left to right unless stated otherwise.

* Function calls
* Unary operators, including logical negation, bitwise complement, increment, decrement, unary positive, unary negative, sizeof expressions. When several unary operators are consecutive, the later ones are nested within the earlier ones: !-x means !\(-x\).
* Multiplication, division, and modular division expressions.
* Addition and subtraction expressions.
* Greater-than, less-than, greater-than-or-equal-to, and less-than-or-equal-to expressions.
* Equal-to and not-equal-to expressions.
* Logical AND expressions.
* Logical OR expressions.
* All assignment expressions.
* Comma operator expressions.



