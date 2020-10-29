---
description: Prefixing "As" to the chaining method for returns a pure array.
---

# ⚡ Prefix - As

### Prefixing "As" to the chaining method for returns a pure array. Method chaining breaks if you use this prefix.



{% tabs %}
{% tab title="Example" %}
```php
$arr = ArrayUtils::from([1,2,3,4,5]);

var_export($arr->reverseAs());
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1)
```
{% endtab %}

{% tab title="is same to" %}
```php
$arr = ArrayUtils::from([1,2,3,4,5]);

var_export((array) $arr->reverse());
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1)
```
{% endtab %}
{% endtabs %}

