# Function Declarations

A function declaration ends with a semicolon. Here is the general form:

```text
return-type function-name (parameter-list) {
    function-body
};
```

* return-type indicates the data type of the value returned by the function. You can declare a function that doesn not return anything by using the return type void.
* function-name can be any valid identifier \(see Identifiers\).
* parameter-list consists of zero or more parameters, separated by commas. A typical parameter consists of a data type and an name for the parameter. You can not declare a function that has a variable number of parameters. Functions can have zero parameter leaving parameter-list empty.

Here is an example of a function declaration with two parameters:

```text
int foo (int param1, char param1) {
    function-body
};
```

The parameter names can be any identifier \(see Identifiers\), and if you have more than one parameter, you can't use the same name more than once within a single declaration.

