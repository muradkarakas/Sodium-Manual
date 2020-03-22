# "post\_update" Trigger

#### Description

`post_update` trigger is fired after a new row successfully updated in underlying database.

**Declaration**

```text
bool block_name.post_update();
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

