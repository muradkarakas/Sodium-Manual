# "button\_item\_clicked" trigger

#### Description

 `button_item_clicked` trigger function is optional. if it is needed, must be in [Code Behind File](../program-structure/code-behind-file.md) or [Controller File](../program-structure/controller-file.md).  
 Whenever a button in data block or control block is clicked, `button_item_clicked` trigger is fired.  
 \``button_item_clicked` trigger has 1 variant:  
 `button_item_clicked` trigger is a function with a specific name. Trigger function and its name should conform to the following format:

**Function's name format:**

> blockName + "." + buttonName

**Declaration**

```text
void ButtonItemClickedTriggerFunctionName(); 
```

#### **Example**

```text
void deps.show_dep_name() {
        message(:deps.dep_name);
}
```

#### **See also**

