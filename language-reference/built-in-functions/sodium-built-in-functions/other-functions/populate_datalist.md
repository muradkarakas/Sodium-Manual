# populate\_datalist

`populate_datalist` function has 1 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Declaration <a id="declaration"></a>

```text
void populate_datalist(char dataListName, recordset rs);
```

#### Description

1. [&lt;datalist&gt;&lt;/datalist&gt;]() tag is needed in [the form file]().
2. `populate_datalist` function fills the data list by using a select query result. Record set variable is used as a reference to `select` statement.
3.  There is no restriction on sql select query command column names and count. However, the `select` statement must have at least 2 columns named as `label` and `value`.
4. Other columns are added to each option tag of the data list tag as additional attribute and used to filter values for a specific look up item value.
5. If you use "lookup-item-name" in a select tag, your data list \(declared in "datalist-name" of that select tag\) must have additional attribute with the same name \(declared in "lookup-item-name"\).

#### Parameters

`char dataListName`

`recordset rs`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

Frmx file

```text
<datalist id="provinces"></datalist>
 
<datalist id="counties"></datalist>
 
<controlblock control-block-name="cb1">
 <select style="width: 100px" name="province_id"
    datalist-name="provinces">
 </select>
</controlblock>
 
<controlblock control-block-name="cb2">
 <select style="width: 100px" name="county_id" datalist-name="counties"
    lookup-item-block-name="cb1" lookup-item-name="province_id">
 </select>
</controlblock>
```

Sqlx file

```text
void page.load() {
        rsProvinces =   select province_name label, province_id value
                                        from
                                                provinces
                                        order by
                                          province_name;
        populate_datalist('provinces', rsProvinces);
 
        rsCounties =    select county_name label, county_id value, province_id province_id
                                        from
                                                counties
                                        order by
                                          county_name;
        populate_datalist('counties', rsCounties);
}
```
{% endtab %}
{% endtabs %}

