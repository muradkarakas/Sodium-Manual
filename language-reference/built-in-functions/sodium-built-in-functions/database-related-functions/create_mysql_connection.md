# create\_mysql\_connection

{% tabs %}
{% tab title="Variant 1" %}
```text
char create_mysql_connection(char connectionName, char databaseName, char userName, char userPassword);
```

#### Return Value <a id="return-value"></a>

Nothing if connection has been made successfully. Otherwise, error text as string.

#### Parameters <a id="parameters"></a>

`char connectionName` - unique name to identify this connection in web session

`char databaseName` - Mysql database name

`char userName` - database login user name 

`char userPassword` - database user password

#### Example <a id="example"></a>

```text
void connection_not_found(char connectionName) {
        char connResult;
        connResult = create_mysql_connection('default', 'mysql', 'root', 'password');
}

void cb_mysql.logon2mysql() {
        char connResult;
        connResult = create_mysql_connection('default', 'mysql', 'root', 'password');
        if (connResult is null) then
                show_page('mysql.frmx');
        else
                message('Error occured: ' || connResult);
        end if;
}

```
{% endtab %}
{% endtabs %}

