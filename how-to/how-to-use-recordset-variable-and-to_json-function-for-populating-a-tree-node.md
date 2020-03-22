# How to: use Recordset variable and to\_json function for populating a tree node

In order to generate json data from database, record set variable and to\_json function can be used as shown in the example below,

Record set must ;

* have at least 3 columns: "id", "text", "parent".
* If actual table column name is different from "id", "text" and "parent", column alias can be used as showed above.

Record set can optionally have;

* "children" column.  As stated in jsTree documentation, recorset's column value must be either "true" or "false". True means the node has child\(s\) node, false means node is a leaf node and cannot be expanded.

### Example:

**SQLX File:**

**Form File:**

```text
<!DOCTYPE html>
  
 <html>
  
         <head>
                 <title>HT/SQL SHOWCASE (LOCATIONS TREE VIEW)</title>
         </head>
  
         <body>
                 <center>
  
                         <controlblock control-block-name="controlblock">
                                 <input name="show_all" type="button" value="All in one"/>
                                 <input name="show_deps" type="button" value="Departments"/>
                                 <input name="show_grid" type="button" value="Locations (Grid View)"/>
                 <input name="show_tree" type="button" value="Locations (Tree View)"/>
                                 <input name="show_colors" type="button" value="Colors"/>
                                 <input name="show_users" type="button" value="Users"/>
                                 <br />
                                 <br />
                                 <input name="commit" type="button" value="Commit"/>
                                 <input name="rollback" type="button" value="Rollback"/>
                                 |-|
                                 <input name="create-record" type="button" value=" + "/>
                                 <input name="delete-record" type="button" value=" - "/>
                                 |-|
                                 <input name="first-page" type="button" value="<<"/>
                                 <input name="prev-page" type="button" value=" < "/>
                                 <input name="next-page" type="button" value=" > "/>
                                 <input name="last-page" type="button" value=" >> "/>
                                 |-|
                                 <input name="enter-query" type="button" value="Enter Query"/>
                                 <input name="execute-query" type="button" value="Execute Query"/>
                                 <input name="cancel-query" type="button" value="Cancel Query"/>
                                 |-|
                                 <input name="kill-session" type="button" value="Log Out"  redirect-url="/site/pages/deps/logon.frmx"/>
                                 <br />
                                 <br />
                         </controlblock>
  
                         <table style="width: 850px">
                                 <tr>
                                         <td style="vertical-align: top; width: 275px">
                                                 <controlblock control-block-name="cbTree">
                                                         <tree id="data"></tree>
                                                 </controlblock>
                                         </td>
  
                                         <td style="vertical-align: top; width: 250px">
  
                                                 <datablock data-block-name="countries" data-schema-name="htsql" data-source-name="countries"
                                                         order-by-clause="country_name" record-count="10" show-hide-mode="display" master-data-block-name="Session">
                                                         <table>
                                                                 <thead>
                                                                         <tr>
                                                                                 <td>COUNTRY ID</td>
                                                                                 <td>COUNTRY NAME</td>
                                         <td>REGION ID</td>
                                                                         </tr>
                                                                 </thead>
                                                                 <tbody>
                                                                         <tr>
                                                                                 <td>
                                                                                         <input name="country_id" data-type="char" column-name="country_id" style="width: 50px"
                                                                                                 type="text" />
                                                                                 </td>
                                                                                 <td>
                                                                                         <input name="country_name" data-type="char" style="width: 150px"
                                                                                                 column-name="country_name" type="text"/>
                                                                                 </td>
                                         <td>
                                                                                         <input name="region_id" data-type="char" style="width: 50px"
                                                                                                 column-name="region_id" type="text" master-item-name="selectedNodeId"/>
                                                                                 </td>
                                                                         </tr>
                                                                 </tbody>
                                                         </table>
                                                 </datablock>
  
                                                 <datablock data-block-name="provinces" data-schema-name="htsql" data-source-name="provinces"
                                                         order-by-clause="province_name" record-count="10" show-hide-mode="display" master-data-block-name="Session">
                                                         <table>
                                                                 <thead>
                                                                         <tr>
                                         <td>PROVINCE ID</td>
                                                                                 <td>PROVINCE NAME</td>
                                         <td>COUNTRY ID</td>
                                                                         </tr>
                                                                 </thead>
                                                                 <tbody>
                                                                         <tr>
                                         <td>
                                                                                         <input name="province_id" column-name="province_id"     sequence-name="htsql.htsql"
                                                 type="text" style="width: 50px"/>
                                                                                 </td>
                                                                                 <td>
                                                                                         <input name="province_name" column-name="province_name" type="text" style="width: 150px"/>
                                                                                 </td>
                                         <td>
                                                                                         <input name="country_id" column-name="country_id"       type="text" style="width: 50px"
                                                 master-item-name="selectedNodeId"/>
                                                                                 </td>
                                                                         </tr>
                                                                 </tbody>
                                                         </table>
                                                 </datablock>
  
                         <datablock data-block-name="counties" data-schema-name="htsql" data-source-name="counties"
                                                         order-by-clause="county_name" record-count="10" show-hide-mode="display" master-data-block-name="Session">
                                                         <table>
                                                                 <thead>
                                                                         <tr>
                                         <td>COUNTY ID</td>
                                                                                 <td>COUNTY NAME</td>
                                         <td>PROVINCE ID</td>
                                                                         </tr>
                                                                 </thead>
                                                                 <tbody>
                                                                         <tr>
                                         <td>
                                                                                         <input name="county_id" column-name="county_id" sequence-name="htsql.htsql"
                                                 type="text" style="width: 50px"/>
                                                                                 </td>
                                                                                 <td>
                                                                                         <input name="county_name" column-name="county_name"     type="text" style="width: 150px"/>
                                                                                 </td>
                                         <td>
                                                                                         <input name="province_id" column-name="province_id"     type="text" style="width: 50px"
                                                 master-item-name="selectedNodeId"/>
                                                                                 </td>
                                                                         </tr>
                                                                 </tbody>
                                                         </table>
                                                 </datablock>
                                                 
                                         </td>
                                 </tr>
                         </table>
  
                 </center>
         </body>
 </html>
```

**SQLX File:**

```text
void page.load() {
         populate_tree('cbTree.data');
 }
  
 void provinces.post_delete() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeParentId);
 }
 void provinces.post_insert() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeId);
 }
 void provinces.post_update() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeParentId);
 }
  
 void countries.post_delete() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeParentId);
 }
 void countries.post_insert() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeId);
 }
 void countries.post_update() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeParentId);
 }
  
 void counties.post_delete() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeParentId);
 }
 void counties.post_insert() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeId);
 }
 void counties.post_update() {
         refresh_tree_node('cbTree.data', :Session.selectedNodeParentId);
 }
  
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
  
 char cbTree.data.tree_node_expanded(char node_id, char node_type) {
         char json;
         
         /* message('node_id : ' || node_id || '. node_type : ' || node_type); */
         
         if (node_id == '#') then
                 
                 rs =    select 
                                           region_id             as      id,
                                           region_name   as      text,
                                           '#'                   as      parent,
                                           'R'                   as      type,
                                           case (select count(*) from htsql.countries c where c.region_id = r.region_id)
                                                 when 0 then
                                                         'false' 
                                                 else
                                                         'true'
                                                 end                     children
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
                 rs =    select 
                                   country_id    as      id,
                                   country_name  as      text,
                                   cc.region_id  as      parent,
                                   'C'                   as      type,
                                   case (select count(*) from htsql.countries c where c.region_id = cc.region_id)
                                         when 0 then
                                                 'false' 
                                         else
                                                 'true'
                                         end                     children
                                   
                                 from
                                         htsql.countries cc
                                 where
                                         cc.region_id = :node_id;
                 json = to_json(rs);
         end if;
         
         if (node_type == 'C') then
         
                  rs = select 
                                   PROVINCE_ID   as  id,
                                   PROVINCE_name as      text,
                                   country_id    as      parent,
                                   'P'                   as      type,
                                   case (select count(*) from htsql.counties c where c.province_id = cc.province_id)
                                         when 0 then
                                                 'false' 
                                         else
                                                 'true'
                                         end                     children
                                 from
                                         htsql.provinces cc
                                 where
                                         cc.country_id = :node_id;
         
                 json = to_json(rs);
         end if;
         
         if (node_type == 'P') then
         
              rs =       select 
                                 county_id     as        id,
                                 county_name   as        text,
                                 province_id   as        parent,
                                 'false'       as        children
                         from
                                 htsql.counties c
                         where
                                 c.province_id = :node_id;
  
                 json = to_json(rs);
         end if;
         
         return json;
 }
```

### See also: <a id="see-also"></a>

For detail on json data format : [https://www.jstree.com/docs/json/](https://www.jstree.com/docs/json/)

