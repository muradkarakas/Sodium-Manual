# Like & Not Like Operators

The LIKE conditions specify a test involving pattern matching. Whereas the equality operator \(=\) exactly matches one character value to another, the LIKE conditions match a portion of one character value to another by searching the first value for the pattern specified by the second.

 **Example:**

```text
void if_test_16() {
        char sonuc;
        sonuc = "if test 16 passed";
 
        if (sonuc like "%test%" and sonuc like "%16%" and sonuc like "if%" and sonuc like "%passed") then
                message("if_test_16 test passed ");
        else
                message("if_test_16 test failed");
        end if;
}
```

