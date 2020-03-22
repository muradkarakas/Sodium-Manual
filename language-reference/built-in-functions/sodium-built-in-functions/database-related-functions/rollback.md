# rollback

 `rollback` function has 2 variants:

{% tabs %}
{% tab title="Variant 1" %}
####  <a id="description"></a>

#### Description <a id="description"></a>

 Sends `rollback` command to the database through `default` connection.

#### Declaration <a id="declaration"></a>

```text
void rollback();
```

#### Parameters <a id="parameters"></a>

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>
{% endtab %}

{% tab title="Variant 2" %}
#### Description <a id="description-1"></a>

 Sends `rollback` command to the database through connection whose name is passed as argument `connectionName`.

#### Declaration <a id="declaration-1"></a>

```text
void rollback(char connectionName);
```

#### Parameters <a id="parameters-1"></a>

* `char connectionName` - 

#### Return Value <a id="return-value-1"></a>

#### Example <a id="example-1"></a>
{% endtab %}
{% endtabs %}

