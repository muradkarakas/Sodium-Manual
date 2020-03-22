# "post\_delete" Trigger

#### Description

`post_delete` trigger is fired after a new row successfully deleted in the underlying database.

**Declaration**

```text
bool block_name.post_delete();
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

