# Native SQL support

Functions in [Code Behind File](program-structure/code-behind-file.md) can contain SQL and/or PL/SQL statements. Sodium developers do not need to write additional code in order to run any SQL statement. And also, they do not need to define a string variable in order to construct SQL statement. All type of SQL and PL/SQL commands runs against "default" connection.

## Examples

### **Select Statement**

In the example below, usage of a single "select" statement / cursor is shown. Select statement is assigned a local variable `rs1`. With this assignment, all columns are easily accessible with the syntax

`cursor_variable_name + "." + column_name`

This example also shows how to use data or control block items value as a parameter in where clause. Before executing "select" command, Sodium engine replaces the block variable with its actual value.

```text
void select_example() {
 
    char counter;
    char depname;
    depname = 'mebs';
 
    rs1 =   select *
            from deps
            where
                dep_name = :depname;
 
    counter = 0;
 
    while (rs1) loop
        message(rs1.dep_name);
        next_record(rs1);
        counter = counter + 1;
    end loop;
 
    message("total number of records :" || counter);
}
```

### **Insert Statement**

In the example below, usage of a single "insert" statement is shown. In order to execute `insert` command, there is no additional coding needed. This example also shows how to use data or control block items value as a parameter in "values" clause and sequence. Before executing "insert" command, Sodium engine replaces the block variable with its actual value

```text
void insert_example() {
    insert into hr.deps (DEP_ID, DEP_NAME)
            values (htsql_test.nextval, :depname);
}
```

### **Update Statement**

In the example below, usage of a single "update" statement is shown. In order to execute `update` command, there is no additional coding needed. This example also shows how to use local variable as a parameter in "where" clause. Before executing "update" command, Sodium engine replaces the local value reference with its actual value.

```text
void update_example() {
    char localVariable;
    localVariable = 'admin';
 
    update hr.deps
    set
        dep_name = 'update test'r
    where
        dep_name like '%'|| :localVariable || '%';
}
```

### **Delete Statement**

In the example below, usage of a single "delete" statement is shown. In order to execute `delete` command, there is no additional coding needed. This example also shows how to use local variable as a parameter in "where" clause. Before executing "delete" command, Sodium engine replaces the local value reference with its actual value.

```text
void delete_example() {
    char dep_name;
    dep_name = 'logistic';
 
    delete
        hr.deps
    where
        dep_name = :dep_name;
}
```

### **Database Script Execution**

In the example below, usage of a PL/SQL block is shown. In order to execute PL/SQL block, there is no additional coding needed. Before executing PL/SQL block, Sodium engine replaces the local variable names with its actual value. This happens once for whole PL/SQL block. PL/SQL block is executed as anonymous "PL/SQL block" in database server. The content of the PL/SQL block \(which is between "begin" and "end;" keywords\) are not parsed by Sodium engine for syntax check.

```text
void plsql_example() {
    char depname;
    depname = 'plsql test';
 
    begin
        insert into hr.deps (DEP_ID, DEP_NAME)
        values (htsql_test.nextval, :depname);
        commit;
    end;
}
```

