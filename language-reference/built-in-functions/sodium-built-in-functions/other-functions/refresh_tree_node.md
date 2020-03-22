# refresh\_tree\_node

`refresh_tree_node` function has 1 variant:

{% tabs %}
{% tab title="Variant 1" %}
#### Declaration

```text
void refresh_tree_node(char blockAndTreeName, char node_id_to_be_refreshed);
```

#### Description <a id="description"></a>

1. `Needs` [`tree tag`](https://sodium.gitbook.io/sodium/language-reference/html-tags/sodium-tags/tree-element)`in`[`form file`](https://sodium.gitbook.io/sodium/language-reference/program-structure/form-file)​
2. Reloads child nodes of the node with `node_id_to_be_refreshed` \(does not reload itself\). If you want to reload and draw the node `node_id_to_be_refreshed`, call this function with the parent id of the `node_id_to_be_refreshed.`

For detail on json data format: [https://www.jstree.com/docs/json/](https://www.jstree.com/docs/json/)​

#### Parameters <a id="parameters"></a>

`char blockAndTreeName`

`char node_id_to_be_refreshed`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>
{% endtab %}
{% endtabs %}

