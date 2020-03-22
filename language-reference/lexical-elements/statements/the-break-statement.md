# The break Statement

You can use the break statement to terminate a while, do or switch statement. Here is an example:

```text
int x = 1;
while (x < 1000) loop
    if (x == 8) then
      break;
    else
      message(x);
    end if;
    x = x  + 1;
end loop;
```

That example prints numbers from 1 to 7. When x is incremented to 8, x == 8 is true, so the break statement is executed, terminating the for loop prematurely.

If you put a break statement inside of a loop or switch statement which itself is inside of a loop or switch statement, the break only terminates the innermost loop or switch statement.

