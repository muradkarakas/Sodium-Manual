# Radio Item

## Description

## Declaration

```text
<input
    name                = ""
    column-name         = ""
    type                = "radio"
    data-type           = "{char|number|date}"
    insert-allowed      = "{yes|no}"
    update-allowed      = "{yes|no}"
    checked-value       = ""
    default-value       = "" />
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

### checked-value Property

**Mandatory :** no  
**Unique :** no  
**Data Type :** char  
**Default Value:** -  
**Predefined Values Allowed:** -

### default-value Property

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

