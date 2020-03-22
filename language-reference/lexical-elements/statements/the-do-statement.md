# The do Statement

The do statement is a loop statement with an exit test at the end of the loop. Here is the general form of the do statement

```text
do
  statement
while (test);
```

The do statement first executes statement. After that, it evaluates test. If test is true, then statement is executed again. Statement continues to execute repeatedly as long as test is true after each execution of statement. 

This example also prints the integers from zero through nine:

```text
int x = 0;
do
  message(x);
  x = x + 1;
while (x < 10);
```

A [break statement](the-break-statement.md) can also cause a do loop to exit.

