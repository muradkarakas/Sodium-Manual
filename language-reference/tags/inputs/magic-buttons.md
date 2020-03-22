# Magic Buttons

Sodium has some built-in features for common operations. Magic buttons are one of them. For the operations below, just declaring a button with specific name is enough to execute desired action.  
  
Writing a ["button\_item\_clicked" trigger](../../built-in-triggers/button_item_clicked-trigger.md) function is not required for Magic Buttons. Therefore, If a trigger function is defined in [Code Behind File](../../program-structure/code-behind-file.md) or [Controller File](../../program-structure/controller-file.md) for any one of the Magic Buttons, it will not be executed. 

Sodium developer may be in need of conditionally execute commands \(commit, rollback, etc\). If that is the case, different button name must be used and its custom trigger function must be defined in [Code Behind File](../../program-structure/code-behind-file.md).

Like other buttons, magic buttons also must be defined in a control or data block.

**For commit:**  
 Execute "commit" command for all active database connections.

```text
<input name="commit" type="button" value="Commit"/>
```

**For rollback:**  
 Execute "rollback" command for all active database connections.

```text
<input name="rollback" type="button" value="Rollback"/>
```

**For creation a new record:**

```text
<input name="create-record" type="button" value="Create"/>
```

**For deleting a record:**

```text
<input name="delete-record" type="button" value="Delete"/>
```

**In order to show first page:**

```text
<input name="first-page" type="button" value="<<"/>
```

**In order to show previous page:**

```text
<input name="prev-page" type="button" value=" < "/>
```

**In order to show next page:**

```text
<input name="next-page" type="button" value=" > "/>
```

**In order to show last page:**

```text
<input name="last-page" type="button" value=" >> "/>
```

**In order to change block status to "enter query" mode:**

```text
<input name="enter-query" type="button" value="Enter Query"/>
```

**In order to execute filtered query on a block:**

```text
<input name="execute-query" type="button" value="Execute Query"/>
```

**In order to cancel "enter query" mode:**

```text
<input name="cancel-query" type="button" value="Cancel Query"/>
```

**In order to kill session**

```text
<input name="kill-session" type="button" value="Log Out" redirect-url="/site/pages/logon.frmx"/>
```

**In order to change current theme**

```text
<select name="theme-selector">
    <option value="default">Sodium Default</option>
    <option value="ocean_blue">Sodium Blue</option>
    <option value="red">Sodium Red</option>
</select>
```

