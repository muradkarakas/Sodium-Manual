# get\_database\_name

 `get_database_name` function has 1 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

Returns the database instance name of the connection whose name passed as a first parameter. If the connection does not exist, returns null.

#### Declaration <a id="declaration"></a>

```text
char get_database_name(char connectionName);
```

#### Parameters <a id="parameters"></a>

`char connectionName` Connection name.

#### Return Value <a id="return-value"></a>

Returns the database instance name of the connection if exists. Otherwise, returns null.

#### Example <a id="example"></a>

```text
void cb.show_database_name() {
        char info = get_database_name('default');
        message(info);
}
```
{% endtab %}
{% endtabs %}

