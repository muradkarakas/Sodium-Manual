# The return Statement

You can use the return statement to end the execution of a function and return program control to the function that called it. Here is the general form of the return statement

`return return-value;`

return-value is an optional expression to return.

If the function's return type is void, then it is invalid to return an expression. You can, however, use the return statement without a return value. 

If the function's return type is not the same as the type of return-value, and automatic type conversion cannot be performed, then returning return-value is invalid. 

If the function's return type is not void and no return value is specified, then the return statement is valid unless the function is called in a context that requires a return value. For example

```text
x = cosine(y); 
```

In that case, the function cosine was called in a context that required a return value, so the value could be assigned to x. 

Even in contexts where a return value is not required, it is a bad idea for a non-void function to omit the return value. 

Here are some examples of using the return statement, in both a void and non-void function:

```text
void print_plus_five(int x) {
  message(x + 5);
  return;
};
```

```text
int square_value(int x) {
  return x * x;
};
```

