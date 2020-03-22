# Order of Evaluation

In Sodium you cannot assume that multiple subexpressions are evaluated in the order that seems natural. For instance, consider the expression

`sizeof(a) * f()`

Does this gets size of `a` before or after calling the function f? The interpreter could do it in either order, so you cannot make assumptions.



