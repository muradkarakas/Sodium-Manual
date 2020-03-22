# create\_postgresql\_connection

`create_postgresql_connection` function has 1 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

1.  `create_postgresql_connection` creates a new named connection if it does not exist.
2. If connection fails, `create_postgresql_connection` returns error messages as character string. If connection exists, does nothing.
3. This function can be called in any phase of execution, however it is advised to be called in ["connection\_not\_found" trigger](https://sodium.gitbook.io/sodium/language-reference/built-in-triggers/session-level-triggers/connection_not_found-trigger) or in user login page.

#### Declaration <a id="declaration"></a>

```text
char create_postgresql_connection(char connectionName, char instanceName, char userName, char userPassword);
```

#### Parameters <a id="parameters"></a>

* `char connectionName` Name for this Connection in Sodium application
* `char instanceName` Database instance name
* `char userName` Database login user name
* `char userPassword` Database login password

#### Return Value <a id="return-value"></a>

Nothing if connection has been made successfully. Otherwise, error text as string.

#### Example <a id="example"></a>

```text
void cb_oracle.logon2oracle() {
        char connResult;
        connResult = create_oracle_connection('default', :cb_oracle.tnsname, :cb_oracle.user, :cb_oracle.password);
        if (connResult is null) then
                show_page('oracle.frmx');
        else
                message('Error occured: ' || connResult);
        end if;
}
 
void cb_postgresql.logon2postgresql() {
    char connResult;
        connResult = create_postgresql_connection('default', :cb_postgresql.database, :cb_postgresql.user, :cb_postgresql.password);
    if (connResult is null) then
        show_page('postgresql.frmx');
        else
                message('Error occured: ' || connResult);
    end if;
}
```
{% endtab %}
{% endtabs %}

