# The while Statement

The while statement is a loop statement with an exit test at the beginning of the loop. Here is the general form of the while statement:

```text
while (test) loop
  statement
end loop;
```

The while statement first evaluates test. If test evaluates to true, statement is executed, and then test is evaluated again. Statement continues to execute repeatedly as long as test is true after each execution of statement. 

This example prints the integers from zero through nine:

```text
int counter = 0;
while (counter < 10) loop
  message(counter);
  counter = counter + 1;
end loop;
```

A [break statement](the-break-statement.md) can also cause a while loop to exit.

