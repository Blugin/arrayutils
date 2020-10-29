---
description: Prefixing "From" to the any methods can called statically.
---

# ⚡ Prefix - From

### Prefixing "From" to the any methods can called statically. It can be used by giving an `iterable` as the first argument.



{% tabs %}
{% tab title="Example" %}
```php
$arr = ArrayUtils::reverseFrom([1,2,3,4,5]);

var_export((array) $arr);
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1
```
{% endtab %}

{% tab title="is same to" %}
```php
$arr = ArrayUtils::from([1,2,3,4,5])->reverse();

var_export((array) $arr);
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1
```
{% endtab %}
{% endtabs %}

