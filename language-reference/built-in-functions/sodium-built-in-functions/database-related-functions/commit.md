# commit

 `commit` function has 2 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

 Sends `commit` command to the database through `default` connection.

#### Declaration <a id="declaration"></a>

```text
void commit();
```

#### Parameters <a id="parameters"></a>

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>
{% endtab %}

{% tab title="Variant 2" %}
#### Description <a id="description-1"></a>

 Sends `commit` command to the database through connection whose name is passed as argument `connectionName`.

#### Declaration <a id="declaration-1"></a>

```text
void commit(char connectionName);
```

#### Parameters <a id="parameters-1"></a>

* `char connectionName` - Connection name to be commited.

#### Return Value <a id="return-value-1"></a>

#### Example <a id="example-1"></a>
{% endtab %}
{% endtabs %}

