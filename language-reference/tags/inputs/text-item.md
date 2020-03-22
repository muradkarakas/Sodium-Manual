# Text Item

## Description

## Declaration

```text
<input
    name                = ""
    type                = "text"
    data-type           = "{char|number|date}"
    master-item-name    = ""
    sequence-name       = ""
    value               = ""
    maxlength           = ""
    column-name         = ""
    insert-allowed      = "{yes|no}"
    update-allowed      = "{yes|no}"
    format-mask         = "" />
```

## Properties

### name Property

**Mandatory :** yes  
**Unique :** yes  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### type Property

**Mandatory :** yes  
**Unique :** no  
**Data Type :** char  
**Default Value:** text  
**Predefined Values Allowed:**  { text \| submit \| button \| checkbox \| radio }

### data-type Property

**Mandatory :** yes  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:**  { char \| number \| date }

### master-item-name Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### sequence-name Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### sequence-schema-name Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:**  Data block's schema name  
**Predefined Values Allowed:** -

### value Property 

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### maxlength Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** number  
**Default Value:** -  
**Predefined Values Allowed:** -

### column-name Property

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

### format-mask Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

## Triggers

###  ["item\_modified" trigger](../../built-in-triggers/item_modified-trigger.md)

##  **Allowed Inner HTML Elements**

None

##  **Related Built-in Functions**

### [hide\_column](../../built-in-functions/sodium-built-in-functions/other-functions/hide_column.md)

### [show\_column](../../built-in-functions/sodium-built-in-functions/other-functions/show_column.md)

### [disable\_column](../../built-in-functions/sodium-built-in-functions/other-functions/disable_column.md)

### [enable\_column](../../built-in-functions/sodium-built-in-functions/other-functions/enable_column.md)

