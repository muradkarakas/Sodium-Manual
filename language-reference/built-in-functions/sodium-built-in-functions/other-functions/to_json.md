# to\_json

`to_json` function has 1 variants:

{% tabs %}
{% tab title="First Tab" %}
#### Declaration

```text
char to_json(recordset rs);
```

#### Description <a id="description"></a>

1. It converts data set `rs` to json data format.
2. Result set must have `id`, `parent`, `text` columns.
3. Result set may optionally have `children`, `icon`, `type` columns as well.
4. If exists, `children` column must have a value of these `true` or `false`.
5.  This funciton is especially designed for ["tree\_node\_expanded" Trigger](https://sodium.gitbook.io/sodium/language-reference/built-in-triggers/item-level-triggers/tree_node_expanded-trigger).

#### Parameters

`recordset rs`

#### Return Value <a id="return-value"></a>

Sql query result set as json format

#### Example

```text
char cbTree.data.tree_node_expanded(char node_id, char node_type) {
	char json;
	
	/* message('node_id : ' || node_id || '. node_type : ' || node_type); */
	
	if (node_id == '#') then
		
		rs =	select 
					  region_id		as	id,
					  region_name 	as	text,
					  '#' 			as	parent,
					  'R'			as	type,
					  case (select count(*) from htsql.countries c where c.region_id = r.region_id)
					  	when 0 then
					  		'false' 
					  	else
							'true'
						end 			children
					from
						htsql.regions r;
        if (rs) then
            /*  */
            json = to_json(rs);
        else
            json = '[ { "id" : "no_region", "parent" : "#", "text" : "Click here to add new region" } ]';
        end if;
	end if;
		
	if (node_type == 'R') then		
		rs =	select 
				  country_id	as	id,
				  country_name 	as	text,
				  cc.region_id	as	parent,
				  'C'			as	type,
				  case (select count(*) from htsql.countries c where c.region_id = cc.region_id)
				  	when 0 then
				  		'false' 
				  	else
						'true'
					end 			children
				  
				from
					htsql.countries cc
				where
					cc.region_id = :node_id;
		json = to_json(rs);
	end if;
	
	if (node_type == 'C') then
	
		 rs = select 
				  PROVINCE_ID	as  id,
				  PROVINCE_name as	text,
				  country_id	as	parent,
				  'P'			as	type,
				  case (select count(*) from htsql.counties c where c.province_id = cc.province_id)
				  	when 0 then
				  		'false' 
				  	else
						'true'
					end 			children
				from
					htsql.provinces cc
				where
					cc.country_id = :node_id;
	
		json = to_json(rs);
	end if;
	
	if (node_type == 'P') then
	
	     rs = 	select 
			  	county_id     as	id,
			  	county_name   as	text,
			  	province_id   as	parent,
			  	'false'       as	children
			from
				htsql.counties c
			where
			  	c.province_id = :node_id;

		json = to_json(rs);
	end if;
	
	return json;
}
```
{% endtab %}
{% endtabs %}

