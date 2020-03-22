# refresh\_block

`refresh_block` function has 2 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Declaration <a id="declaration"></a>

```text
void refresh_block(char blockName);
```

#### Description

`refresh_block` function does sequentially:

1. Needs [datablock ]()tag in [form file]().
2. Prepares and executes data block's query.
3. Executes ["post\_query" trigger]() for each row.
4. Sends the new content of the data block to the client.

#### Parameters <a id="parameters"></a>

`char blockName`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

Reads all rows from database and shows them in [data block]().

```text
refresh_block('emps');
```
{% endtab %}

{% tab title="Variant 2" %}
#### Declaration

```text
void refresh_block(char blockName, char whereClause);
```

#### Description <a id="description-1"></a>

Same as Variant 1 except this version filter database rows stated in `whereClause` condition

#### Parameters <a id="parameters-1"></a>

`char blockName`

`char whereClause`

#### Return Value <a id="return-value-1"></a>

#### Example <a id="example-1"></a>

Reads filtered data from database and shows them in [data block]().

```text
refresh_block('emps', 'department_id = ' || :Session.UserDepartmentId);
```
{% endtab %}
{% endtabs %}

