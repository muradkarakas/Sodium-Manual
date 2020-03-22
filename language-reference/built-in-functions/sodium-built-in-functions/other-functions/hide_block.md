# hide\_block

 `hide_block` function has 2 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

Hides the data block specified with `blockName` parameter.

#### Declaration <a id="declaration"></a>

```text
void hide_block(char blockName);
```

#### Parameters <a id="parameters"></a>

`char blockName`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

```text
hide_block('emps');
```
{% endtab %}

{% tab title="Variant 2" %}
#### Description <a id="description-1"></a>

Same as Variant 1 if `cascade` is `false`. if `cascade` parameter is true, hides all detail blocks recursively.

#### Declaration <a id="declaration-1"></a>

```text
void hide_block(char blockName, bool cascade);
```

#### Parameters <a id="parameters-1"></a>

`char blockName`

`bool cascade`

#### Return Value <a id="return-value-1"></a>

#### Example <a id="example-1"></a>
{% endtab %}
{% endtabs %}

