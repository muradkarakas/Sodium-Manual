# Comparison Operators

You use the comparison operators to determine how two operands relate to each other: are they equal to each other, is one larger than the other, is one smaller than the other, and so on. When you use any of the comparison operators, the result is either true or false, respectively.

* The equal-to operator == tests its two operands for equality. The result is true if the operands are equal, and false if the operands are not equal.

```text
if (x == y) then
    message("x is equal to y");
else
    message("x is not equal to y");
end if;
```

* The not-equal-to operator != or &lt;&gt; tests its two operands for inequality. The result is true if the operands are not equal, and false if the operands are equal.

```text
if (x != y) then
    message("x is not equal to y");
else
    message("x is equal to y");
end if;
```

* Beyond equality and inequality, there are operators you can use to test if one value is less than, greater than, less-than-or-equal-to, or greater-than-or-equal-to another value. Here are some code samples that exemplify usage of these operators:

```text
if (x < y) then
  message("x is less than y");
end if;
 
if (x <= y) then
  message("x is less than or equal to y");
end if;
 
if (x > y) then
  message("x is greater than y");
end if;
 
if (x >= y) then
  message("x is greater than or equal to y");
end if;
```

