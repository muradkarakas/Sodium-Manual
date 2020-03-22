# get\_database\_type

 `get_database_type` function has 1 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

1. Returns the database vendor name of the connection whose name passed as a first parameter. If the connection does not exist, returns null.

#### Declaration <a id="declaration"></a>

```text
char get_database_type(char connectionName);
```

#### Parameters <a id="parameters"></a>

`char connectionName` Connection name.

#### Return Value <a id="return-value"></a>

1. Returns 'oracle' for Oracle database.
2. Returns 'postgresql' for PostgreSQL database

#### Example <a id="example"></a>

```text
void dual.show_database_type() {
        char info = get_database_type('default');
        message(info);
}
```
{% endtab %}
{% endtabs %}

