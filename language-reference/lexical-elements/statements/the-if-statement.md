# The "if" Statement

You can use the if statement to conditionally execute part of your program, based on the truth value of a given expression. Here is the general form of an if statement:

```text
if (test) then
  then-statement
else
  else-statement
end if;
```

If test evaluates to true, then then-statement is executed and else-statement is not. If test evaluates to false, then else-statement is executed and then-statement is not. The else clause is optional. Here is an actual example:

```text
if (x == 10) then
  message("x is 10");
end if;
```

If x == 10 evaluates to true, then the statement message\("x is 10"\); is executed. If x == 10 evaluates to false, then the statement message\("x is 10"\); is not executed.

Here is an example using else:

```text
if (x == 10) then
  message("x is 10");
else
  message("x is not 10");
end if;
```

You can use a series of if statements to test for multiple conditions:

```text
if (x == 1) then
  message("x is 1");
else if (x == 2) then
  message("x is 2");
else if (x == 3) then
  message("x is 3");
else
  message("x is something else");
end if;
```

This function calculates and displays the date of Easter for the given year y:

```text
void easterDate (int y) {
    int n = 0;
    int g = (y % 19) + 1;
    int c = (y / 100) + 1;
    int x = ((3 * c) / 4) - 12;
    int z = (((8 * c) + 5) / 25) - 5;
    int d = ((5 * y) / 4) - x - 10;
    int e = ((11 * g) + 20 + z - x) % 30;
 
    if (((e == 25) && (g > 11)) || (e == 24)) then
        e = e + 1;
    end if;
 
    n = 44 - e;
 
    if (n < 21) then
        n = n + 30;
    end if;
 
    n = n + 7 - ((d + n) % 7);
 
    if (n > 31) then
        message("Easter:" || n-31, "April " || y);
    else
        message("Easter: " || n || "March " || y);
    end if;
}
```

