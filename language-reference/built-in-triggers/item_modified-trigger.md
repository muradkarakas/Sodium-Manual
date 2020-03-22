# "item\_modified" trigger

#### Description

`item_modified` trigger function is optional. if it is needed, it must be in [Code Behind File](https://muradkarakas.github.io/Sodium-Manual/code_behind_file.html).  
 Whenever a control/data block item's value has been changed, item modified trigger is fired.

**Declaration**

Trigger function's name should conform to the following format:

`blockName + "." + itemName`

```text
void ItemModifiedTriggerFunctionName(char oldValue);
```

#### **Example**

```text
void emps.has_car(char oldValue) {
        if ( :emps.has_car == "E" ) then
                show_block("cars", true);
        else
                hide_block("cars", true);
        end if;
}
```

