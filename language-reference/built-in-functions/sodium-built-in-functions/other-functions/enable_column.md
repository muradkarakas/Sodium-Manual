# enable\_column

`enable_column` function has 1 variant:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

1.  Enables the data block's column specified with `blockAndItemName` parameter.
2.  `blockAndItemName` should have the following format: `block name + '.' + item name`

#### Declaration <a id="declaration"></a>

```text
void enable_column(char blockAndItemName);
```

#### Parameters <a id="parameters"></a>

`char blockAndItemName`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

```text
enable_column('deps.dep_name');
```
{% endtab %}
{% endtabs %}

