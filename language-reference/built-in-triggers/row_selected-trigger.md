# "row\_selected" trigger

#### Description

 After a selection of any data block's row, row\_selected trigger is fired.  
 `row_selected` trigger function is optional. if it is needed, must be in [Code Behind File](https://muradkarakas.github.io/Sodium-Manual/code_behind_file.html).  
 `row_selected` trigger has 1 variants.  
 row\_selected trigger is a function with a specific name. Trigger function and its name should conform to the following format:

**Function's name format:**

> blockName + ".row\_selected"

**What can be done in `row_selected` trigger function:**

* Refreshing details block.

**Declaration** 

```text
void RowSelectedTriggerFunctionName(); 
```

#### **Example**

```text
void emps.row_selected() {

	refresh_block('employee_photo');
	refresh_block('cars');

	if (:emps.has_car == 'E') then
		show_block('cars', true);
	else
		hide_block('cars', true);
	end if;

}
```

#### **See also**

