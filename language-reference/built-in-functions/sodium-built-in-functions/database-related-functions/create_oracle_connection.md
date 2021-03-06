# create\_oracle\_connection

`create_oracle_connection` function has 1 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

1.  `create_oracle_connection` creates a new named connection if it does not exist. If connection exists, does nothing.
2. If connection fails, `create_oracle_connection` returns error messages as character string.
3.  This function can be called in any phase of execution, however it is advised to be called in ["connection\_not\_found" trigger](https://sodium.gitbook.io/sodium/language-reference/built-in-triggers/session-level-triggers/connection_not_found-trigger) or in user login page.

#### Declaration <a id="declaration"></a>

```text
char create_oracle_connection(char connectionName, char tnsName, char userName, char userPassword);
```

#### Return Value <a id="return-value"></a>

Nothing if connection has been made successfully. Otherwise, error text as string.

#### Parameters <a id="parameters"></a>

`char connectionName` - unique name to identify this connection in web session

`char tnsName` - Oracle TNS Name

`char userName` - database login user name 

`char userPassword` - database user password

#### Example <a id="example"></a>

```text
void connection_not_found(char connectionName) {
        char connResult;
        connResult = create_oracle_connection('default', 'XE', 'sys', 'password');
        /* or 
              connResult = create_oracle_connection('default', 'hello.world', 'sys', 'password');  
        */
}

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

