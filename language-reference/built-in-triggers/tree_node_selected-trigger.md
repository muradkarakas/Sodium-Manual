# "tree\_node\_selected" Trigger

#### Description

 Whenever a tree node is clicked, this trigger function is called.

**Declaration**

```text
blockName + '.' + tree element name + '.tree_node_selected' 
```

#### **Example**

```text
void cbTree.data.tree_node_selected(char node_id, char parent_id, char node_type) {
	:Session.selectedNodeId = node_id;
	:Session.selectedNodeParentId = parent_id;

    /* message('node_id : ' || node_id || '. node_type : ' || node_type);  */

    if (node_id == 'no_region') then
        show_page('locations_grid.frmx');
    end if;

	hide_block('countries');
	hide_block('provinces');
	hide_block('counties');
	
	if (node_type == 'R') then
		refresh_block('countries', 'region_id = :node_id');
		show_block('countries');
	end if;
	
	if (node_type == 'C') then
		refresh_block('provinces', 'country_id = :node_id');
		show_block('provinces');
	end if;

	if (node_type == 'P') then
		refresh_block('counties', 'province_id = :node_id');
		show_block('counties');
	end if;
}
```

#### **See also**

 For detail on json data format: [https://www.jstree.com/docs/json/](https://www.jstree.com/docs/json/)

