# run\_sql\_file

 `run_sql_file` function has 1 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

1.  `run_sql_file` function opens and execute all sql commands in the file sequentially.
2. Each sql commands must end wih ';' character.
3. If error occured during execution, the function execution is stopped immediately and

   database specific error message is returned.

4.  Database script file path is relative to the `SodiumServer.Exe` file.
5.  Database script file can contain DML or DDL statements but cannot contain `begin` and `end` block since Sodium executes each command separated by ';' character.

#### Declaration <a id="declaration"></a>

```text
char run_sql_file(char filePath);
```

#### Parameters <a id="parameters"></a>

`char filePath` Sql script file full path.

#### Return Value <a id="return-value"></a>

Returns error message if any error message occured.

#### Example <a id="example"></a>

```text
void dual.htsql_demo_installation() {
        char ret = run_sql_file('htsql_demo_installation.sql');
        if (ret is not null) then
                message('Error occured : ' || ret);
        else
                message('Sodium demo schema and objects has been created.');
        end if;
}
```
{% endtab %}
{% endtabs %}

