# Logical Operators

Logical operators test the truth value of a pair of operands.

* The logical conjunction operator `and` tests if two expressions are both true. Even thought the first expression is false, the second expression will be evaluated.

```text
if ((x == 5) and (y == 10)) then
    message("x is 5 and y is 10");
end if;
```

* The logical disjunction operator `or` tests if at least one of two expressions it true. Even thought the first expression is true, the second expression will be evaluated.

```text
if ((x == 5) or (y == 10)) then
   message("x is 5 or y is 10");
end if;
```

* You can prepend a logical expression with a negation operator `!` to flip the truth value. The logical expression must be between parenthesis.

```text
if (!(x == 5)) then
    message("x is not 5");
end if;
```

