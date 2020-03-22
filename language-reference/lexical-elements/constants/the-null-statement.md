# The Null Statement

The null statement is merely a semicolon alone.

`;`

A null statement does not do anything. It does not store a value anywhere. It does not cause time to pass during the execution of your program.

Most often, a null statement is used as the body of a loop statement, or as one or more of the expressions in a for statement. Here is an example of a for statement that uses the null statement as the body of the loop \(and also calculates the integer square root of n, just for fun\):

for \(i = 1; i\*i &lt; n; i++\) ;

Here is another example that uses the null statement as the body of a for loop and also produces output:

for \(x = 1; x &lt;= 5; printf \("x is now %d\n", x\), x++\) ;

A null statement is also sometimes used to follow a label that would otherwise be the last thing in a block.

