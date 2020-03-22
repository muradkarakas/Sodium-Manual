# Calling Functions

You can call a function by using its name and supplying any needed parameters. Here is the general form of a function call:

```text
function-name (parameters)
```

A function call can make up an entire statement, or it can be used as a subexpression. Here is an example of a standalone function call:

```text
foo(5); 
```

In that example, the function `foo` is called with the parameter 5.

Here is an example of a function call used as a subexpression:

```text
a = square(5); 
```

Supposing that the function `square` squares its parameter, the above example assigns the value 25 to a.

If a parameter takes more than one argument, you separate parameters with commas:

```text
a = quux(5, 10); 
```

