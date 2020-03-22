# show\_block

`show_block` function has 2 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

Show the data block specified with `blockName` parameter.

#### Declaration <a id="declaration"></a>

```text
void show_block(char blockName);
```

#### Parameters <a id="parameters"></a>

`char blockName`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

```text
show_block('emps');
```
{% endtab %}

{% tab title="Variant 2" %}
#### Description <a id="description-1"></a>

Same as Variant 1 if `cascade` is `false`. if `cascade` parameter is true, shows all detail blocks recursively.

#### Declaration <a id="declaration-1"></a>

```
void show_block(char blockName, bool cascade);
```

#### Parameters <a id="parameters-1"></a>

`char blockName`

`bool cascade`

#### Return Value <a id="return-value-1"></a>

#### Example <a id="example-1"></a>
{% endtab %}
{% endtabs %}

