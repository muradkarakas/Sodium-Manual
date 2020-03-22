# "tree\_node\_expanded" Trigger

#### Description

Fired when a tree node is expanded for the first time. That is, If a node does not have the knowledge of its children \(data is not loaded previously\), this trigger is fired. Function's return value is a json data and used to create sub nodes of the triggered node.

**Declaration**

```text
blockName + '.' + tree element name + '.tree_node_expanded' 
```

#### **Example**

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

#### \*\*\*\*

#### **See also**

 For detail on json data format: [https://www.jstree.com/docs/json/](https://www.jstree.com/docs/json/)

