# substr

`substr` has 1 variant:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

 `substr` functions allows you to extract a substring from a string.

* If start\_position is 0, then the SUBSTR function treats start\_position as 1 \(ie: the first position in the string\).
* If start\_position is a positive number, then the SUBSTR function starts from the beginning of the string.
* If start\_position is a negative number, then the SUBSTR function starts from the end of the string and counts backwards.
* If length is a negative number, then the SUBSTR function will return a NULL value.

#### Declaration <a id="declaration"></a>

```text
char substr(char string, int startPosition, int length);
```

#### Parameters <a id="parameters"></a>

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

```text
char str;
str = substr("This is a test", 6, 2);
```

Result: "is"

#### See also <a id="see-also"></a>
{% endtab %}
{% endtabs %}

