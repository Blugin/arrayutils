---
description: >-
  The from() static method creates a new, shallow-copied ArrayUtils instance
  from an iterable.
---

# ArrayUtils::from\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

var_export(ArrayUtils::from([3,6,9]));
//ArrayUtils(array(3, 6, 9))

var_export(ArrayUtils::from([1, 2, 3], function($x){ return $x + $x; }));
//ArrayUtils(array(2, 4, 9))
```
{% endcode %}

## Syntax

```php
ArrayUtils::from(iterable $iterable, ?callable $mapFn = null) : ArrayUtils
```

### Parameter

* `$iterable` 
  * Iterable object to convert to an array.
* `$mapFn`  ![](../.gitbook/assets/badge_optional.svg) 
  * Map function to call on every element of the array.

### Return value

* A new `ArrayUtils` instance.

## Polymorphism

This method not have polymorphic element

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/from" caption="" %}

