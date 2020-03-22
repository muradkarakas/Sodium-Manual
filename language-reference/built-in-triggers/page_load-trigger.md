# "page\_load" trigger

#### Description

`page_load` trigger function is optional. if it is needed, must be in [Code Behind File](../program-structure/code-behind-file.md).  
 For each [Form File](../program-structure/form-file.md) request, `page_load` trigger function has been executed once.

In `page_load` trigger function:

* All Sodium elements defined in form file,
* Functions and variables defined in code behind and controller file are available/accessible.

**Declaration**

```text
void page_load();
```

#### **Example**

```text
void page_load() {
        rsSchemaOwners =        select owner as label, owner as value
                                                from all_objects s
                                                group by  owner;
        populate_datalist('schemas', rsSchemaOwners);
 
        rsObjectTypes  =        select owner as schema_name, object_type as label, object_type as value
                                                from all_objects
                                                group by owner, object_type;
        populate_datalist('object_types', rsObjectTypes);
}

```

#### **See also**

