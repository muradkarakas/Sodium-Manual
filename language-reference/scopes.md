# Scopes

Scope refers to what parts of the program can "see" a declared object. A declared object can be visible only within a particular function, or within a particular file, or may be visible to an entire set of files by way of including required files.

Unless explicitly stated otherwise, declarations made at the top-level of a file \(i.e., not within a function\) are visible to the entire file, including from within functions, but are not visible outside of the file.

Declarations made within functions are visible only within those functions.

A declaration is not visible to declarations that came before it; for example:

```text
int x = 5;
int y = x + 10;
```

will work, but:

```text
int x = y + 10;
int y = 5;
```

will not.

