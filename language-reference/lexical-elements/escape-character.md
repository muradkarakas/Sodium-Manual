# Escape Character

 Escape Character is `\`.

```text
void provinces.row_selected() {
        refresh_block('counties', 'province_id = \'' || :provinces.province_id || '\'');
}
```

