# Data Block

## Description

Data block is the main visual element corresponding to tables/views in database.

With data blocks, end users can:

* see
* sort
* filter and
* manipulate

the data in tables/views.

* Defined in [form file](../../program-structure/form-file.md).
* Data blocks can not be nested.
* Supports two type of view modes. [Data Block: Grid View Mode](data-block-grid-view-mode.md), [Data Block: Form View Mode](data-block-form-view-mode.md) and [Data Block: Mix View Mode](data-block-mix-view-mode.md).
* Data block must only have one [Table TAG](../table-tag.md) element as inner element.

## Declaration

```text
<datablock
    data-block-name     = ""
    data-source-name    = ""
    data-schema-name    = ""
    connection-name     = ""
    auto-generated-columns="*|comma separated column names"
    where-clause        = ""
    order-by-clause     = ""
    master-data-block-name = ""
    join-condition      = ""
    record-count        = ""
    insert-allowed      = "{yes|no}"
    update-allowed      = "{yes|no}"
    delete-allowed      = "{yes|no}"
    show-hide-mode      = {display|visibility}>
</datablock>
```

## Example

```text
<datablock data-block-name="deps" data-source-name="deps" data-schema-name = "htsql"
    where-clause="" order-by-clause="dep_id" record-count="11">
 
    <table>
        <thead>
            <tr>
                <td>DEP ID</td>
                <td>DEP NAME</td>
                <td>EMP.CNT.</td>
                <td>LOGO</td>
                <td>OPS</td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>
                    <input name="dep_id" data-type="number" column-name="dep_id"
                        type="text" size="3" sequence-name="HTSQL"></input>
                </td>
                <td>
                    <input name="dep_name" data-type="char" column-name="dep_name"
                        size="15px" type="text"></input>
                </td>
                <td>
                    <input name="employee_count" data-type="char" size="5px"
                        type="text"></input>
                </td>
                <td>
                    <input name="dep_logo" type="image" height="25px"
                        width="25"></input>
                </td>
                <td>
                    <input name="show_dep_name" type="button" value="Show"></input>
                </td>
            </tr>
        </tbody>
    </table>
 
</datablock>
```

## Properties

### data-block-name property

**Mandatory :** yes  
**Unique :** yes  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### data-source-name property

#### Description

Data source name is the table/view name.

It cannot contain the schema name if the connected/current user is not the owner of the table/view.

It cannot be a sub select/query.

**Mandatory :** yes  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### data-schema-name property

#### Description

Schema name of the the table/view name. 

It can be empty if the current schema/user is the the owner of the table/view.

**Mandatory :** yes  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### connection-name property

#### Description

Property is not mandatory. 

If it is not specified, "default" is used as connection name.

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### where-clause property

#### Description

Do not write "where" keyword in the property value. 

Can contain any legal SQL WHERE condition statement\(s\) \(etc database functions, sub selects\)

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

#### Examples:

```text
emp_name = 'john'  
```

```text
emp_name = 'john' and emp_surname is not null
```

```text
getAge() > 25
```

### order-by-clause property

#### Description

It is SQL "order by" clause. 

Do not write "order by" in the property value. 

Can contain any legal "order by" statements

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

#### Examples

```text
emp_name 
```

```text
emp_name, emp_surname
```

```text
getAge() 
```

```text
(select count(*) from cars where car_id = emp_id)
```

### master-data-block-name property

#### **Description**

It is used to implement master-detail relationship between data blocks.  
It is the master data block name of the current data block.  
A data block can only have one master data block but can have many detail data blocks.  
Master data block must be defined in the [Form File](../../program-structure/form-file.md) before the current data block.  
It works together with [join-condition property](./#join-condition-property)

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

```text
master-data-block-name="deps" join-condition="dep_id = :deps.dep_id" 
```

### join-condition property

#### Description

It is used to implement master-detail relationship between data blocks.  
It is a "where" statement. It should conform the SQL specification  
One of the operands used in join condition statement must reference to the item name of the master data block  
Master data block must be defined in the [Form File](../../program-structure/form-file.md) before the current data block.  
It works together with [master-data-block-name property](./#master-data-block-name-property)

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### record-count property

It is the number of records to be displayed on the screen.

**Mandatory :** yes  
**Unique :** no  
**Data Type :** number  
**Default Value:** -  
**Predefined Values Allowed:** &gt; 0

### insert-allowed property

 **Not implemented yet.**

**Mandatory :** **no**  
**Unique :** no  
**Data Type :** bool  
**Default Value:** yes  
**Predefined Values Allowed:**  {yes\|no}

### update-allowed property

**Not implemented yet.**

**Mandatory :** **no**  
**Unique :** no  
**Data Type :** bool  
**Default Value:** yes  
**Predefined Values Allowed:**  {yes\|no}

### delete-allowed property

**Not implemented yet.**

**Mandatory :** **no**  
**Unique :** no  
**Data Type :** bool  
**Default Value:** yes  
**Predefined Values Allowed:**  {yes\|no}

### show-hide-mode property

CSS show/hide method

**Mandatory :** **no**  
**Unique :** no  
**Data Type :** char  
**Default Value:** visibility  
**Predefined Values Allowed:**  {display\|visibility}

### auto-generated-columns property

 Use `auto-generated-columns property` in order to declare which columns will be shown in data block.

**Mandatory :** **no**  
**Unique :** no  
**Data Type :** char  
**Default Value:** no  
**Predefined Values Allowed:**  { \* \| comma separated column names}

#### Example

```text
<datablock data-block-name="table" auto-generated-columns="*" record-count="10">
</datablock>
 
<datablock data-block-name="emps" auto-generated-columns="emp_id, emp_name" record-count="10">
</datablock>

```

## Triggers

###  ["post\_query" trigger](../../built-in-triggers/post_query-trigger.md)

###  ["row\_selected" trigger](../../built-in-triggers/row_selected-trigger.md)

###  ["pre\_insert" Trigger](../../built-in-triggers/pre_insert-trigger.md)

###  ["pre\_update" Trigger](../../built-in-triggers/pre_update-trigger.md)

###  ["pre\_delete" Trigger](../../built-in-triggers/pre_delete-trigger.md)

###  ["post\_insert" Trigger](../../built-in-triggers/post_insert-trigger.md)

###  ["post\_delete" Trigger](../../built-in-triggers/post_delete-trigger.md)

###  ["post\_update" Trigger](../../built-in-triggers/post_update-trigger.md)

## Allowed Inner HTML Elements

 Must be empty if [auto-generated-columns property](./#auto-generated-columns-property) is set.  
 [Table TAG](../table-tag.md)

## Built-in Functions

 [refresh\_block](../../built-in-functions/sodium-built-in-functions/other-functions/refresh_block.md)  
 [show\_block](../../built-in-functions/sodium-built-in-functions/other-functions/show_block.md)  
 [hide\_block](../../built-in-functions/sodium-built-in-functions/other-functions/hide_block.md)  
 [set\_datablock\_property](../../built-in-functions/sodium-built-in-functions/other-functions/set_datablock_property.md)

## See also

 [Data Block: Form View Mode](data-block-form-view-mode.md)  
 [Data Block: Grid View Mode](data-block-grid-view-mode.md)  
 [Data Block: Mix View Mode](data-block-mix-view-mode.md)

