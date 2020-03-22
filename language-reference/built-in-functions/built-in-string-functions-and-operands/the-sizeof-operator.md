# The "sizeof" Operator

You can use the `sizeof` operator to obtain the size \(in bytes\) of the data type of its operand. The operand may be an actual type specifier \(such as `int` or `date`\), as well as any valid expression. If the parameter is type of string, you can also use `strlen` function. Here are some examples:

```text
int a = sizeof(int);
int b = sizeof(bool);
int c = sizeof(5);
int d = sizeof(5.143);
int e = sizeof(a);
```

 The result of the `sizeof` operator is of type `int`.

