# message

 `message` function has 2 variants:

{% tabs %}
{% tab title="Variant 1" %}
#### Description <a id="description"></a>

Shows a text on browser.

#### Declaration <a id="declaration"></a>

```text
void message(char messageText);
```

#### Parameters <a id="parameters"></a>

`char messageText`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

```text
message('Hello world');
```
{% endtab %}

{% tab title="Variant 2" %}
#### Description <a id="description"></a>

Shows a text on browser with title and style.  

#### Declaration <a id="declaration"></a>

```text
void message(char messageTitle, char messageText, char messageType);
```

#### Parameters <a id="parameters"></a>

`char messageTitle`

`char messageText`

`char messageType` Possible values are `notice`,`error`, `info`, `success`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

```text
message('For Your Information', 'Hello world', 'info');
```
{% endtab %}

{% tab title="Variant 3" %}
#### Description <a id="description"></a>

Shows a text on browser with title in `info messageType` style.

#### Declaration <a id="declaration"></a>

```text
void message(char messageTitle, char messageText);
```

#### Parameters <a id="parameters"></a>

`char messageTitle`

`char messageText`

#### Return Value <a id="return-value"></a>

#### Example <a id="example"></a>

```text
message('For Your Information', 'Hello world');
```
{% endtab %}
{% endtabs %}

