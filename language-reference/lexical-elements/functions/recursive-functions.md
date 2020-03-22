# Recursive Functions

Recursive Functions is supported.

You can write a function that is recursive \(a function that calls itself\). Here is an example that computes the factorial of an integer:

```text
int factorial(int x) {
    if (x < 1) then
        return 1;
    else
        return (x * factorial (x - 1));
    end if;
};
```

Be careful that you do not write a function that is infinitely recursive. In the above example, once x is 1, the recursion stops. However, in the following example, the recursion does not stop until the program is interrupted or runs out of memory:

```text
int watermelon (int x) {
  return watermelon(x);
};
```

Functions can also be indirectly recursive, of course.

