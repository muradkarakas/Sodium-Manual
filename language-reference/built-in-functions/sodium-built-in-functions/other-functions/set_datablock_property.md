# set\_datablock\_property

`set_datablock_property` function has 1 variant:

{% tabs %}
{% tab title="Variant 1" %}
#### Declaration

```text
void set_datablock_property(char dataBlockName, char propertyName, char schemaName, char schemaObjectName);
```

#### Description <a id="description"></a>

#### Parameters <a id="parameters"></a>

1. `char dataBlockName`
2. `char propertyName:` 

   Must be one of these:

   data-source-name: Sets the data-source-name property of the data block dataBlockName. Data block's auto-generated-columns property must be set to '\*' value if you get meaningful result from that function.

3. `char schemaName`
4. `char schemaObjectName`

#### Return Value

#### Example

```text
void cb2.schema_object(char oldValue) {
 
        if (:cb2.object_type == 'TABLE' or :cb2.object_type == 'VIEW') then
                set_datablock_property('table', 'data-source-name', :cb1.schema_name, : cb2.schema_object);
                refresh_block('table');
                show_block('table');
        else
                hide_block('table');
        end if;
 
}
```
{% endtab %}
{% endtabs %}

