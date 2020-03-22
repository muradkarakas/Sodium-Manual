# "pre\_insert" Trigger

#### Description

  `pre_insert` trigger is fired just before an insert sql command issued to the database. If function returns false, SQL command will not be issued.

**Declaration**

```text
bool block_name.pre_insert();
```

#### **Example**

```text
bool categories.pre_update() {
        return false;
}
 
bool categories.pre_delete() {
        return false;
}
 
bool categories.pre_insert() {
        return false;
}
```

#### **See also**

