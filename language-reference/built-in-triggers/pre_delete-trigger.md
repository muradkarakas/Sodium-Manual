# "pre\_delete" Trigger

#### Description

   `pre_delete` trigger is fired just before a delete sql command issued to the database. If function returns false, SQL command will not be issued.

**Declaration**

```text
bool block_name.pre_delete();
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

