# populate\_tree

`populate_tree` function has 1 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Declaration

```text
void populate_tree(char treeName);
```

#### Description <a id="description"></a>

1. `Needs` [`tree tag`](https://sodium.gitbook.io/sodium/language-reference/html-tags/sodium-tags/tree-element)`in`[`form file`](https://sodium.gitbook.io/sodium/language-reference/program-structure/form-file)​
2. `populate_tree` function initializes the tree element. After successful initializing, ["tree\_node\_expanded" Trigger](https://sodium.gitbook.io/sodium/language-reference/built-in-triggers/item-level-triggers/tree_node_expanded-trigger) will be fired.
3. `treeName` property is a string and should have match the following format: `block name + '.' + tree id`
4.  For detail on json data format: [https://www.jstree.com/docs/json/](https://www.jstree.com/docs/json/)​

#### Parameters <a id="parameters"></a>

`char treeName`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

Form file

```text
<controlblock control-block-name="cbTree">
    <tree id="data"></tree>
</controlblock>
```

Sqlx file

```text
void page.load() {
	 populate_tree('cbTree.data');
}
```
{% endtab %}
{% endtabs %}



