# Function Calls as Expressions

A call to any function which returns a value is an expression.

```text
int getNumber(void) [
    return 5;
}
 
void test() {
    int a;
    a = 10 + getNumber();
}
```

