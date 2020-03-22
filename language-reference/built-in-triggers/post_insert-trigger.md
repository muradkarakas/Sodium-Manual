# "post\_insert" Trigger

#### Description

`post_insert` trigger is fired after a new row successfully inserted to the underlying database.

**Declaration**

```text
bool block_name.post_insert();
```

#### **Example**

```text
void product_categories.post_delete() {
        refresh_tree_node('cb.data', :Global.selectedNodeParentId);
}

void product_categories.post_insert() {
        refresh_tree_node('cb.data', :Global.selectedNodeId);
}

void product_categories.post_update() {
        refresh_tree_node('cb.data', :Global.selectedNodeParentId);
}
```

#### **See also**

