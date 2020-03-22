# Select Item

## Description

## Declaration

```text
<select
    name            = ""
    column-name     = ""
    datalist-name   = ""
    lookup-input-block-name  = ""
    lookup-input-name        = ""
    data-type               = "{char|number|date}"
    default-value           = ""
    insert-allowed          = "{yes|no}"
    update-allowed          = "{yes|no}">
</select>
```

## Properties

### name Property

**Mandatory :** yes  
**Unique :** yes  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### column-name Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### data-type Property

**Mandatory :** yes  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:**  { char \| number \| date }

### default-value Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### insert-allowed Property 

Not implemented yet

**Mandatory :** no  
**Unique :** no  
**Data Type :** bool  
**Default Value:** yes  
**Predefined Values Allowed:** {yes\|no}

### update-allowed Property

Not implemented yet

**Mandatory :** no  
**Unique :** no  
**Data Type :** bool  
**Default Value:** yes  
**Predefined Values Allowed:** {yes\|no}

### data-list-name Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### lookup-input-block-name Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

###  lookup-input-name Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

## Triggers

###  ["item\_modified" trigger](../../built-in-triggers/item_modified-trigger.md)

## **Allowed Inner HTML Elements**

None

## **Related Built-in Functions**

### [hide\_column](../../built-in-functions/sodium-built-in-functions/other-functions/hide_column.md)

### [show\_column](../../built-in-functions/sodium-built-in-functions/other-functions/show_column.md)

### [disable\_column](../../built-in-functions/sodium-built-in-functions/other-functions/disable_column.md)

### [enable\_column](../../built-in-functions/sodium-built-in-functions/other-functions/enable_column.md)

