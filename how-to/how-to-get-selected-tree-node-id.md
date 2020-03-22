# How to: get selected tree node id

## How to: get selected tree node id

 The only way to get selected node's id is to use ["tree\_node\_selected" Trigger](https://sodium.gitbook.io/sodium/language-reference/built-in-triggers/item-level-triggers/tree_node_selected-trigger).

```text
void cb.data.tree_node_selected(char node_id, char parent_id) {
 
        :Global.selectedNodeId = node_id;
        :Global.selectedNodeParentId = parent_id;
 
        refresh_block('product_categories', 'id = ' || node_id);
}
```

​

